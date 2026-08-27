# Product Requirements Document (PRD) — MyMatchMates

## 1. Visão Geral e Objetivo

O **My MatchMates** é uma aplicação web voltada para a conexão de jogadores e formação de times no cenário de eSports, com escopo inicial focado no ecossistema do jogo _Valorant_.

**O grande diferencial (Regra de Negócio Principal):** Ao contrário dos chats de jogo tradicionais ou grupos informais de redes sociais, o sistema centraliza a busca de duos e parceiros de equipe por meio de filtros precisos baseados nas habilidades e nas escolhas do jogador (Elo, Agente Principal, Função e Horários disponíveis). A plataforma utiliza mídias oficiais em tempo real para apresentar os perfis dos jogadores de forma visual, garantindo rápida identificação de compatibilidade competitiva.

---

## 2. Atores do Sistema

- **Visitante:** Usuário não cadastrado que acessa a plataforma e navega pelo mural de anúncios públicos para explorar opções de parceiros de jogo.
- **Anunciante (Jogador):** Usuário que preenche o formulário da plataforma para publicar, editar ou remover um anúncio de busca por duo/time.
- **O Sistema (My MatchMates):** Ator invisível responsável por validar os campos, consultar as mídias da API pública (_Valorant-API_) e salvar/exibir os anúncios cadastrados no banco de dados local (_JSON Server_).

---

## 3. Histórias de Usuário e Escopo

Abaixo estão as funcionalidades principais do MVP (_Minimum Viable Product_), organizadas por Épicos e escritas sob a perspectiva dos atores do sistema:

### 🎮 Épico 1: Cadastro e Gerenciamento de Anúncios

- **US01 - Publicação de Anúncio:** Como um **Anunciante**, quero preencher um formulário com meus dados de jogo (Nick, Tag, Discord, Elo, Agente Principal e Horário) para publicar meu perfil no mural de buscas.
  - **Critérios de Aceitação:** Os campos de Nick, Tag e Discord são obrigatórios; as seleções de Elo e Agente devem ser carregadas dinamicamente com as imagens e dados da _Valorant-API_.
- **US02 - Remoção de Anúncio:** Como um **Anunciante**, quero ter a opção de excluir meu anúncio publicado quando já tiver encontrado um duo para a partida.
  - **Critérios de Aceitação:** O sistema deve enviar uma requisição HTTP (`DELETE`) para a API Fake (_JSON Server_) e remover o card da tela imediatamente.

### 🔍 Épico 2: Visualização e Filtro de Parceiros

- **US03 - Mural de Anúncios:** Como um **Visitante**, quero visualizar os cards dos jogadores cadastrados com suas fotos de Agente, ícones de Elo e horários, para escolher com quem desejo jogar.
  - **Critérios de Aceitação:** Os cards devem ser responsivos (Mobile e Desktop) e apresentar visualmente as artes oficiais do jogo obtidas via API.
- **US04 - Filtragem por Elo e Agente:** Como um **Visitante**, quero aplicar filtros por Elo (Patente) e Função do Agente (Duelista, Controlador, etc.) para encontrar parceiros que se encaixem no meu nível e estilo de jogo.
  - **Critérios de Aceitação:** A lista de cards exibidos na tela deve ser atualizada dinamicamente ao selecionar uma opção no menu de filtros.

### 💬 Épico 3: Contato e Conexão

- **US05 - Visualização de Contato (Modal):** Como um **Visitante**, quero clicar no card de um jogador para abrir uma janela de detalhes (Modal) e visualizar seu Discord/Riot ID para adicioná-lo ao jogo.
  - **Critérios de Aceitação:** O Modal deve exibir o usuário de contato formatado com opção de cópia rápida para a área de transferência.
