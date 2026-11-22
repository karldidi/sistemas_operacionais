# Resumo das aulas --- Sistemas Operacionais

Resumo organizado por aula e por slide, seguindo a sequência dos
arquivos enviados.

------------------------------------------------------------------------

# Aula 02 --- Evolução Histórica dos Sistemas Operacionais

1.  **Capa:** Apresenta o tema da aula.
2.  **Sumário:** Introduz as gerações dos sistemas operacionais e as
    atividades.
3.  **Introdução:** O sistema operacional intermedeia usuário e hardware
    e simplifica o uso dos computadores.
4.  **Método de estudos por livros:** Slide visual sobre o uso de livros
    como apoio ao estudo.
5.  **Primeira geração (1945--1955):** Computadores utilizavam válvulas,
    eram grandes, caros, consumiam muita energia e falhavam com
    frequência.
6.  **Programação na primeira geração:** Era feita em código de máquina
    específico para o hardware; às vezes exigia alterar conexões físicas
    ou painéis.
7.  **Imagem da primeira geração:** Ilustração dos computadores desse
    período.
8.  **Segunda geração (1955--1965):** Transistores substituíram
    válvulas, tornando os computadores menores, mais rápidos e
    confiáveis.
9.  **Sistemas em lote (Batch):** Programas eram preparados
    antecipadamente e executados em sequência, sem interação direta do
    usuário; utilizavam cartões perfurados.
10. **Imagem da segunda geração:** Ilustração dos computadores desse
    período.
11. **Terceira geração (1965--1980):** Circuitos integrados permitiram
    computadores mais compactos e potentes. A multiprogramação mantinha
    vários programas na memória e aproveitava a CPU enquanto outro
    aguardava E/S.
12. **Compartilhamento de tempo e spooling:** Vários usuários utilizavam
    o sistema por terminais; o spooling armazenava dados de entrada e
    saída em disco.
13. **Imagem da terceira geração:** Ilustração dos computadores desse
    período.
14. **Quarta geração (1980--presente):** Popularização dos computadores
    pessoais e das interfaces gráficas, mais simples que comandos
    textuais.
15. **UNIX e sistemas atuais:** UNIX influenciou Linux, macOS e Android.
    Sistemas operacionais atuais estão em PCs, servidores e smartphones.
16. **Imagem da quarta geração:** Ilustração dos computadores pessoais.
17. **Quinta geração (1990--presente):** Aborda a evolução dos
    smartphones, que combinaram telefone e funções de PDA; o material
    cita Nokia N9000 e Ericsson.
18. **Imagem da quinta geração:** Ilustração sobre dispositivos móveis.
19. **Sexta geração:** Propõe refletir sobre possíveis características
    de uma próxima geração de sistemas operacionais.
20. **Atividade:** Introduz o trabalho relacionado ao conteúdo
    histórico.
21. **Estudo de caso --- OpenClaw:** Apresenta o OpenClaw como tema para
    estudo de caso.
22. **Atividade --- resumo histórico:** Solicita um arquivo Markdown com
    mais de 500 linhas sobre o capítulo de história dos sistemas
    operacionais de Tanenbaum.
23. **Atividade --- linha do tempo:** Solicita ampliar a linha do tempo
    por gerações, detalhar características e exportar o resultado do
    Miro para o GitHub.
24. **Referências:** Lista livros e documentações usados como fontes.
25. **Encerramento:** Retoma o título da aula e identifica o professor.

------------------------------------------------------------------------

# Aula 03 --- Conceitos, Funções e Tipos de Sistemas Operacionais

1.  **Capa:** Apresenta o tema da aula.
2.  **Sumário:** Tipos de SO, Git, boas práticas de versionamento, IDE e
    atividade.
3.  **Mainframes:** Sistemas de grande porte voltados a muitas
    transações e operações de E/S; priorizam confiabilidade,
    disponibilidade e segurança.
4.  **Mainframes --- exemplos e usos:** Cita OS/360, OS/390, Linux em
    mainframes e variantes UNIX; são usados em bancos, e-commerce e
    serviços de grande escala.
5.  **Sistemas de servidor:** Atendem múltiplos usuários e serviços de
    rede, como web, arquivos, bancos de dados e autenticação.
6.  **Multiprocessadores:** Utilizam várias CPUs ou núcleos e exigem
    escalonamento, sincronização e coerência de cache.
7.  **Computadores pessoais:** SOs voltados ao uso individual, com
    interface gráfica e compatibilidade com aplicações; exemplos:
    Windows, macOS e Linux.
8.  **Sistemas portáteis:** Android e iOS priorizam energia, sensores,
    permissões, segurança e integração com hardware.
9.  **Sistemas embarcados:** Executam em dispositivos dedicados, como
    micro-ondas, TVs e automóveis; podem ter recursos limitados e
    exigências de resposta.
10. **Nós sensores:** Dispositivos pequenos, sem fio e com bateria
    limitada; priorizam baixo consumo. Exemplos: TinyOS e Contiki.
11. **Tempo real:** Hard real-time não pode perder prazos sem
    consequências graves; soft real-time tolera atrasos com degradação
    do serviço.
12. **Cartões inteligentes:** Possuem recursos restritos e exigem
    gerenciamento de memória, criptografia, autenticação e isolamento.
13. **Introdução ao Git:** Sistema de controle de versão que registra
    alterações, permite restaurar versões e sincronizar projetos.
14. **Instalação do Git --- imagem:** Apresenta visualmente a página de
    download.
15. **Instalação do Git --- etapas:** Baixar o instalador adequado e
    verificar com `git --version`.
16. **Configuração Git/VS Code:** Configurar nome e e-mail com
    `git config --global` e integrar o Git ao controle de código-fonte
    do VS Code.
17. **Criar repositório no VS Code:** Criar pasta e arquivo Markdown,
    inicializar o repositório e registrar um commit.
18. **Publicar no GitHub:** Publicar a branch, autenticar-se e escolher
    repositório público ou privado.
19. **Boas práticas Git:** Fazer commits pequenos e frequentes, usar
    mensagens claras e branches e testar antes do merge.
20. **Atividade --- integração:** Configurar IDE, Git e GitHub e validar
    commit, push e pull.
21. **Atividade --- clone:** Criar repositório, alterar e enviar
    arquivos, apagar a pasta local e recuperar com `git clone`.
22. **Atividade --- projetos:** Clonar cinco projetos do GitHub e
    analisar seus conteúdos.
23. **Referências:** Lista fontes bibliográficas e documentações.
24. **Encerramento:** Identifica a aula e o professor.

------------------------------------------------------------------------

# Aula 04 --- Estrutura e Arquitetura de Sistemas Operacionais

1.  **Capa:** Apresenta o tema.
2.  **Sumário:** Componentes, kernel, modos de execução, processos,
    memória, arquivos e dispositivos.
3.  **Por que precisamos de um SO?:** Sem SO, cada aplicação teria de
    controlar hardware, memória, CPU, arquivos e segurança. O SO abstrai
    esses recursos.
4.  **Componentes do SO:** Kernel, gerenciamento de processos e memória,
    sistema de arquivos, entrada/saída e drivers.
5.  **Camadas do sistema:** O hardware fica na base, o SO gerencia
    recursos e as aplicações interagem com essa camada.
6.  **Kernel:** Núcleo que gerencia processos, threads, memória,
    dispositivos, comunicação e segurança.
7.  **Modos de execução:** Aplicações operam em modo usuário; chamadas
    de sistema solicitam serviços ao kernel, executado em modo
    privilegiado.
8.  **Processos:** Um processo é um programa em execução, com memória e
    recursos próprios, como código, dados, pilha, registradores e
    arquivos.
9.  **Programa, processo e thread:** Programa é arquivo armazenado;
    processo é programa em execução; thread é um fluxo de execução
    dentro do processo.
10. **Revisão:** Slide de atividade para revisar os conceitos.
11. **Sistema de arquivos:** Organiza dados em diretórios hierárquicos
    para facilitar localização e gerenciamento.
12. **Entrada/saída e drivers:** O SO controla teclado, mouse, disco,
    rede e impressora; drivers fazem a comunicação com o hardware.
13. **Atividade 1 --- instalação:** Descrever as etapas de formatação e
    instalação de um sistema operacional conforme o roteiro.
14. **Atividade 1 --- Markdown:** Registrar o processo em sequência,
    explicando o que ocorre e quais componentes do SO participam.
15. **Reaproveitamento:** Dispositivos frequentemente adaptam sistemas
    existentes, reduzindo custos e aproveitando estabilidade, segurança
    e atualizações.
16. **Raspberry Pi:** O Raspberry Pi OS é apresentado como adaptação do
    Debian Linux.
17. **PlayStation 4:** O Orbis OS é apresentado como baseado no FreeBSD.
18. **Atividade 2 --- pesquisa:** Identificar cinco SOs desenvolvidos a
    partir de outro sistema ou que reutilizam sua base.
19. **Atividade 2 --- comparação:** Criar tabela comparativa entre os
    sistemas e suas bases e salvar em Markdown.
20. **Referências e encerramento:** Lista fontes e encerra a aula.

------------------------------------------------------------------------

# Aula 05 --- Introdução à Virtualização

1.  **Capa:** Apresenta o tema.
2.  **Sumário:** Virtualização, vantagens, máquinas virtuais,
    VirtualBox, criação de VM e atividade.
3.  **Definição:** Virtualização permite executar vários SOs em um
    computador físico, em ambientes isolados que simulam hardware.
4.  **Vantagens:** Economia de hardware, isolamento, testes seguros,
    snapshots e execução simultânea de diferentes sistemas.
5.  **Slide visual:** Material ilustrativo sobre virtualização.
6.  **Hypervisor:** Camada que cria e gerencia VMs, distribui CPU e
    memória, administra dispositivos virtuais e isola máquinas.
7.  **Máquina virtual:** Host é o SO principal; a virtualização simula
    hardware; guest é o SO executado dentro da VM.
8.  **Oracle VirtualBox:** Ferramenta de virtualização da Oracle,
    gratuita para uso pessoal e educacional e multiplataforma.
9.  **Interface do VirtualBox:** Mostra lista de VMs, configurações de
    CPU/memória, armazenamento, ISOs e rede.
10. **Tiny Core Linux:** Apresentado como exemplo de sistema operacional
    para virtualização.
11. **Slide visual:** Material ilustrativo relacionado ao exemplo de SO.
12. **Criar uma VM:** Clicar em Nova, selecionar tipo e versão do SO,
    definir RAM e criar disco virtual.
13. **Instalar um SO:** Obter ISO, montá-la na VM, iniciar a máquina e
    seguir o instalador.
14. **Slide visual:** Apoio visual ao processo de virtualização.
15. **Slide visual:** Continuação do material ilustrativo.
16. **Tiny Core Linux --- características:** Distribuição Linux leve,
    modular e personalizável, indicada para testes e baixo consumo de
    recursos.
17. **Apresentação --- orientações:** Grupos devem apresentar um SO
    virtualizado, suas características, história, ferramentas, usos,
    vantagens e limitações.
18. **Apresentação --- horários:** Define horários dos grupos e solicita
    participação de todos os integrantes.
19. **Apresentação --- slide visual:** Material de apoio às
    apresentações.
20. **Atividade:** Instalar VirtualBox, criar VM, instalar Linux leve,
    testar e documentar o processo em manual.
21. **Referências e encerramento:** Lista fontes e encerra a aula.

------------------------------------------------------------------------

# Aula 06 --- Nuvem e Sistemas Operacionais

1.  **Capa:** Apresenta o tema.
2.  **Sumário:** Cloud computing, virtualização, modelos de serviço,
    provedores, segurança, containers, backend e deploy.
3.  **Conceito de cloud:** Recursos computacionais são acessados sob
    demanda pela rede, compartilhados e medidos.
4.  **Características NIST:** Autoatendimento, amplo acesso à rede, pool
    de recursos, elasticidade e serviço mensurável.
5.  **Infraestrutura tradicional e cloud:** A nuvem reduz a necessidade
    de comprar hardware (CAPEX) e permite pagar pelo consumo (OPEX).
6.  **Virtualização:** Permite criar várias VMs em um servidor físico; o
    hypervisor abstrai os recursos de hardware.
7.  **Camadas da virtualização:** Hardware físico, hypervisor e máquinas
    virtuais com SOs e aplicações independentes.
8.  **Recursos sob demanda:** O usuário provisiona recursos sem
    intervenção manual; elasticidade aumenta ou reduz capacidade
    conforme a demanda.
9.  **Alta disponibilidade:** Zonas de disponibilidade, balanceamento de
    carga, replicação e failover ajudam a manter serviços ativos.
10. **IaaS:** Provedor oferece infraestrutura virtualizada; cliente
    administra SO e aplicações. Exemplos: AWS EC2, Google Compute Engine
    e Azure VMs.
11. **PaaS:** Provedor gerencia infraestrutura e plataforma;
    desenvolvedor foca no código. Exemplos: App Engine, Azure App
    Service, Heroku e Elastic Beanstalk.
12. **SaaS:** Software pronto é acessado pela internet e gerenciado pelo
    provedor. Exemplos: Google Workspace, Microsoft 365, Salesforce,
    Slack e Zoom.
13. **Provedores:** Apresenta AWS, Azure, Google Cloud, Oracle Cloud,
    IBM Cloud, Alibaba Cloud e provedores regionais.
14. **Modelos de implantação:** Nuvem pública é compartilhada; privada é
    dedicada; híbrida combina ambientes públicos e privados.
15. **Vantagens e desafios:** Vantagens: menor investimento inicial,
    escalabilidade e disponibilidade. Desafios: dependência de
    fornecedor, segurança, custos, latência e complexidade.
16. **Segurança:** Provedor protege a infraestrutura; cliente protege
    dados, acessos e configurações. São importantes criptografia,
    controle de acesso e monitoramento.
17. **Containers e microsserviços:** Containers empacotam aplicações e
    dependências; Docker cria e distribui containers e Kubernetes os
    orquestra. Microsserviços dividem aplicações em serviços
    independentes.
18. **Backend e Web Service:** Backend processa requisições, executa
    regras de negócio e acessa dados. Web services permitem comunicação
    entre sistemas via web.
19. **API REST com Express:** Criar projeto, instalar Express e CORS,
    desenvolver API e iniciar com Node.js. CORS controla acesso entre
    domínios no navegador.
20. **Render:** Plataforma de hospedagem em nuvem que suporta Node.js e
    outras linguagens e integra-se com Git.
21. **Render --- imagem:** Slide visual da plataforma.
22. **Benefícios do Render:** Deploy simples, integração GitHub,
    atualização automática, escalabilidade e monitoramento.
23. **Deploy no Render:** Enviar projeto ao GitHub, criar serviço web,
    conectar repositório, configurar inicialização e publicar.
24. **Atividade 1 --- aplicação:** Criar API Express que exiba hostname,
    plataforma, arquitetura, CPUs, memória e uptime; testar localmente.
25. **Atividade 2 --- cloud:** Publicar no GitHub e Render e comparar
    dados da máquina local com o ambiente em nuvem.
26. **Atividade 3 --- conceitos:** Relacionar a aplicação a processos,
    memória, CPU, SO hospedeiro, virtualização e cloud.
27. **Atividade 4 --- manual:** Documentar instalação, desenvolvimento,
    deploy, testes, comparação e conclusões.
28. **Referências e encerramento:** Lista fontes e encerra a aula.

------------------------------------------------------------------------

# Aula 07 --- Projeto: Nuvem e Sistemas Operacionais

1.  **Capa:** Apresenta o projeto prático.
2.  **API REST com Express:** Criar projeto, instalar Express e CORS,
    preparar o arquivo da API e executar com Node.js.
3.  **Render como Web Service:** Apresenta hospedagem em nuvem com
    suporte a Node.js, integração Git e deploy contínuo.
4.  **Render --- imagem:** Slide visual da plataforma.
5.  **Benefícios do Render:** Deploy simplificado, integração GitHub,
    escalabilidade, monitoramento e infraestrutura para projetos.
6.  **Deploy da API:** Enviar projeto ao GitHub, conectar o repositório
    no Render, configurar o comando de início e publicar.
7.  **Evolução para dashboard:** Ampliar a aplicação anterior, que
    mostrava dados básicos da máquina, para um painel de monitoramento.
8.  **Slide visual do projeto:** Apoio visual à proposta de dashboard.
9.  **Indicadores:** Mostrar uso de RAM, uso médio de CPU, uptime,
    quantidade de arquivos, IP principal e status da máquina.
10. **Dados do sistema operacional:** Exibir hostname, tipo de sistema,
    versão do kernel, arquitetura, endianness e versão do Node.js.
11. **Local ou cloud:** Identificar se a aplicação roda localmente ou em
    nuvem e mostrar variáveis de ambiente, porta e modo de execução.
12. **Comparação de plataformas:** Publicar a aplicação em serviço
    semelhante ao Render e elaborar relatório comparativo.
13. **Referências:** Lista fontes bibliográficas e documentações.
14. **Encerramento:** Retoma o título do projeto e identifica o
    professor.

------------------------------------------------------------------------

# Aula 08 --- Documentação de Software

1.  **Capa:** Apresenta o tema.
2.  **Sumário:** Definição, áreas relacionadas, tipos de documentação,
    README, DevOps e atividade.
3.  **Pergunta inicial:** Verifica se alguém conseguiria entender e
    executar o projeto apenas pelo GitHub.
4.  **Sem documentação:** Gera dependência de pessoas, dificulta
    integração de novos membros, provoca configurações inconsistentes e
    aumenta o tempo de manutenção.
5.  **Definição:** Documentação reúne informações para compreender,
    utilizar, desenvolver, testar e manter um sistema.
6.  **Por que documentar?:** Apoia comunicação, manutenção, colaboração
    e continuidade do conhecimento.
7.  **Projetos bem documentados:** Cita repositórios como Linux, React,
    Node.js, Docker Docs, Bitcoin e GitHub Brasil.
8.  **Quem utiliza?:** Desenvolvedores, testadores, DevOps, gestores e
    usuários consultam a documentação para suas tarefas.
9.  **Combinação de áreas:** Reúne Engenharia de Software, Gestão de
    Projetos, DevOps, Segurança, Qualidade e Produto/UX.
10. **Tipos de documentação:** Técnica descreve arquitetura e
    componentes; projeto registra objetivos e requisitos; processo
    descreve branches, commits, testes, pipeline e deploy.
11. **README:** Primeiro documento geralmente consultado no repositório;
    apresenta propósito, tecnologias, pré-requisitos, instalação,
    execução, testes e contribuição.
12. **Tecnologias e pré-requisitos:** Informar linguagens e versões,
    frameworks, banco de dados, gerenciador de pacotes, Docker e
    ferramentas necessárias.
13. **Instalação e execução:** Registrar sequência reproduzível: clonar,
    acessar pasta, instalar dependências, configurar variáveis, iniciar
    e testar.
14. **Configuração e variáveis:** Explicar finalidade e obrigatoriedade
    das variáveis sem expor credenciais reais.
15. **Execução e testes:** Incluir comandos para iniciar aplicação e
    executar testes unitários, de integração e desempenho, quando
    houver.
16. **Estrutura do projeto:** Explicar pastas importantes, como `src/`,
    `tests/`, `docs/` e `.github/workflows/`.
17. **DevOps --- desenvolvimento:** Documentar implementação, Git,
    commits, Pull Requests e build.
18. **DevOps --- entrega:** Documentar testes, pipeline CI/CD e deploy.
19. **Tecnologias utilizadas:** Registrar stack, versões, ferramentas e
    pré-requisitos para reproduzir o ambiente.
20. **Instalação e execução:** Explicar dependências, variáveis,
    serviços externos, inicialização e validação.
21. **O que não documentar:** Não expor senhas, credenciais, chaves de
    API, tokens ou dados pessoais e confidenciais.
22. **Arquivos e infraestrutura sigilosos:** Não publicar `.env` com
    segredos nem detalhes restritos que facilitem acessos indevidos.
23. **Atividade --- documentação:** Documentar objetivo, problema,
    escopo, requisitos funcionais e não funcionais, tecnologias e
    arquitetura de um projeto.
24. **Atividade --- README:** Criar ou atualizar README com
    pré-requisitos, instalação, configuração e execução; incluir APIs,
    banco, variáveis, testes e deploy quando aplicável.
25. **Referências:** Lista livros e documentações de apoio.
26. **Encerramento:** Retoma o título da aula e identifica o professor.

------------------------------------------------------------------------

## Revisão geral

-   **Aula 02:** História e evolução dos sistemas operacionais.
-   **Aula 03:** Tipos de sistemas operacionais e controle de versão com
    Git/GitHub.
-   **Aula 04:** Kernel, processos, memória, arquivos, drivers e
    arquitetura.
-   **Aula 05:** Virtualização, hypervisor, máquinas virtuais e
    VirtualBox.
-   **Aula 06:** Computação em nuvem, modelos de serviço, segurança,
    containers e backend.
-   **Aula 07:** Desenvolvimento e publicação de uma API/dashboard de
    monitoramento.
-   **Aula 08:** Documentação de software, README e processos DevOps.
