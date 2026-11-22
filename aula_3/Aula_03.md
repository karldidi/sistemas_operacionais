# Aula 03 — Tipos de SO e Git

## Atividade 1 — Configurar IDE e GitHub
1. Instalar Git: https://git-scm.com/downloads.
2. Verificar no Prompt: `git --version`.
3. Configurar:
   ```bash
   git config --global user.name "Seu Nome"
   git config --global user.email "seu-email@example.com"
   ```
4. Abrir uma pasta no VS Code, criar `README.md` e entrar em Controle do Código-Fonte.
5. Selecionar Inicializar Repositório, adicionar o arquivo e fazer um commit.
6. Entrar na conta GitHub, publicar a branch e confirmar no site que o repositório foi criado.
7. Testar push e pull.

## Atividade 2 — Repositório de teste
```bash
mkdir projeto-teste
cd projeto-teste
git init
```
Criar `README.md`, inserir uma descrição e executar:
```bash
git add README.md
git commit -m "Cria arquivo inicial"
```
Criar um repositório vazio no GitHub e associar:
```bash
git remote add origin https://github.com/SEU-USUARIO/projeto-teste.git
git branch -M main
git push -u origin main
```
Alterar o README e sincronizar:
```bash
git add README.md
git commit -m "Atualiza documentação"
git push
```
Depois de confirmar o envio, apagar a pasta local e clonar novamente:
```bash
git clone https://github.com/SEU-USUARIO/projeto-teste.git
```
Abrir a pasta clonada e conferir se o arquivo foi restaurado corretamente. Só apagar a pasta original depois de confirmar que o push terminou sem erros.

## Atividade 3 — Cinco projetos para clonar e analisar
| Projeto | Repositório | Análise |
|---|---|---|
| Linux | https://github.com/torvalds/linux | Kernel; código C/Assembly, subsistemas e documentação. |
| React | https://github.com/facebook/react | Biblioteca de interfaces; código, testes e instruções para contribuir. |
| Node.js | https://github.com/nodejs/node | Ambiente JavaScript; componentes, testes e documentação de APIs. |
| Docker Docs | https://github.com/docker/docs | Guias, tutoriais, conceitos e exemplos técnicos. |
| Bitcoin | https://github.com/bitcoin/bitcoin | Código da aplicação, testes e instruções de compilação. |

Comandos:
```bash
git clone https://github.com/torvalds/linux.git
git clone https://github.com/facebook/react.git
git clone https://github.com/nodejs/node.git
git clone https://github.com/docker/docs.git
git clone https://github.com/bitcoin/bitcoin.git
```
**Conclusão:** Git controla versões e histórico; GitHub hospeda repositórios remotamente; clone cria uma cópia local do repositório.
