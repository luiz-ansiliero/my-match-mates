# MyMatchMates — Duo & Team Finder

**Autor:** Luiz Eduardo Ferreira Ansiliero
**Curso:** Tecnologia em Sistemas para Internet — UTFPR  
**Disciplina:** Desenvolvimento de Páginas Web com Framework e CSS

---

Este projeto tem como objetivo implementar progressivamente e de forma didática uma aplicação web voltada para a conexão de jogadores e formação de times no cenário de eSports (iniciando com suporte ao jogo Valorant). O sistema permite o cadastro de anúncios de jogadores com suas respectivas preferências (elo, agente, armas favoritas e horários) e a filtragem de duos para partidas competitivas.

O frontend da aplicação foi desenvolvido utilizando HTML5, CSS3/Sass e JavaScript (com jQuery), consumindo a API pública **Valorant-API** para mídias oficiais do jogo e o **JSON Server** para a simulação de persistência dos anúncios de usuários.

---

## 📚 Documentação do Projeto

Para entender as regras de negócio, o escopo e a arquitetura técnica da aplicação, consulte os documentos abaixo:

- 📄 [Product Requirements Document (PRD)](docs/prd.md) — Visão geral, atores e histórias de usuário.
- 🛠️ [Especificação Técnica (Tech Spec)](docs/architecture.md) — Diagrama de banco de dados (DER em Mermaid), arquitetura e rotas da API.

---

## 🎨 Design

- 🎨 **Design System** — Identidade visual (Cores, Tipografia e Componentes).
- 🖼️ **Protótipo no Figma** — Telas interativas da aplicação.
- 🌐 **Site em Produção** — GitHub Pages (`https://seu-usuario.github.io/my-match-mates/`)

---

## 💻 Tecnologias e Dependências

- **Framework CSS:** Bootstrap 5
- **Preprocessador CSS:** Sass (SCSS)
- **JavaScript:** Vanilla (ES6+) + jQuery (para manipulação do DOM e uso de plugins)
- **API Fake:** JSON Server (para simular uma API REST de anúncios)
- **API Pública:** Valorant-API (para catálogo de mídias de agentes, elos e armas)

---

## ✅ Checklist | Indicadores de Desempenho (ID) dos Resultados de Aprendizagem (RA)

### RA1 - Utilizar Frameworks CSS para estilização de elementos HTML e criação de layouts responsivos.

- [ ] **ID 01** - Prototipa interfaces adaptáveis para no mínimo os tamanhos de tela mobile e desktop, usando ferramentas de design tradicionais (Figma, Quant UX ou Sketch) ou IA (Stitch).
- [ ] **ID 02** - Implementa layout responsivo com Framework CSS (Bootstrap, Materialize, Tailwind + DaisyUI) usando Flexbox ou Grid do próprio framework.
- [ ] **ID 03** - Implementa layout responsivo com CSS puro, usando Flexbox ou Grid Layout.
- [ ] **ID 04** - Utiliza componentes prontos de um Framework CSS (ex.: card, button) e componentes JavaScript do framework (ex.: modal, carousel).
- [ ] **ID 05** - Cria layout fluido usando unidades relativas (vw, vh, %, em, rem) no lugar de unidades fixas (px).
- [ ] **ID 06** - Aplica um Design System consistente (cores, tipografia, padrões de componentes) em toda a aplicação.
- [ ] **ID 07** - Utiliza Sass (SCSS) com ou sem framework, aplicando variáveis, mixins e funções para modularizar o código.
- [ ] **ID 08** - Aplica tipografia responsiva (media queries mobile first) ou tipografia fluida (função clamp() + unidades relativas).
- [ ] **ID 09** - Aplica técnicas de responsividade de imagens usando CSS (object-fit, containers com unidades relativas).
- [ ] **ID 10** - Otimiza imagens usando formatos modernos (WebP) e carregamento adaptativo (srcset, picture, ou parâmetros do Cloudinary).

### RA2 - Realizar tratamento de formulários e aplicar validações customizadas no lado cliente.

- [ ] **ID 11** - Implementa validação HTML nativa (campos obrigatórios, tipos, limites de caracteres) com mensagens de erro/sucesso no lado cliente.
- [ ] **ID 12** - Aplica expressões regulares (REGEX) para validações customizadas (e-mail, telefone, datas, etc.)
- [ ] **ID 13** - Utiliza elementos de seleção em formulários (checkbox, radio, select) para coleta de dados.
- [ ] **ID 14** - Implementa leitura e escrita no Web Storage (localStorage/sessionStorage) para persistir dados localmente.

### RA3 - Aplicar ferramentas para otimização do processo de desenvolvimento web.

- [ ] **ID 15** - Configura ambiente com Node.js e NPM para gerenciamento de pacotes e dependências.
- [ ] **ID 16** - Utiliza boas práticas de versionamento no Git/GitHub (branch main ou branches específicos, uso de .gitignore).
- [x] **ID 17** - Mantém um README.md padronizado, conforme template da disciplina, com checklist preenchido.
- [ ] **ID 18** - Organiza arquivos do projeto de forma modular, seguindo padrão de exemplo fornecido.
- [ ] **ID 19** - Configura linters e formatadores (ESLint, Prettier) para manter qualidade e padronização do código.

### RA4 - Aplicar bibliotecas de funções e componentes em JavaScript para aprimorar a interatividade de páginas web.

- [ ] **ID 20** - Utiliza jQuery para manipulação do DOM e interatividade (eventos, animações, manipulação de elementos).
- [ ] **ID 21** - Integra e configura um plugin jQuery relevante (ex.: jQuery Mask Plugin).

### RA5 - Efetuar requisições assíncronas para uma API fake e APIs públicas, permitindo a obtenção e manipulação de dados dinamicamente.

- [ ] **ID 22** - Realiza requisições assíncronas para uma API fake (ex.: JSON Server) para persistir dados de um formulário.
- [ ] **ID 23** - Realiza requisições assíncronas para uma API fake para exibir dados na página.
- [ ] **ID 24** - Realiza requisições assíncronas para APIs públicas reais (Valorant-API), exibindo os dados e tratando erros.

---

## 🚀 Manual de Execução

1. Clonar o repositório:
   ```bash
   git clone [https://github.com/SEU-USUARIO/my-match-mates.git](https://github.com/SEU-USUARIO/my-match-mates.git)
   ```
