# Software Design Document (Architecture) — My MatchMates

## 1. Visão Geral da Arquitetura
A aplicação adota uma arquitetura Client-Side Rendering (CSR) construída com HTML5 semântico, CSS3/Sass, Bootstrap 5 e JavaScript Vanilla (ES6+). 

A persistência de dados de anúncios criados pelos usuários é realizada via requisições HTTP para uma API Fake local (JSON Server), enquanto imagens e metadados oficiais do jogo (Agentes, Armas e Emblemas de Elo) são consumidos assincronamente da API pública **Valorant-API**.

## 2. Diagrama de Modelo de Dados (Mermaid)

```mermaid
erDiagram
    JOGADOR_ANUNCIO ||--o{ COMPATIBILIDADE : busca
    JOGADOR_ANUNCIO {
        string id PK "Identificador único do anúncio"
        string nick "Nick do jogador no jogo"
        string tag "Tag do Riot ID (ex: BR1)"
        string discord "Usuário do Discord"
        string eloId "Código do Elo selecionado"
        string eloNome "Nome do Elo (ex: Ouro 3)"
        string eloIcone "URL do ícone obtido da API"
        string agenteNome "Nome do Agente (ex: Jett)"
        string agenteIcone "URL do ícone obtido da API"
        string armaFavorita "Nome da arma favorita"
        string periodoJogo "Horário disponível"
        string descricao "Texto descritivo do anúncio"
    }

    VALORANT_API_DADOS {
        string uuid PK "ID da entidade na API externa"
        string displayName "Nome do Agente/Arma/Elo"
        string displayIcon "URL do recurso visual oficial"
    }

    JOGADOR_ANUNCIO }|..|{ VALORANT_API_DADOS : "consome imagens de"
```

## 3. Descrição das Entidades
* **JOGADOR_ANUNCIO (JSON Server / db.json):** Entidade principal do sistema. Armazena os dados cadastrados pelos usuários via formulário e persiste os registros na API Fake local.
* **VALORANT_API_DADOS (API Pública Externa):** Dados dinâmicos de leitura consumidos da URL `https://valorant-api.com/v1/` para preencher os seletores do formulário e fornecer os ativos visuais (imagens) para a entidade de anúncios.

## 4. Tecnologias e Dependências
* **Front-end:** HTML5, CSS3, Sass (SCSS), JavaScript (ES6+ Fetch API).
* **Framework CSS:** Bootstrap 5 (Grid System, Flexbox, Cards, Modais, Navbar).
* **Bibliotecas JS:** jQuery + jQuery Mask Plugin.
* **Ambiente de Dados:** JSON Server (`db.json`) e Web Storage (`localStorage`).
* **Hospedagem:** GitHub Pages.