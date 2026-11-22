# Aula 07 — Dashboard de Monitoramento

## Objetivo
Expandir a aplicação anterior para exibir uso de RAM, uso médio de CPU, uptime formatado, quantidade de arquivos, IP principal, status, hostname, tipo de sistema, kernel, arquitetura, endianness, versão do Node e identificação de execução local/cloud.

## Código de referência — `index.js`
```javascript
const express = require('express');
const cors = require('cors');
const os = require('os');
const fs = require('fs');
const path = require('path');
const app = express();
const PORT = process.env.PORT || 3000;
app.use(cors());
app.use(express.static(path.join(__dirname, 'public')));

function contarArquivos(dir) {
  let total = 0;
  for (const item of fs.readdirSync(dir, { withFileTypes: true })) {
    if (item.name === 'node_modules' || item.name === '.git') continue;
    const p = path.join(dir, item.name);
    total += item.isDirectory() ? contarArquivos(p) : 1;
  }
  return total;
}
function obterIP() {
  const interfaces = os.networkInterfaces();
  for (const nome of Object.keys(interfaces)) {
    for (const item of interfaces[nome] || []) {
      if (item.family === 'IPv4' && !item.internal) return item.address;
    }
  }
  return 'Não identificado';
}
app.get('/api/dashboard', (req, res) => {
  const total = os.totalmem();
  const livre = os.freemem();
  const cpus = os.cpus();
  let ocupado = 0, tempoTotal = 0;
  for (const cpu of cpus) {
    const t = cpu.times;
    ocupado += t.user + t.nice + t.sys + t.irq;
    tempoTotal += t.user + t.nice + t.sys + t.irq + t.idle;
  }
  const cloud = Boolean(process.env.RENDER || process.env.RAILWAY_ENVIRONMENT);
  res.json({
    status: 'Operacional',
    ambiente: cloud ? 'Nuvem' : 'Local',
    hostname: os.hostname(),
    sistema: os.type(),
    kernel: os.release(),
    arquitetura: os.arch(),
    endianness: os.endianness(),
    node: process.version,
    memoriaTotal: total,
    memoriaLivre: livre,
    usoMemoria: Number(((total - livre) / total * 100).toFixed(2)),
    usoCPU: Number((tempoTotal ? ocupado / tempoTotal * 100 : 0).toFixed(2)),
    uptime: os.uptime(),
    quantidadeArquivos: contarArquivos(__dirname),
    ipPrincipal: obterIP(),
    porta: PORT,
    modo: process.env.NODE_ENV || 'development'
  });
});
app.listen(PORT, '0.0.0.0', () => console.log(`Dashboard na porta ${PORT}`));
```

Criar `public/index.html`:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head><meta charset="UTF-8"><title>Dashboard SO</title></head>
<body>
<h1>Dashboard de Monitoramento</h1><button onclick="atualizar()">Atualizar</button>
<pre id="painel">Carregando...</pre>
<script>
async function atualizar() {
  const r = await fetch('/api/dashboard');
  const d = await r.json();
  const gb = n => (n / 1024 ** 3).toFixed(2) + ' GB';
  document.getElementById('painel').textContent =
    `Status: ${d.status}\nAmbiente: ${d.ambiente}\nHost: ${d.hostname}\nSO: ${d.sistema}\nKernel: ${d.kernel}\nArquitetura: ${d.arquitetura}\nEndianness: ${d.endianness}\nNode: ${d.node}\nRAM total: ${gb(d.memoriaTotal)}\nRAM livre: ${gb(d.memoriaLivre)}\nUso RAM: ${d.usoMemoria}%\nUso CPU estimado: ${d.usoCPU}%\nUptime: ${Math.floor(d.uptime / 3600)} horas\nArquivos: ${d.quantidadeArquivos}\nIP: ${d.ipPrincipal}\nPorta: ${d.porta}\nModo: ${d.modo}`;
}
atualizar();
</script>
</body></html>
```

**Observações:** a métrica de CPU acima é uma estimativa acumulada desde o início do sistema, não uma amostra instantânea. O IP pode ser interno e não representar o IP público. A identificação cloud por variáveis de ambiente é indicativa.

## Comparação com Railway
Publicar a mesma aplicação no Railway e comparar com Render. Ambas integram repositórios Git e oferecem deploy de aplicações Node.js. Comparar facilidade de configuração, logs, variáveis de ambiente, métricas, disponibilidade e custos do plano vigente. Registrar resultados reais das duas publicações; não presumir qual é mais rápida ou barata sem testar.

## Conclusão
O dashboard permite visualizar recursos do sistema e identificar o ambiente de execução. Na nuvem, os dados pertencem ao servidor remoto, e não ao computador do usuário.
