# 🖥️ Aula 01 — Introdução aos Sistemas Operacionais

## 🧠 Mapa Mental

```text
                         SISTEMAS OPERACIONAIS
                                  │
        ┌─────────────────────────┼─────────────────────────┐
        │                         │                         │
    CONCEITO                 ESTRUTURA                  PROCESSOS
        │                         │                         │
        ├─ Software essencial    ├─ Camadas               ├─ Escalonamento
        ├─ Gerencia hardware     ├─ Monolítico            ├─ Eficiência
        │  e software            ├─ Modular               ├─ Justiça
        └─ Interface usuário     └─ Kernel                └─ Tempo de resposta
           ↕ máquina                 │
                                     ├─ Núcleo do SO
                                     ├─ Acesso ao hardware
                                     └─ Gerencia recursos

        ┌─────────────────────────┼─────────────────────────┐
        │                         │                         │
     MEMÓRIA                 DISPOSITIVOS               SEGURANÇA
        │                    E ARQUIVOS                     │
        │                         │                         ├─ Proteção
        ├─ Memória principal     ├─ Gerenciamento de E/S   │  contra ameaças
        ├─ Alocação dinâmica     ├─ Sistemas de arquivos  │
        ├─ Proteção              └─ Organização e acesso  └─ Virtualização
        │                           aos dados                  │
        └─ Memória virtual                                  └─ Otimização
           ├─ Paginação
           ├─ Segmentação
           └─ Expansão lógica da RAM

                         MODOS DE OPERAÇÃO
                                  │
                    ┌─────────────┴─────────────┐
                    │                           │
              MODO USUÁRIO                 MODO KERNEL
                    │                           │
              Programas comuns          Privilégios elevados
                                        Acesso total
```

---

# 📅 Linha do Tempo dos Sistemas Operacionais

A evolução dos sistemas operacionais passou por diferentes gerações, desde os primeiros sistemas para **mainframes** até os sistemas modernos para computadores pessoais e dispositivos móveis.

```text
1956
 │
 ▼
GM-NAA I/O
Primeiros sistemas operacionais para mainframes
 │
 ▼
1961
 │
 ▼
CTSS
Sistema de tempo compartilhado
 │
 ▼
1964
 │
 ▼
OS/360
Sistema operacional desenvolvido pela IBM
 │
 ▼
1969
 │
 ▼
UNIX
Sistema multiusuário e multitarefa desenvolvido
nos Bell Labs
 │
 ▼
1974
 │
 ▼
CP/M
Sistema operacional voltado para microcomputadores
 │
 ▼
1981
 │
 ▼
MS-DOS
Sistema operacional utilizado nos primeiros
computadores pessoais IBM PC
 │
 ▼
1984
 │
 ▼
Macintosh System Software
Sistema da Apple com interface gráfica
 │
 ▼
1985
 │
 ▼
Windows 1.0
Primeira versão do Microsoft Windows
 │
 ▼
1987
 │
 ▼
OS/2
Desenvolvido pela IBM e Microsoft
 │
 ▼
1991
 │
 ▼
Linux
Kernel criado por Linus Torvalds
 │
 ▼
1993
 │
 ▼
Windows NT
Nova linha de sistemas da Microsoft
 │
 ▼
1995
 │
 ▼
Windows 95
Popularização do Windows nos computadores pessoais
 │
 ▼
2001
 │
 ▼
Mac OS X
Nova geração do sistema operacional da Apple
 │
 ▼
2001
 │
 ▼
Windows XP
Uma das versões mais populares do Windows
 │
 ▼
2007
 │
 ▼
iPhone OS (atual iOS)
Sistema operacional móvel da Apple
 │
 ▼
2008
 │
 ▼
Android
Sistema operacional móvel baseado no kernel Linux
 │
 ▼
2015
 │
 ▼
Windows 10
Sistema operacional da Microsoft
 │
 ▼
2021
 │
 ▼
Windows 11
Atualização da linha principal do Windows
```

## 📊 Tabela da Linha do Tempo

|      Ano | Sistema Operacional           | Principal característica                               |
| -------: | ----------------------------- | ------------------------------------------------------ |
| **1956** | **GM-NAA I/O**                | Um dos primeiros sistemas operacionais para mainframes |
| **1961** | **CTSS**                      | Introduziu o conceito de tempo compartilhado           |
| **1964** | **OS/360**                    | Sistema operacional para mainframes da IBM             |
| **1969** | **UNIX**                      | Sistema multiusuário e multitarefa                     |
| **1974** | **CP/M**                      | Sistema para microcomputadores                         |
| **1981** | **MS-DOS**                    | Sistema utilizado no IBM PC                            |
| **1984** | **Macintosh System Software** | Interface gráfica da Apple                             |
| **1985** | **Windows 1.0**               | Primeira versão do Windows                             |
| **1987** | **OS/2**                      | Projeto IBM/Microsoft                                  |
| **1991** | **Linux**                     | Kernel criado por Linus Torvalds                       |
| **1993** | **Windows NT**                | Nova arquitetura do Windows                            |
| **1995** | **Windows 95**                | Grande popularização do Windows                        |
| **2001** | **Mac OS X**                  | Nova geração do sistema da Apple                       |
| **2001** | **Windows XP**                | Uma das versões mais populares da Microsoft            |
| **2007** | **iPhone OS / iOS**           | Sistema operacional móvel da Apple                     |
| **2008** | **Android**                   | Sistema móvel baseado em Linux                         |
| **2015** | **Windows 10**                | Nova geração do Windows                                |
| **2021** | **Windows 11**                | Evolução do Windows 10                                 |

A seleção acima resume os principais marcos; existem muitos outros sistemas operacionais na história.

---

# ⚙️ Principais Conceitos da Aula

## O que são Sistemas Operacionais?

Um **Sistema Operacional (SO)** é um software essencial que:

* Gerencia o **hardware**.
* Gerencia o **software**.
* Faz a interface entre o **usuário e a máquina**.

### Exemplos

* Windows
* macOS
* Linux
* Android
* iOS

---

## 🧩 Estrutura Interna

### Estrutura em Camadas

Organização hierárquica utilizada para facilitar a **modularidade** do sistema.

### Monolítica e Modular

São diferentes formas de organizar e desenvolver o **kernel**.

### Kernel

É o **núcleo do Sistema Operacional**.

Responsável por:

* Acesso ao hardware.
* Gerenciamento dos recursos.
* Funções essenciais do sistema.

---

# 🔐 Modos de Operação

## Modo Usuário

* Executa programas comuns.
* Possui acesso limitado aos recursos do sistema.

## Modo Kernel

* Possui privilégios elevados.
* Possui acesso total aos recursos do sistema.

---

# 🔄 Escalonamento de Processos

O Sistema Operacional decide:

> **Qual processo será executado e por quanto tempo.**

### Objetivos

* Eficiência
* Justiça
* Tempo de resposta
* Melhor desempenho

### Algoritmos

* **FIFO**
* **Round Robin**
* **Prioridade**

---

# 🧠 Gerenciamento de Memória

## Memória Principal

* Alocação dinâmica
* Proteção de memória

## Memória Virtual

* Expansão lógica da RAM
* Paginação
* Segmentação
* Maior segurança
* Maior flexibilidade

---

# 🔌 Dispositivos, Arquivos e Segurança

## Gerenciamento de E/S

Controle dos dispositivos e periféricos de hardware.

## Sistemas de Arquivos

Responsáveis pela:

* Organização dos dados.
* Acesso aos dados.

## Segurança

Proteção do sistema contra ameaças.

## Virtualização

Permite:

* Melhor utilização dos recursos.
* Maior flexibilidade.

---

# 📚 Atividade da Aula

1. Formar grupos de **3 a 5 integrantes**.
2. Manter a mesma composição nas atividades semanais.
3. Criar um repositório no **GitHub**.
4. Criar um arquivo **Markdown (`.md`)** com o resumo da Aula 01.
5. Criar uma **linha do tempo em formato de mapa mental** mostrando os anos de lançamento dos sistemas operacionais.
6. Desenvolver a atividade colaborativamente no **Miro**.
7. Transformar o conteúdo em `.md` para salvar no repositório.

---

# 📊 Critérios de Avaliação

A fórmula apresentada na aula é:

```text
(P1 × 0,25) + (P2 × 0,25) + ((PJ + AT) × 0,25)
```

### Significado:

* **P1** → Prova 1
* **P2** → Prova 2
* **PJ** → Projeto
* **AT** → Atividades

---

# 💼 Portfólio

A aula destaca a importância de possuir um **portfólio de projetos**.

Ele permite:

* Demonstrar habilidades práticas.
* Demonstrar criatividade.
* Comprovar o domínio de ferramentas.
* Evidenciar o aprendizado.
* Facilitar oportunidades de estágio e emprego.
* Incentivar organização e melhoria contínua.
* Preparar o aluno para desafios profissionais.

---

# 📝 Conclusão

Os Sistemas Operacionais são fundamentais para o funcionamento dos computadores e dispositivos modernos. Eles fazem o gerenciamento dos recursos de hardware e software e permitem a interação entre o usuário e a máquina.

Na Aula 01 foram apresentados conceitos fundamentais como **kernel, processos, escalonamento, memória, sistemas de arquivos, segurança, virtualização e modos de operação**.

Também foi apresentada a atividade de criação de um **repositório GitHub**, um resumo em Markdown e uma **linha do tempo dos Sistemas Operacionais**.

---

# 📖 Referências

* TANENBAUM, Andrew S.; BOS, Herbert. *Sistemas Operacionais Modernos*. 4. ed. São Paulo: Pearson, 2016.
* SILBERSCHATZ, Abraham; GALVIN, Peter B.; GAGNE, Greg. *Fundamentos de Sistemas Operacionais*. 9. ed. Rio de Janeiro: LTC, 2015.
* STALLINGS, William. *Sistemas Operacionais: Conceitos e Projetos*. 8. ed. São Paulo: Pearson, 2015.
* DENARDIN, G. W.; BARRIQUELLO, C. H. *Sistemas Operacionais de Tempo Real e sua Aplicação em Sistemas Embarcados*. Porto Alegre: Editora da UFRGS, 2014.
* DOWNEY, Allen B. *Think OS: A Brief Introduction to Operating Systems*. Green Tea Press, 2015.
* Red Hat. *Red Hat Enterprise Linux – System Administration Guide*.
* Docker Inc. *Docker Documentation*.
