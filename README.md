# OutGuessed

OutGuessed é um jogo multiplayer de perguntas, dicas e estratégia em tabuleiro. Em cada partida, os jogadores escolhem uma sala e um tema, usam as pistas disponíveis para encontrar a resposta e avançam pelo tabuleiro. Quanto menos dicas forem necessárias para acertar, maior poderá ser o avanço; vence quem alcançar primeiro o final do percurso.

## Visão do projeto

<img width="768" height="855" alt="laptop" src="https://github.com/user-attachments/assets/56e93feb-1733-4c5c-915f-8f7304035b80" />

O projeto prevê partidas em tempo real para até oito competidores, reunindo:

- acesso por conta ou como convidado;
- salas temáticas, decks de cartas e tabuleiros personalizados;
- jogadores humanos e bots;
- chat durante a partida;
- reconexão e sincronização do estado do jogo.

O servidor será a autoridade sobre respostas, turnos, movimentos e resultados, garantindo que todos os participantes recebam o mesmo estado da partida.

## Arquitetura

- **Frontend:** React, TypeScript, Vite e Tailwind CSS.
- **Backend:** monólito modular planejado em Go, com HTTP para autenticação e recursos e WebSocket para as partidas em tempo real.
- **Dados:** PostgreSQL para o estado permanente e histórico; Redis para sessões, presença, conexões e chat temporário.

## Repositórios

- [outguessed-front](https://github.com/Vinist021/outguessed-front) — interface e experiência do jogador.
- [outguessed-back](https://github.com/Vinist021/outguessed-back) — regras de negócio, arquitetura e futura implementação do servidor.

## Estado atual

O frontend possui uma Home responsiva que apresenta a identidade visual, salas e fluxos iniciais de acesso, ainda com dados ilustrativos e sem integração com o servidor. O backend encontra-se na fase de especificação, com regras de negócio, modelo de dados (DER), responsabilidades do Redis e etapas de implementação documentadas.
