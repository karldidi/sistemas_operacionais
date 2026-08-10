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
        │                     E ARQUIVOS                     │
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

## 💻 O que é um Sistema Operacional?

Um **Sistema Operacional (SO)** é um software essencial responsável por gerenciar o **hardware e o software** de um computador.

Ele funciona como uma **interface entre o usuário e a máquina**.

### Exemplos

* Windows
* macOS
* Linux
* Android
* iOS

---

## ⚙️ Estrutura Interna

Os sistemas operacionais podem ser organizados utilizando diferentes modelos.

### Estrutura em Camadas

* Organização hierárquica.
* Facilita a modularidade do sistema.

### Monolítico e Modular

* São diferentes abordagens para o desenvolvimento do **kernel**.

### Kernel

O **kernel** é o núcleo do sistema operacional.

Suas principais características são:

* Acesso direto ao hardware.
* Gerenciamento de recursos importantes.
* Controle das funções essenciais do sistema.

---

## 🔐 Modos de Operação

### Modo Usuário

* Utilizado por programas comuns.
* Possui limitações de acesso aos recursos do sistema.

### Modo Kernel

* Possui privilégios elevados.
* Permite acesso total aos recursos do sistema.

---

## 🔄 Escalonamento de Processos

O sistema operacional precisa decidir **qual processo será executado e por quanto tempo**.

### Objetivos

* Eficiência
* Justiça
* Tempo de resposta
* Melhor desempenho geral

### Algoritmos

* **FIFO**
* **Round Robin**
* **Prioridade**

---

## 🧠 Gerenciamento de Memória

### Memória Principal

Responsável pelo armazenamento dos dados e programas em execução.

Principais recursos:

* Alocação dinâmica
* Proteção de memória

### Memória Virtual

Permite uma **expansão lógica da RAM**.

Utiliza técnicas como:

* Paginação
* Segmentação

Também proporciona maior:

* Segurança
* Flexibilidade

---

## 🔌 Dispositivos e Sistemas de Arquivos

### Gerenciamento de E/S

Responsável pelo controle dos **dispositivos e periféricos de hardware**.

### Sistemas de Arquivos

Responsáveis pela:

* Organização dos dados.
* Acesso aos dados.

### Segurança

Busca proteger o sistema contra ameaças.

### Virtualização

Permite melhor:

* Otimização dos recursos.
* Flexibilidade.

---

# 📅 Linha do Tempo dos Sistemas Operacionais

> **Importante:** o PDF da Aula 01 solicita a criação de uma linha do tempo com os anos de lançamento dos sistemas operacionais, mas **não apresenta os anos de lançamento**. Portanto, os dados abaixo devem ser preenchidos conforme a pesquisa/atividade realizada no Miro.

```text
LINHA DO TEMPO
     │
     ▼
┌───────────────┐
│     ANO       │
│      ↓        │
│   SISTEMA     │
│ OPERACIONAL   │
└───────┬───────┘
        │
        ▼
┌───────────────┐
│     ANO       │
│      ↓        │
│   SISTEMA     │
│ OPERACIONAL   │
└───────┬───────┘
        │
        ▼
┌───────────────┐
│     ANO       │
│      ↓        │
│   SISTEMA     │
│ OPERACIONAL   │
└───────┬───────┘
        │
        ▼
┌───────────────┐
│     ANO       │
│      ↓        │
│   SISTEMA     │
│ OPERACIONAL   │
└───────┬───────┘
        │
        ▼
┌───────────────┐
│     ANO       │
│      ↓        │
│   SISTEMA     │
│ OPERACIONAL   │
└───────────────┘
```

### Tabela para organizar a linha do tempo

|  Ano | Sistema Operacional | Marco/Observação   |
| ---: | ------------------- | ------------------ |
| ____ | __________________  | __________________ |
| ____ | __________________  | __________________ |
| ____ | __________________  | __________________ |
| ____ | __________________  | __________________ |
| ____ | __________________  | __________________ |
| ____ | __________________  | __________________ |
| ____ | __________________  | __________________ |
| ____ | __________________  | __________________ |

---

# 📚 Atividade da Aula

1. Formar grupos de **3 a 5 integrantes**.
2. Manter a mesma composição nas atividades semanais.
3. Criar um repositório no **GitHub**.
4. Criar um arquivo **Markdown (`.md`)** contendo o resumo da Aula 01.
5. Criar uma **linha do tempo em formato de mapa mental** mostrando os anos de lançamento dos sistemas operacionais.
6. Desenvolver a linha do tempo colaborativamente no **Miro**.
7. Transformar o conteúdo em `.md` para salvar no repositório.

---

# 📊 Critérios de Avaliação

A fórmula apresentada na aula é:

```text
(P1 × 0,25) + (P2 × 0,25) + ((PJ + AT) × 0,25)
```

Onde:

* **P1** = Prova 1
* **P2** = Prova 2
* **PJ** = Projeto
* **AT** = Atividades

---

# 📌 Resumo

O **Sistema Operacional** é responsável por gerenciar os recursos de hardware e software e servir como interface entre o usuário e a máquina.

Os principais conceitos apresentados na Aula 01 foram:

* Sistemas Operacionais
* Kernel
* Estrutura em camadas
* Modelos monolítico e modular
* Modo usuário e modo kernel
* Escalonamento de processos
* Gerenciamento de memória
* Memória virtual
* Gerenciamento de dispositivos
* Sistemas de arquivos
* Segurança
* Virtualização

A aula também apresenta a criação de um **portfólio de projetos** como forma de demonstrar habilidades práticas, organização, aprendizado e preparação para o mercado profissional.

---

# 📖 Referências

* TANENBAUM, Andrew S.; BOS, Herbert. *Sistemas Operacionais Modernos*. 4. ed. São Paulo: Pearson, 2016.
* SILBERSCHATZ, Abraham; GALVIN, Peter B.; GAGNE, Greg. *Fundamentos de Sistemas Operacionais*. 9. ed. Rio de Janeiro: LTC, 2015.
* STALLINGS, William. *Sistemas Operacionais: Conceitos e Projetos*. 8. ed. São Paulo: Pearson, 2015.
* DENARDIN, G. W.; BARRIQUELLO, C. H. *Sistemas Operacionais de Tempo Real e sua Aplicação em Sistemas Embarcados*. Porto Alegre: Editora da UFRGS, 2014.
* DOWNEY, Allen B. *Think OS: A Brief Introduction to Operating Systems*. Green Tea Press, 2015.
* Red Hat. *Red Hat Enterprise Linux – System Administration Guide*.
* Docker Inc. *Docker Documentation*.
