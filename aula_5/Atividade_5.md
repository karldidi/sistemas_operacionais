# Aula 05 — Virtualização

## Atividade 1 — Instalar VirtualBox e criar VM Linux
1. Baixar VirtualBox: https://www.virtualbox.org/.
2. Baixar a ISO de uma distribuição Linux leve, como Tiny Core, Lubuntu ou Xubuntu.
3. Abrir VirtualBox e clicar em Nova.
4. Definir nome, tipo Linux e versão.
5. Reservar memória RAM (o slide recomenda 2048 MB ou mais), sem comprometer o computador hospedeiro.
6. Criar disco virtual de 20–40 GB, conforme o espaço disponível.
7. Em Armazenamento, associar a ISO ao drive óptico virtual.
8. Iniciar a VM e seguir o instalador Linux.
9. Reiniciar, remover a ISO virtual e iniciar pelo disco virtual.
10. Testar interface, rede, terminal e aplicativos.

## Atividade 2 — Manual
**Host:** sistema operacional principal do computador. **Guest:** Linux instalado na VM. **Hypervisor:** VirtualBox, que cria e gerencia o hardware virtual. **Disco virtual:** arquivo que representa o armazenamento da VM. **ISO:** imagem utilizada para iniciar a instalação.

**Registro sugerido:** incluir capturas da tela principal do VirtualBox, configurações de RAM e disco, ISO montada, instalador e Linux funcionando.

**Conclusão:** virtualização permite executar outro sistema isolado sem substituir o sistema principal. É útil para testes, estudos e recuperação por snapshots.
