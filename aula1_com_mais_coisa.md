# 🖥️ Aula 01 — Apresentação da Disciplina e Introdução aos Sistemas Operacionais

## 📚 Sumário

* Apresentação da disciplina
* Plano de aulas e ensino
* Contexto da disciplina
* Sequência dos conteúdos do semestre
* Metodologia de ensino
* Critérios de avaliação
* Atividade
* Introdução aos Sistemas Operacionais

---

# 🖥️ Sistemas Operacionais

## O que são?

Um **Sistema Operacional (SO)** é um **software essencial** responsável por gerenciar:

* 💻 Hardware
* 🧩 Software
* 👤 Interface entre usuário e máquina

### Exemplos

| Sistema Operacional | Dispositivo/Contexto      |
| ------------------- | ------------------------- |
| Windows             | Computadores              |
| macOS               | Computadores Apple        |
| Linux               | Computadores e servidores |
| Android             | Dispositivos móveis       |
| iOS                 | Dispositivos móveis Apple |

---

# 🧠 Mapa Mental — Sistemas Operacionais

```text
                         🖥️ SISTEMAS OPERACIONAIS
                                  │
        ┌─────────────────────────┼─────────────────────────┐
        │                         │                         │
        ▼                         ▼                         ▼
   📌 CONCEITO              ⚙️ ESTRUTURA              🔄 PROCESSOS
        │                         │                         │
        ├─ Software essencial     ├─ Camadas                ├─ Escalonamento
        ├─ Gerencia hardware     ├─ Monolítico             ├─ Eficiência
        ├─ Gerencia software     ├─ Modular                ├─ Justiça
        └─ Interface usuário     └─ Kernel                 └─ Tempo de resposta
           ↕ máquina                 │
                                     ├─ Núcleo do SO
                                     ├─ Acesso ao hardware
                                     └─ Gerencia recursos
                                     
        ┌─────────────────────────┼─────────────────────────┐
        │                         │                         │
        ▼                         ▼                         ▼
   🧠 MEMÓRIA              🔌 DISPOSITIVOS             🔐 SEGURANÇA
        │                    E ARQUIVOS                     │
        │                         │                         ├─ Proteção
        ├─ Memória principal     ├─ Gerenciamento de E/S   │  contra ameaças
        │  ├─ Alocação dinâmica  ├─ Sistemas de arquivos  │
        │  └─ Proteção           └─ Organização e acesso  └─ Virtualização
        │                           aos dados
        └─ Memória virtual
           ├─ Expansão lógica
           │  da RAM
           ├─ Paginação
           └─ Segmentação
```

---

# ⚙️ Estrutura Interna

Os Sistemas Operacionais possuem diferentes formas de organização interna.

## 🧱 Estrutura em Camadas

* Organização hierárquica.
* Facilita a modularidade do sistema.

## 🔧 Monolítica e Modular

São diferentes abordagens de design do **kernel**.

## 🧩 Kernel

O **kernel** é o núcleo do Sistema Operacional.

Suas principais funções incluem:

* Acesso direto ao hardware.
* Gerenciamento de recursos vitais.
* Controle das funções essenciais do sistema.

---

# 🔑 Modos de Operação

## 👤 Modo Usuário

É utilizado pelos **programas comuns**.

Possui limitações de acesso aos recursos do sistema.

## ⚡ Modo Kernel

Possui:

* Privilégios elevados.
* Acesso total aos recursos do sistema.

```text
              🔑 MODOS DE OPERAÇÃO
                       │
             ┌─────────┴─────────┐
             ▼                   ▼
       👤 MODO USUÁRIO      ⚡ MODO KERNEL
             │                   │
      Programas comuns     Privilégios elevados
                            Acesso total
```

---

# 🔄 Escalonamento de Processos

O **escalonamento** determina:

> Qual processo será executado e por quanto tempo.

## 🎯 Objetivos

* Eficiência
* Justiça
* Tempo de resposta
* Melhor desempenho geral do sistema

## 📋 Algoritmos apresentados

### FIFO

Primeiro processo a chegar é o primeiro a ser executado.

### Round Robin

Os processos recebem períodos de execução.

### Prioridade

Os processos são executados de acordo com seus níveis de prioridade.

---

# 🧠 Gerenciamento de Memória

O Sistema Operacional precisa controlar e organizar a utilização da memória.

## 💾 Memória Principal

Principais recursos:

* Alocação dinâmica
* Proteção de memória

## 🗃️ Memória Virtual

Permite uma **expansão lógica da RAM**.

### Técnicas

* Paginação
* Segmentação

### Benefícios

* Maior segurança
* Maior flexibilidade

---

# 🔌 Dispositivos, Arquivos e Segurança

## 🖱️ Gerenciamento de E/S

Responsável pelo controle do **hardware periférico**.

## 📁 Sistemas de Arquivos

Responsáveis pela:

* Organização dos dados.
* Acesso aos dados.

## 🛡️ Segurança

Responsável pela proteção contra ameaças.

## ☁️ Virtualização

Permite:

* Otimização de recursos.
* Maior flexibilidade.

---

# 💼 Portfólio de Projetos

A aula destaca a importância de possuir um **portfólio de projetos**.

### O portfólio permite:

* Demonstrar habilidades práticas.
* Demonstrar criatividade.
* Demonstrar domínio de ferramentas.
* Servir como evidência do aprendizado.
* Facilitar a avaliação pelo professor.
* Ampliar oportunidades de estágio e emprego.
* Incentivar organização.
* Promover melhoria contínua.
* Desenvolver soluções reais.
* Preparar para desafios do mercado profissional.

---

# 📊 Critérios de Avaliação

A fórmula apresentada no slide é:

```text
(P1 × 0,25) + (P2 × 0,25) + ((PJ + AT) × 0,25)
```

### 📌 Onde:

* **P1** → Prova 1
* **P2** → Prova 2
* **PJ** → Projeto
* **AT** → Atividades

---

# 👥 Atividade

## Formação dos grupos

* Grupos de **3 a 5 integrantes**.
* Todas as atividades semanais deverão ser realizadas em grupo.
* A composição do grupo deve permanecer a mesma.

## 📂 Repositório

Após formar o grupo:

1. Criar um repositório no **GitHub**.
2. O repositório será o diretório principal das atividades durante o semestre.
3. Criar um arquivo **Markdown (`.md`)**.
4. Colocar nele o resumo da Aula 01.
5. Criar uma linha do tempo dos Sistemas Operacionais.
6. Realizar a linha do tempo colaborativamente no **Miro**.
7. Transformar o conteúdo em `.md` e salvar no repositório.

---

# 📅 Linha do Tempo dos Sistemas Operacionais

> **Importante:** o slide da Aula 01 solicita uma linha do tempo demonstrando os anos em que os sistemas operacionais foram lançados, mas **não apresenta no próprio material uma lista desses anos**. Portanto, os anos abaixo não fazem parte do conteúdo fornecido no slide e devem ser adicionados a partir da pesquisa solicitada na atividade.

```text
📅 LINHA DO TEMPO

1956 ──► GM-NAA I/O
          │
          ▼
1961 ──► CTSS
          │
          ▼
1964 ──► OS/360
          │
          ▼
1969 ──► UNIX
          │
          ▼
1974 ──► CP/M
          │
          ▼
1981 ──► MS-DOS
          │
          ▼
1984 ──► Macintosh System Software
          │
          ▼
1985 ──► Windows 1.0
          │
          ▼
1987 ──► OS/2
          │
          ▼
1991 ──► Linux
          │
          ▼
1993 ──► Windows NT
          │
          ▼
1995 ──► Windows 95
          │
          ▼
2001 ──► Mac OS X
          │
          ▼
2001 ──► Windows XP
          │
          ▼
2007 ──► iPhone OS
          │
          ▼
2008 ──► Android
          │
          ▼
2015 ──► Windows 10
          │
          ▼
2021 ──► Windows 11
```

---

# 📌 Conclusão

A Aula 01 apresentou:

* A disciplina e seu plano de ensino.
* O contexto dos Sistemas Operacionais.
* A estrutura interna dos SOs.
* O funcionamento do kernel.
* Os modos de operação.
* O escalonamento de processos.
* O gerenciamento de memória.
* O gerenciamento de dispositivos.
* Os sistemas de arquivos.
* Segurança.
* Virtualização.
* Critérios de avaliação.
* Atividades da disciplina.
* Criação de um repositório GitHub.
* Elaboração de uma linha do tempo dos Sistemas Operacionais.

---

# 📚 Referências

* TANENBAUM, Andrew S.; BOS, Herbert. *Sistemas Operacionais Modernos*. 4. ed. São Paulo: Pearson, 2016.
* SILBERSCHATZ, Abraham; GALVIN, Peter B.; GAGNE, Greg. *Fundamentos de Sistemas Operacionais*. 9. ed. Rio de Janeiro: LTC, 2015.
* STALLINGS, William. *Sistemas Operacionais: Conceitos e Projetos*. 8. ed. São Paulo: Pearson, 2015.
* DENARDIN, G. W.; BARRIQUELLO, C. H. *Sistemas Operacionais de Tempo Real e sua Aplicação em Sistemas Embarcados*. Porto Alegre: Editora da UFRGS, 2014.
* AWASTHI, A.; RAWAT, V. *Ramificação e Tarefas do Sistema Operacional*. Edições Nosso Conhecimento, 2023.
* DOWNEY, Allen B. *Think OS: A Brief Introduction to Operating Systems*. Green Tea Press, 2015.
* Red Hat. *Red Hat Enterprise Linux – System Administration Guide*.
* Docker Inc. *Docker Documentation*.
