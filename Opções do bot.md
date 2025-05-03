 FURIA CS Fan Application

Um aplicativo multiplataforma para fãs do time FURIA CS, oferecendo informações atualizadas sobre o time, jogadores, partidas e muito mais!

## 📋 Visão Geral

Este projeto foi desenvolvido para proporcionar aos fãs da FURIA CS uma experiência completa de acompanhamento do time. O sistema funciona em 3 plataformas diferentes:

1. **Bot do Telegram**: Acessível através do Telegram, permitindo interação por comandos
2. **Aplicativo Standalone**: Versão local com interface de terminal interativa
3. **Interface Web**: Aplicativo web responsivo usando Flask

## 🌟 Funcionalidades

- 📰 **Notícias**: Últimas notícias sobre a FURIA CS
- 🎮 **Partidas**: Informações sobre próximas partidas e horários
- 👥 **Jogadores**: Dados detalhados sobre os jogadores, incluindo fotos, estatísticas e funções
- 🏆 **Conquistas**: Principais títulos e colocações do time
- 📊 **Stats**: Estatísticas de desempenho do time
- 📱 **Redes Sociais**: Links para as redes sociais da FURIA
- 🗣️ **Torcida**: Mensagens e interações com a torcida
- 🔴 **Ao Vivo**: Atualizações em tempo real de partidas em andamento
- 📱 **WhatsApp**: Contato rápido via WhatsApp

## 🚀 Como Executar

### Bot do Telegram
```bash
python furia_bot.py
```

### Aplicativo Standalone (Interativo)
```bash
python furia_standalone.py
```

### Aplicativo Standalone (Não-Interativo)
```bash
python furia_standalone_non_interactive.py noticias
python furia_standalone_non_interactive.py jogadores
python furia_standalone_non_interactive.py partidas
# Outros comandos: conquistas, stats, redes, torcida, aovivo, whatsapp
```

### Interface Web
```bash
gunicorn --bind 0.0.0.0:5000 --reuse-port --reload main:app
```
Ou use o workflow "Start application" no Replit.

## 🔧 Tecnologias Utilizadas

- **Python**: Linguagem principal de programação
- **python-telegram-bot**: Para a funcionalidade do bot do Telegram
- **Flask**: Framework web para a interface web
- **Gunicorn**: Servidor WSGI para a aplicação web
- **Bootstrap**: Framework CSS para estilização responsiva
- **SVG**: Para imagens vetoriais dos jogadores
- **JSON**: Para armazenamento de dados persistentes

## 📁 Estrutura do Projeto

- `furia_bot.py`: Implementação do bot do Telegram
- `furia_standalone.py`: Versão interativa para terminal
- `furia_standalone_non_interactive.py`: Versão para linha de comando
- `main.py`: Aplicação web Flask
- `static/`: Arquivos estáticos (CSS, JavaScript e imagens)
- `templates/`: Templates HTML para a aplicação web
- `utils/`: Módulos utilitários (como gerenciamento de banco de dados)
- `data/`: Armazenamento de dados locais em JSON

## 🎭 Jogadores Atuais

| Nome | Função | Nacionalidade |
|------|--------|--------------|
| KSCERATO | Rifler | 🇧🇷 Brasil |
| YUURIH | Entry Fragger | 🇧🇷 Brasil |
| ART | AWPer/IGL | 🇧🇷 Brasil |
| FALEN | Support | 🇧🇷 Brasil |
| SAFFEE | AWPer | 🇧🇷 Brasil |

## 🔄 Mantenha-se atualizado

O aplicativo sempre exibe as informações mais recentes sobre a FURIA CS, incluindo:
- Status de partidas em tempo real
- Estatísticas atualizadas dos jogadores
- Notícias e conquistas recentes

## 📱 Bot do Telegram

Para usar o bot do Telegram, busque por `@FuriaCS_Fan_Bot` ou acesse https://t.me/FuriaCS_Fan_Bot.

Comandos disponíveis:
- `/start` - Iniciar o bot
- `/noticias` - Ver últimas notícias
- `/partidas` - Ver próximas partidas
- `/jogadores` - Ver informações dos jogadores
- `/conquistas` - Ver conquistas do time
- `/stats` - Ver estatísticas do time
- `/redes` - Ver redes sociais
- `/torcida` - Ver mensagens da torcida
- `/aovivo` - Ver partidas ao vivo
- `/whatsapp` - Ver contato de WhatsApp

## 🖼️ Fotos dos Jogadores

O projeto inclui fotos estilizadas de todos os jogadores em formato SVG, proporcionando uma experiência visual atraente tanto na interface web quanto nos aplicativos.

## 🧡 #DIADEFURIA
