# FURIA CS:GO Fan Bot

<div align="center">
  <img src="https://raw.githubusercontent.com/vicfaknta10/FuriaFanChat/main/logo.png" alt="FURIA Fan Bot Logo" width="200">
  <h3>Bot de Telegram para torcedores da FURIA CS:GO</h3>
  <p>Acompanhe partidas, estatísticas, notícias e receba notificações do seu time favorito</p>
  
  <a href="https://t.me/Pantera17Bot">
    <img src="https://img.shields.io/badge/Telegram-Bot-blue?style=for-the-badge&logo=telegram" alt="Telegram Bot">
  </a>
  <a href="https://857a0156-685f-4e5b-b066-da7167a84742-00-1cmuvq0lnvlqf.worf.replit.dev">
    <img src="https://img.shields.io/badge/Website-Live-orange?style=for-the-badge&logo=replit" alt="Live Website">
  </a>
</div>

## 💻 Demo Online

Acesse a versão online do projeto:
- **Website**: [FURIA Fan Bot](https://857a0156-685f-4e5b-b066-da7167a84742-00-1cmuvq0lnvlqf.worf.replit.dev)
- **Bot Telegram**: [@Pantera17Bot](https://t.me/Pantera17Bot)

## 📡 Visão Geral

O FURIA Fan Bot é uma solução completa para torcedores da FURIA CS:GO que desejam acompanhar as últimas notícias, resultados de partidas, estatísticas de jogadores e receber notificações em tempo real. O projeto consiste em um website informativo e um bot do Telegram que fornece acesso instantâneo a informações sobre o time.

### Principais funcionalidades:

- 📺 **Atualizações ao vivo** de partidas
- 📈 **Estatísticas detalhadas** de jogadores e mapas
- 🗓 **Calendário** de próximas partidas
- 📰 **Notícias** e atualizações do time
- 🔔 **Notificações personalizadas** de partidas e notícias
- 📱 **Acesso multi-plataforma** via web e Telegram

## 📝 Conteúdo

- [Demo Online](#-demo-online)
- [Visão Geral](#-visão-geral)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Instalação e Execução](#-instalação-e-execução)
- [Como Usar o Bot do Telegram](#-como-usar-o-bot-do-telegram)
- [API e Endpoints](#-api-e-endpoints)
- [Componentes Principais](#-componentes-principais)
- [Contribuições](#-contribuições)
- [Licença](#-licença)

## 🛠 Tecnologias Utilizadas

### Frontend
- **React.js** - Biblioteca para construção da interface
- **TypeScript** - Tipagem estática para JavaScript
- **Tailwind CSS** - Framework CSS utilitário
- **Shadcn UI** - Componentes de UI de alta qualidade
- **React Query** - Gerenciamento de estado e cache
- **Wouter** - Roteamento leve

### Backend
- **Node.js** - Ambiente de execução JavaScript
- **Express** - Framework web para Node.js
- **Telegraf** - Framework para criação de bots do Telegram
- **HLTV API** - Integração com dados de CS:GO
- **Drizzle ORM** - ORM para TypeScript

### Build & Deploy
- **Vite** - Ferramenta de build rápida
- **Replit** - Hospedagem e deploy

## 📊 Estrutura do Projeto

```
.
├── client/              # Código do frontend React
│   ├── src/
│   │   ├── assets/       # Imagens e recursos estáticos
│   │   ├── components/   # Componentes React
│   │   ├── hooks/         # Hooks personalizados
│   │   ├── lib/           # Utilitários e bibliotecas
│   │   ├── pages/         # Páginas da aplicação
│   │   ├── App.tsx        # Componente principal
│   │   ├── index.css      # Estilos globais
│   │   └── main.tsx        # Ponto de entrada
│   └── index.html        # Template HTML
├── server/              # Código do backend
│   ├── index.ts         # Ponto de entrada do servidor
│   ├── routes.ts        # Rotas da API
│   ├── storage.ts       # Interface de armazenamento
│   ├── vite.ts          # Configuração do Vite
│   ├── hltvService.ts   # Integração com HLTV
│   ├── scheduler.ts     # Agendador de tarefas
│   └── telegramBot.ts   # Lógica do bot do Telegram
├── shared/              # Código compartilhado
│   ├── schema.ts        # Esquema do banco de dados
│   └── types.ts         # Tipos compartilhados
├── components.json     # Configuração de componentes Shadcn
├── drizzle.config.ts   # Configuração do Drizzle ORM
├── package.json       # Dependências do projeto
├── postcss.config.js   # Configuração do PostCSS
├── tailwind.config.ts  # Configuração do Tailwind CSS
├── tsconfig.json      # Configuração do TypeScript
└── vite.config.ts      # Configuração do Vite
```

## 💪 Instalação e Execução

### Pré-requisitos

- Node.js v18 ou superior
- npm ou yarn
- Git

### Passo a passo

1. Clone o repositório

```bash
git clone https://github.com/vicfaknta10/FuriaFanChat.git
cd FuriaFanChat
```

2. Instale as dependências

```bash
npm install
# ou
yarn install
```

3. Configure as variáveis de ambiente (opcional)

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```env
BOT_TOKEN=7791446755:AAELG8US7GMIt1CLVsPKnfNmQAYCWbOpPLU
DB_CONNECTION_STRING=seu_db_connection_string
```

4. Inicie o servidor de desenvolvimento

```bash
npm run dev
# ou
yarn dev
```

5. Acesse o aplicativo no navegador

```
http://localhost:3000
```

## 🧹 Como Usar o Bot do Telegram

### Acesso ao Bot

1. Abra o Telegram e pesquise por `@Pantera17Bot` ou acesse diretamente pelo link: [https://t.me/Pantera17Bot](https://t.me/Pantera17Bot)

2. Clique em "Start" ou envie `/start` para iniciar o bot

### Comandos Disponíveis

- `/start` - Inicia o bot e exibe mensagem de boas-vindas
- `/help` - Mostra todos os comandos disponíveis
- `/next` - Informações sobre o próximo jogo
- `/results` - Mostra resultados recentes
- `/roster` - Exibe o elenco atual da FURIA
- `/maps` - Estatísticas de desempenho por mapa
- `/stats [jogador]` - Estatísticas de um jogador específico
- `/news` - Últimas notícias sobre a FURIA
- `/notify matches` - Ativar/desativar notificações de partidas
- `/notify news` - Ativar/desativar notificações de notícias
- `/settings` - Configurações de notificações

## 🚀 API e Endpoints

O backend fornece uma API REST para acesso aos dados:

- **GET /api/team/roster** - Informações sobre o elenco atual
- **GET /api/team/map-stats** - Estatísticas por mapa
- **GET /api/matches/upcoming** - Próximas partidas
- **GET /api/matches/results** - Resultados recentes
- **GET /api/matches/:id** - Detalhes de uma partida específica
- **GET /api/player/:name** - Estatísticas de jogador
- **GET /api/news** - Últimas notícias
- **GET /api/bot/status** - Status do bot do Telegram
- **GET /api/bot/commands** - Lista de comandos disponíveis

## 📂 Componentes Principais

### Frontend

- **Hero**: Seção principal da página com chamada para ação
- **TelegramQRCode**: Código QR para acesso rápido ao bot
- **CommandsSection**: Lista de comandos disponíveis no bot
- **UpcomingMatches**: Exibe próximas partidas da FURIA
- **RecentResults**: Mostra resultados recentes de jogos
- **MapStatsChart**: Gráfico de desempenho por mapa
- **TeamSection**: Informações sobre o elenco atual
- **PerformanceChart**: Gráficos de desempenho de jogadores
- **AboutModal**: Modal com informações detalhadas sobre o bot

### Backend

- **telegramBot.ts**: Configuração e comandos do bot do Telegram
- **hltvService.ts**: Integração com a API HLTV para dados de CS:GO
- **storage.ts**: Interface de armazenamento para dados de usuários
- **scheduler.ts**: Agendador de tarefas para notificações

## 👍 Contribuições

Contribuições são bem-vindas! Para contribuir com o projeto:

1. Faça um fork do repositório
2. Crie uma branch para sua funcionalidade (`git checkout -b feature/nova-funcionalidade`)
3. Faça commit das suas alterações (`git commit -m 'Adiciona nova funcionalidade'`)
4. Faça push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

### Diretrizes para contribuição

- Mantenha o código limpo e bem documentado
- Adicione testes para novas funcionalidades
- Siga as convenções de código existentes
- Atualize a documentação conforme necessário

## 📜 Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

<div align="center">
  <p>Desenvolvido com ❤️ para os torcedores da FURIA</p>
  <a href="https://twitter.com/FURIA">
    <img src="https://img.shields.io/badge/Twitter-@FURIA-blue?style=flat&logo=twitter" alt="Twitter">
  </a>
  <a href="https://www.instagram.com/furiagg/">
    <img src="https://img.shields.io/badge/Instagram-@furiagg-purple?style=flat&logo=instagram" alt="Instagram">
  </a>
</div>
