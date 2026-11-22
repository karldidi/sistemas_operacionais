# Aula 04 — Estrutura e Arquitetura

## Atividade 01 — Formatação e instalação de SO
O slide menciona um roteiro específico no repositório da disciplina que não veio junto com as apresentações. Abaixo está uma sequência geral para documentar o processo:

1. Fazer backup dos arquivos importantes.
2. Conferir requisitos de hardware e compatibilidade.
3. Baixar a imagem ISO oficial do sistema.
4. Criar um pendrive inicializável.
5. Acessar BIOS/UEFI e selecionar o pendrive no boot.
6. Iniciar o instalador e selecionar idioma e teclado.
7. Selecionar disco e partições. A formatação apaga os dados da partição escolhida.
8. Copiar os arquivos do sistema para o armazenamento.
9. Criar usuário, senha, nome do computador, rede e fuso horário.
10. Instalar drivers e atualizações.
11. Reiniciar e validar rede, áudio, vídeo, armazenamento e periféricos.

**Componentes envolvidos:** bootloader inicia o kernel; kernel gerencia CPU, memória e dispositivos; drivers comunicam o SO com o hardware; sistema de arquivos organiza os dados; gerenciador de processos inicia serviços e programas; mecanismos de segurança controlam contas e permissões.

## Atividade 02 — Cinco sistemas baseados em outros
| Sistema derivado/adaptado | Base | Diferenças |
|---|---|---|
| Ubuntu | Debian GNU/Linux | Distribuição com ciclos próprios, ferramentas de configuração e foco em facilidade de uso. |
| Linux Mint | Ubuntu (e edição baseada diretamente no Debian) | Interface e ferramentas próprias, com foco em desktop simples. |
| Raspberry Pi OS | Debian GNU/Linux | Adaptado ao hardware Raspberry Pi, incluindo arquitetura ARM e ferramentas específicas. |
| Android | Kernel Linux | Acrescenta framework Android, runtime, serviços móveis e modelo de permissões para apps. |
| Orbis OS (PS4) | FreeBSD | Adaptado ao hardware do console, com serviços e recursos específicos para jogos. |

**Conclusão:** reaproveitar kernel, arquitetura ou componentes reduz esforço e aproveita tecnologias testadas. Mesmo com uma base comum, cada sistema pode ter interface, serviços e finalidade diferentes.
