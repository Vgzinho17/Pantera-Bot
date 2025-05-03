# FURIA CS Telegram Bot - Documentação Técnica

## 📋 Visão Geral

Este documento contém a documentação técnica do bot do Telegram para fãs da FURIA CS. O bot fornece informações sobre o time, jogadores, partidas, estatísticas e outras funcionalidades para os fãs.

## 🤖 Informações do Bot

- **Nome**: FURIA CS Fan Bot
- **Username**: @FuriaCS_Fan_Bot

## 🛠️ Arquitetura do Bot

O projeto utiliza a estrutura de aplicação moderna da biblioteca `python-telegram-bot` (v22.0+) com padrões assíncronos e handlers baseados em funções.

### Componentes Principais:

1. **Inicialização do Bot**: Configuração da aplicação, definição de handlers e rotina principal.
2. **Handlers de Comandos**: Funções para processar comandos específicos enviados pelos usuários.
3. **Handlers de Mensagens**: Funções para processar mensagens regulares, interpretando e respondendo adequadamente.
4. **Gerenciamento de Dados**: Sistema para carregar, armazenar e atualizar dados persistentes.

## 🚀 Como Executar

```bash
# Instalar dependências
pip install python-telegram-bot pytz

# Executar o bot
python furia_bot.py
```

Você também pode usar o workflow `telegram_bot` no Replit:

```bash
# No ambiente Replit
pip install python-telegram-bot pytz && python furia_bot.py
```

## 📡 Comandos Disponíveis

| Comando | Descrição |
|---------|-----------|
| `/start` | Inicia o bot com uma mensagem de boas-vindas e as opções disponíveis |
| `/noticias` | Exibe as últimas notícias sobre a FURIA CS |
| `/partidas` | Mostra informações sobre as próximas partidas da FURIA |
| `/jogadores` | Lista detalhes dos jogadores da equipe atual |
| `/conquistas` | Exibe as principais conquistas e títulos do time |
| `/stats` | Mostra estatísticas de desempenho da equipe |
| `/redes` | Lista os canais de redes sociais oficiais da FURIA |
| `/torcida` | Exibe mensagens enviadas pela torcida |
| `/aovivo` | Informa sobre partidas que estão acontecendo no momento |
| `/whatsapp` | Fornece o link de contato por WhatsApp |

## 📦 Estrutura de Dados

Os dados do time são armazenados em uma estrutura JSON com os seguintes componentes:

```json
{
  "torcida_messages": [],    // Mensagens da torcida
  "live_matches": {},        // Informações sobre partidas ao vivo
  "team_info": {
    "jogadores": {},         // Detalhes dos jogadores
    "conquistas": [],        // Lista de conquistas
    "proximas_partidas": [], // Agenda de partidas
    "redes_sociais": {},     // Links para redes sociais
    "whatsapp": ""           // Link para contato no WhatsApp
  }
}
```

## 📂 Integração com Sistema de Arquivos

O bot utiliza o sistema de arquivos para persistência, armazenando dados em:

- `data/team_data.json`: Dados da equipe, jogadores, conquistas, etc.
- `data/bot_data.json`: Dados específicos do bot como contadores, estatísticas de uso, etc.

## 🔄 Fluxo de Processamento

1. O usuário envia um comando ou mensagem para o bot
2. O framework `python-telegram-bot` roteia a mensagem para o handler apropriado
3. O handler processa o comando e busca os dados necessários
4. Uma resposta formatada é enviada de volta ao usuário

## 🧩 Módulos Auxiliares

### `DBManager` (em utils/db_manager.py)

Classe que gerencia a persistência de dados via arquivo JSON, simulando funcionalidades de banco de dados:

- `get_value(key, default=None)`: Recupera um valor armazenado
- `set_value(key, value)`: Define um valor para uma chave específica
- `increment_value(key, increment=1)`: Incrementa um valor numérico

## 🔄 Atualizações Futuras Planejadas

1. Adicionar notificações push para partidas ao vivo
2. Implementar sistema de votação para MVP das partidas
3. Adicionar mais estatísticas detalhadas por jogador
4. Implementar sistema de lembretes para próximas partidas

## 🐞 Solução de Problemas

### Problemas comuns e soluções:

1. **Bot não responde**: Verifique se o token está correto e se o bot está rodando
2. **Erros na exibição de dados**: Verifique a estrutura do arquivo JSON
3. **Comandos não funcionam**: Certifique-se de que todos os handlers estão registrados corretamente

## 📚 Recursos da API do Telegram Utilizados

- `telegram.ext.Application`: Para gerenciar o ciclo de vida do bot
- `telegram.ext.CommandHandler`: Para processar comandos
- `telegram.ext.MessageHandler`: Para processar mensagens normais
- `telegram.ext.filters`: Para filtrar tipos específicos de mensagens

## 👨‍💻 Manutenção

Para atualizar informações da equipe:

1. Edite o arquivo `data/team_data.json` com os novos dados
2. Reinicie o bot para carregar as alterações

Para atualizar o bot:

1. Faça as alterações necessárias no código
2. Reinicie o serviço do bot

## 🧡 #DIADEFURIA

Desenvolvido com paixão por um fã da FURIA CS.

---

© 2024 FURIA CS Telegram Bot | Desenvolvido por [Vgzinho17](https://github.com/Vgzinho17)
