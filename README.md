# lg-webos1-lab

Laboratório de experimentos numa LG 47LB6500 (2014) com webOS 1.4, sem suporte do fabricante desde 2022.

## O que já sabemos
- Firmware 05.05.90, kernel Linux 3.10.19 (compilado em mar/2022), CPU ARMv7 dual-core (Cortex-A9), ~930 MB de RAM.
- Sistema de arquivos principal somente leitura (squashfs); ~4 GB livres em /media/developer.
- Modo desenvolvedor: SSH na porta 9922 com o usuário `prisoner`, em shell restrito (sem acesso à pasta de apps do sistema).
- A TV verifica certificados públicos modernos (teste com google.com: OK).
- O Netflix dá o erro NW-4-7. A API do Netflix usa uma autoridade certificadora própria de 2024 que a TV não conhece. Hipótese (não confirmada): o app antigo não é mais compatível. Ver `logs/`.

## Estrutura
- `logs/`: saídas dos comandos de inventário
- `docs/`: notas
- `apps/`: apps de teste para a TV
