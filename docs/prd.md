# Product Requirements Document (PRD) — My MatchMates

## 1. Identificação
* **Autor:** [Seu Nome Completo]
* **Curso:** Tecnologia em Sistemas para Internet — UTFPR
* **Nome do Projeto:** My MatchMates

## 2. Descrição do Projeto
O **My MatchMates** é uma aplicação web responsiva projetada para conectar jogadores que buscam parceiros (Duos) ou formações de times para partidas competitivas de eSports. A aplicação resolve a dor de jogar com parceiros aleatórios sem comunicação, permitindo a publicação e filtragem de anúncios. O escopo inicial é focado no ecossistema do jogo Valorant, com arquitetura preparada para suportar outros títulos no futuro.

## 3. Atores do Sistema
* **Visitante:** Usuário que navega pela plataforma, visualiza cards de anúncios e aplica filtros por Elo ou Agente.
* **Anunciante (Jogador):** Usuário que cadastra seu perfil com dados de contato (Discord/Riot ID) e preferências de jogo para encontrar um duo.

## 4. Histórias de Usuário (User Stories)
* **US01:** Como Visitante, quero visualizar os anúncios de jogadores em cards interativos para encontrar um parceiro compatível.
* **US02:** Como Visitante, quero filtrar anúncios por Elo (Patente) e Agente para selecionar apenas parceiros com nível competitivo alinhado.
* **US03:** Como Anunciante, quero cadastrar meu anúncio preenchendo Nick, Tag, Discord, Elo, Agente Principal e Horário para ser encontrado por outros jogadores.
* **US04:** Como Anunciante, quero selecionar meu Agente e Elo via menus alimentados por imagens oficiais obtidas da API do jogo.
* **US05:** Como Visitante, quero clicar no card para abrir um Modal com as informações de contato do Discord.
* **US06:** Como Anunciante, quero poder remover meu anúncio da plataforma assim que encontrar uma dupla.