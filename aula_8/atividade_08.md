# Aula 08 — Documentação de Software

## Atividade 1 — Documentação de um projeto
**Projeto:** Sistema de Gerenciamento de Tarefas.

**Objetivo:** permitir cadastrar, listar, editar, excluir e concluir tarefas.

**Problema:** tarefas espalhadas em anotações podem ser esquecidas ou ficar desorganizadas. O sistema centraliza as atividades.

**Escopo:** cadastro com título e descrição, listagem, edição, exclusão e marcação de conclusão.

**Requisitos funcionais:**
- RF01: permitir cadastrar uma tarefa.
- RF02: listar tarefas cadastradas.
- RF03: editar título e descrição.
- RF04: excluir uma tarefa.
- RF05: marcar uma tarefa como concluída.

**Requisitos não funcionais:**
- RNF01: interface simples e compreensível.
- RNF02: validar campos obrigatórios.
- RNF03: apresentar mensagens de erro claras.
- RNF04: manter código organizado e documentado.
- RNF05: funcionar em navegadores modernos.

**Tecnologias:** HTML, CSS e JavaScript no front-end; Node.js e Express no back-end; Git e GitHub para versionamento. Um banco de dados pode ser adicionado conforme a evolução.

**Arquitetura:** navegador apresenta a interface e envia requisições HTTP ao Express. O servidor valida os dados, aplica regras de negócio e consulta ou atualiza a persistência.

**Componentes:** interface, rotas, regras de negócio, armazenamento e testes.

## Atividade 2 — README.md
```markdown
# Sistema de Gerenciamento de Tarefas

## Objetivo
Cadastrar, visualizar, editar, excluir e concluir tarefas.

## Funcionalidades
- Cadastro de tarefas
- Listagem
- Edição
- Exclusão
- Marcação como concluída

## Tecnologias
HTML, CSS, JavaScript, Node.js, Express, Git e GitHub.

## Pré-requisitos
Node.js, npm, Git e navegador atualizado.

## Instalação
1. Clone o repositório: `git clone URL_DO_REPOSITORIO`
2. Entre na pasta: `cd nome-do-projeto`
3. Instale as dependências: `npm install`

## Configuração
Se necessário, crie `.env` com variáveis de ambiente.
Exemplo: `PORT=3000`.
Não publique senhas, tokens ou chaves reais.

## Execução
Execute `npm start` e acesse `http://localhost:3000`.

## Testes
Execute `npm test`, quando configurado.
Verifique cadastro, listagem, edição, exclusão e conclusão.

## Estrutura
- `src/`: código da aplicação
- `public/`: interface
- `tests/`: testes
- `docs/`: documentação
- `README.md`: instruções

## Segurança
Não armazene senhas, tokens, chaves de API ou dados pessoais no repositório.
Mantenha arquivos `.env` fora do controle de versão.

## Contribuição
Crie uma branch, faça commits claros e abra Pull Request para revisão.
```

**Conclusão:** documentação de qualidade explica o propósito, requisitos, arquitetura e operação. Um README bem organizado permite que outra pessoa compreenda, instale, execute e teste o projeto sem depender de explicações informais.
