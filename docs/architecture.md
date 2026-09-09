# 🛠️ Especificação Técnica (Tech Spec) — My MatchMates

Este documento detalha a arquitetura técnica, a stack tecnológica, o modelo de dados e os contratos de API do sistema **My MatchMates**.

## 1. Stack Tecnológica

- **Framework CSS:** Bulma CSS (utilizado para grid responsivo flexbox, formulários e estrutura base de componentes).
- **Estilização Customizada:** Sass/CSS customizado para aplicar o Design System dark/neon do Valorant sobre o Bulma.
- **JavaScript:** Vanilla JS + jQuery para manipulação do DOM, controle do formulário multi-etapas e lógica dos modais.
- **APIs:** JSON Server (API local para armazenamento) e Valorant-API (API pública para mídias oficiais).

---

## 2. Modelo de Dados (Diagrama ER)

```mermaid
erDiagram
    USER ||--o{ MATCH_PREFERENCE : configures
    USER {
        string id PK "Gerado pelo JSON Server"
        string username "Login do usuário"
        string password "Senha do usuário"
        string riotId "Nome de exibição no jogo (ex: ImpostoDeReyna#2204)"
        string elo "Patente atual (ex: Diamante)"
        string eloDivision "Sub-divisão do elo (I, II, III)"
        boolean activeLobby "Status de disponibilidade no feed"
    }

    MATCH_PREFERENCE {
        string id PK
        string userId FK "Vínculo com a conta do jogador"
        string preferredRoles "Funções selecionadas (Duelista, Controlador, etc.)"
        string favoriteAgent "Agente exibido como foto de perfil"
        string preferredAgents "Lista de até 2 agentes prioritários"
        string aptAgents "Lista de até 8 agentes conhecidos"
        string activeDays "Dias da semana ativos"
        string timeSlots "Faixas horárias disponíveis"
        string communication "Tipos de comunicação aceitos"
    }

```

```
{
  "users": [
    {
      "id": "1",
      "username": "impostodereyna",
      "password": "senha_segura_aqui",
      "riotId": "ImpostoDeReyna#2204",
      "elo": "Diamante",
      "eloDivision": "I",
      "activeLobby": true,
      "preferredRoles": ["Controlador", "Duelista"],
      "favoriteAgent": "Reyna",
      "preferredAgents": ["Omen", "Reyna"],
      "aptAgents": ["Reyna", "Omen", "Jett", "Killjoy", "Sova", "Viper", "Fade", "Clove"],
      "activeDays": ["Sex", "Sáb", "Dom"],
      "timeSlots": ["Noite", "Madrugada"],
      "communication": ["Microfone", "Discord Call"]
    }
  ]
}
```
