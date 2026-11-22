# Aula 06 — Nuvem e Sistemas Operacionais

## Atividade 1 — Aplicação cloud-so-app
Estrutura:
```text
cloud-so-app/
├── index.js
├── package.json
└── public/index.html
```
Criar o projeto:
```bash
mkdir cloud-so-app
cd cloud-so-app
npm init -y
npm install express cors
mkdir public
```

Arquivo `index.js`:
```javascript
const express = require('express');
const cors = require('cors');
const os = require('os');
const path = require('path');
const app = express();
const PORT = process.env.PORT || 3000;

app.use(cors());
app.use(express.static(path.join(__dirname, 'public')));

app.get('/api/sistema', (req, res) => {
  res.json({
    hostname: os.hostname(),
    plataforma: os.platform(),
    arquitetura: os.arch(),
    quantidadeCPUs: os.cpus().length,
    memoriaTotal: os.totalmem(),
    memoriaLivre: os.freemem(),
    uptimeSegundos: os.uptime()
  });
});

app.listen(PORT, '0.0.0.0', () => {
  console.log(`Servidor executando na porta ${PORT}`);
});
```

Arquivo `public/index.html`:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head><meta charset="UTF-8"><title>Monitor do Sistema</title></head>
<body>
<h1>Informações do Sistema Operacional</h1>
<button onclick="carregar()">Atualizar</button>
<pre id="dados">Carregando...</pre>
<script>
async function carregar() {
  const resposta = await fetch('/api/sistema');
  const d = await resposta.json();
  const gb = n => (n / (1024 ** 3)).toFixed(2) + ' GB';
  const h = Math.floor(d.uptimeSegundos / 3600);
  const m = Math.floor((d.uptimeSegundos % 3600) / 60);
  document.getElementById('dados').textContent =
    `Host: ${d.hostname}\nPlataforma: ${d.plataforma}\nArquitetura: ${d.arquitetura}\nCPUs: ${d.quantidadeCPUs}\nMemória total: ${gb(d.memoriaTotal)}\nMemória livre: ${gb(d.memoriaLivre)}\nTempo ligado: ${h}h ${m}min`;
}
carregar();
</script>
</body>
</html>
```
Executar `node index.js` e abrir `http://localhost:3000`.

## Atividade 2 — GitHub e Render
Criar repositório `cloud-so-app` no GitHub e executar dentro da pasta:
```bash
git init
git add .
git commit -m "Cria aplicação de monitoramento"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/cloud-so-app.git
git push -u origin main
```
No Render, conectar GitHub, criar Web Service, selecionar o repositório, usar `npm install` como Build Command e `node index.js` como Start Command. Publicar e acessar a URL fornecida.

**Comparação:** localmente, os dados representam o computador em que Node está rodando. No Render, representam o servidor remoto. Hostname, plataforma, arquitetura, CPUs, memória e uptime podem ser diferentes.

## Atividade 3 — Conceitos de SO
- **Processos:** Node.js executa como processo e atende requisições HTTP.
- **Memória:** `os.totalmem()` e `os.freemem()` informam memória total e livre do ambiente.
- **CPU:** `os.cpus()` informa os processadores lógicos; quantidade de CPUs não é percentual instantâneo de uso.
- **SO hospedeiro:** sistema que executa o processo Node.
- **Virtualização:** infraestrutura pode isolar aplicações em VMs ou containers.
- **Nuvem:** aplicação fica disponível pela internet em infraestrutura remota.

## Atividade 4 — Manual e conclusão
Documentar instalação das ferramentas, criação dos arquivos, execução local, envio ao GitHub, publicação no Render, testes e comparação. Os valores reais e a URL devem ser preenchidos depois de executar e publicar o projeto; não devem ser inventados.
