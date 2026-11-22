# Aula 05 — Introdução à Virtualização

A aula apresentou o conceito de virtualização, tecnologia que permite executar diferentes sistemas operacionais em um mesmo computador físico por meio de ambientes virtuais isolados. Essa solução facilita testes, desenvolvimento e utilização de sistemas diferentes sem a necessidade de possuir vários computadores.

Entre as principais vantagens da virtualização estão a economia de equipamentos, o melhor aproveitamento dos recursos físicos, o isolamento dos ambientes e a possibilidade de criar snapshots para salvar estados e recuperar configurações. Também foi explicado o papel do hypervisor, camada responsável por criar e administrar máquinas virtuais, distribuindo recursos como memória e CPU e controlando o acesso ao hardware.

Foram definidos os conceitos de host e guest: host é o sistema principal instalado no computador físico, enquanto guest é o sistema operacional executado dentro da máquina virtual. Como ferramenta prática, foi apresentado o Oracle VirtualBox, que permite configurar máquinas virtuais, definir memória RAM, processadores, armazenamento e dispositivos de rede.

A aula utilizou o Tiny Core Linux como exemplo de distribuição leve, adequada para testes e ambientes com poucos recursos. Também foram demonstradas as etapas gerais para criar uma máquina virtual: selecionar o sistema operacional, configurar os recursos, criar um disco virtual, adicionar a imagem ISO e iniciar a instalação.

As atividades propuseram instalar o VirtualBox, criar uma máquina virtual com uma distribuição Linux leve, explorar suas funcionalidades e registrar o procedimento em um manual.
