# Product Requirements Document (PRD) — My MatchMates

## 1. Visão Geral e Objetivo

O **My MatchMates** é uma aplicação web responsiva de matchmaking para o jogo _Valorant_, desenvolvida como projeto prático para a disciplina de Desenvolvimento de Páginas Web da UTFPR.

**O grande diferencial:** A plataforma centraliza a busca de parceiros competitivos por meio de parâmetros táticos avançados (Elo, Sub-divisão, Funções, Pool de Agentes, Horários, Dias ativos e Comunicação). O sistema consome mídias oficiais em tempo real para apresentar os cards de jogadores com identidade visual alinhada ao jogo.

---

## 2. Atores do Sistema

- **Visitante:** Usuário não autenticado que acessa as páginas de entrada e visualiza a estrutura pública.
- **Jogador Autenticado:** Usuário cadastrado no sistema que pode configurar seu perfil tático no formulário em etapas, filtrar parceiros na aba "Explorar", ativar o status "Lobby Ativo" e utilizar o matchmaking instantâneo.
- **O Sistema (My MatchMates):** Ator invisível responsável pela validação dos formulários no cliente, integração assíncrona com a _Valorant-API_ (para mídias de agentes e elos) e persistência dos dados dos usuários na API Fake (_JSON Server_).

---

## 3. Histórias de Usuário e Escopo

Abaixo estão as funcionalidades principais do MVP (_Minimum Viable Product_):

### 🔐 Épico 1: Autenticação e Perfil do Jogador

- **US01 - Cadastro de Usuário em Etapas:** Como um **Visitante**, quero me cadastrar por meio de um formulário multi-etapas para preencher minhas credenciais de acesso, Riot ID, Elo, Funções, Agentes e Disponibilidade.
  - **Critérios de Aceitação:** O formulário deve conter validações para criação de senha segura; a seleção de Agentes e Elos deve carregar dinamicamente dados e imagens da _Valorant-API_.
- **US02 - Configuração do Perfil:** Como um **Jogador Autenticado**, quero editar minhas preferências na aba "Meu Perfil" para manter meu card de jogador atualizado para a comunidade.

### 🔍 Épico 2: Feed e Filtros Táticos (Aba Explorar)

- **US03 - Feed de Jogadores:** Como um **Jogador Autenticado**, quero navegar pela aba "Explorar" e visualizar os cards de outros jogadores contendo seus Agentes Favoritos, Patente, Funções e status de disponibilidade.
- **US04 - Filtragem Avançada:** Como um **Jogador Autenticado**, quero utilizar a barra lateral para filtrar a lista por Faixa de Elo (mínimo e máximo), Função Requerida (Duelista, Controlador, etc.) e Meio de Comunicação (Microfone, Discord Call, Chat/ping).
- **US05 - Cópia de ID:** Como um **Jogador Autenticado**, quero clicar no botão "Copiar ID" dentro do card de um jogador para copiar o Riot ID/Discord diretamente para a área de transferência.

### ⚡ Épico 3: Matchmaking Instantâneo (Aba Instant)

- **US06 - Fila Instantânea:** Como um **Jogador Autenticado**, quero acionar a busca na aba "Instant" para receber sugestões imediatas de duos, trios e equipes (_Instant Duo_, _Instant Trio_, _Instant Comp_) alinhadas ao meu perfil tático.
