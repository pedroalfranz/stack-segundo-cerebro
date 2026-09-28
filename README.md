# Stack do segundo cérebro

Um desktop Windows 11 que fica ligado como servidor de um segundo cérebro em Obsidian, e o mapa de como as
peças se conectam: o que entra (celular, Telegram, gravador, e-mail, relógio), quem transcreve e resume
(modelos locais e Claude), onde a informação mora (o vault) e para onde ela sai (Obsidian, git, backup,
notificações e um painel de parede).

**A página:** https://pedroalfranz.github.io/stack-segundo-cerebro/

Quatro visões, todas navegáveis — clicar em qualquer caixa abre o detalhe daquela peça:

- **Mapa** — fontes → coleta → processamento → vault → destinos, com a faixa de supervisão embaixo.
- **Rotinas em 24 h** — cada rotina agendada e o horário em que roda, colorida por quem faz o trabalho
  (script, modelo local, Claude).
- **Fluxos** — cada entrada seguida sozinha, estação por estação, da captura até virar nota revisada.
- **Rodando agora** — daemons, contêineres e serviços de pé na última leitura.

## Como é gerado

Um coletor em PowerShell lê o estado real da máquina (Agendador de Tarefas, processos, Docker, Ollama e os
arquivos de estado do vault), grava um JSON e uma página é montada a partir dele. Uma tarefa agendada repete
isso **de hora em hora**. A estrutura (o mapa, os fluxos, as explicações) é escrita à mão; o estado
(última execução, o que está de pé, custo, cota) vem da coleta.

## Sobre esta versão

Esta é a versão pública: saem os endereços de rede, as portas abertas, os caminhos de arquivo, a parte de
acesso remoto e a lista de pontos de atenção da máquina. A versão completa roda só na rede de casa.

Nenhum segredo, credencial ou conteúdo de nota é lido pelo coletor ou aparece aqui.
