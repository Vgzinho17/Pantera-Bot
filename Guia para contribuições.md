# Guia de Contribuição

Obrigado por considerar contribuir para o FURIA Fan Bot! Este documento fornece as diretrizes para contribuir com o projeto.

## 🛠 Configuração do Ambiente de Desenvolvimento

### Pré-requisitos

- Node.js v18 ou superior
- npm v8 ou superior
- Git

### Passos para Configuração

1. Clone o repositório:

```bash
git clone https://github.com/vicfaknta10/FuriaFanChat.git
cd FuriaFanChat
```

2. Instale as dependências:

```bash
npm install
```

3. Configure as variáveis de ambiente:

Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:

```env
BOT_TOKEN=seu_token_do_telegram_bot
HLTV_API_KEY=sua_chave_api_hltv_opcional
```

4. Inicie o servidor de desenvolvimento:

```bash
npm run dev
```

## 🔧 Estrutura do Projeto

### Frontend (React + TypeScript)

- `/client/src/components` - Componentes React reutilizáveis
- `/client/src/pages` - Páginas da aplicação
- `/client/src/assets` - Recursos estáticos (imagens, fontes)
- `/client/src/hooks` - React hooks personalizados
- `/client/src/lib` - Utilitários e configurações

### Backend (Node.js + Express + TypeScript)

- `/server/index.ts` - Ponto de entrada do servidor
- `/server/routes.ts` - Rotas da API
- `/server/telegramBot.ts` - Lógica do bot do Telegram
- `/server/hltvService.ts` - Serviço para busca de dados do HLTV
- `/server/storage.ts` - Interface de armazenamento de dados
- `/server/scheduler.ts` - Agendador para notificações

### Compartilhado

- `/shared/schema.ts` - Definições de esquema do banco de dados
- `/shared/types.ts` - Tipos compartilhados entre frontend e backend

## 💡 Fluxo de Trabalho de Desenvolvimento

### Adição de Novas Funcionalidades

1. Crie uma nova branch para sua funcionalidade:

```bash
git checkout -b feature/nome-da-funcionalidade
```

2. Implemente sua funcionalidade seguindo as convenções de código:
   - Use TypeScript estritamente tipado
   - Siga os padrões de codificação do projeto
   - Adicione comentários em partes complexas

3. Teste sua funcionalidade localmente:
   - Certifique-se de que a aplicação inicializa sem erros
   - Verifique se todas as funcionalidades existentes continuam funcionando
   - Teste sua nova funcionalidade em diferentes dispositivos/navegadores (se aplicável)

4. Envie suas alterações:

```bash
git add .
git commit -m "descrição clara das alterações"
git push origin feature/nome-da-funcionalidade
```

5. Crie um Pull Request para a branch `main`.

### Correção de Bugs

1. Crie uma branch para a correção:

```bash
git checkout -b fix/descricao-do-bug
```

2. Corrija o bug e certifique-se de que o problema foi resolvido.

3. Envie suas alterações e crie um Pull Request, incluindo uma descrição clara do bug e como ele foi corrigido.

## 📖 Convenções de Código

### Estilo de Código

- Use indentação de 2 espaços
- Termine todas as linhas com ponto e vírgula
- Use aspas simples para strings
- Mantenha linhas com no máximo 100 caracteres
- Use camelCase para variáveis e funções
- Use PascalCase para componentes React e classes
- Use UPPER_CASE para constantes

### Nomenclatura

- **Componentes React**: Use nomes descritivos e PascalCase (ex: `UserProfile`, `MatchCard`)
- **Hooks**: Prefixe com `use` (ex: `useFetchData`, `useMatchStatus`)
- **Arquivos de componentes**: Use o mesmo nome do componente (ex: `Button.tsx`)
- **Arquivos de serviço**: Sufixo `Service` (ex: `userService.ts`)
- **Interfaces TypeScript**: Prefixo `I` ou sem prefixo dependendo do contexto (ex: `IUser` ou `User`)
- **Tipos TypeScript**: Sufixo `Type` (ex: `ButtonType`)

### Estrutura de Componentes React

```tsx
// Imports organizados por grupos (React, bibliotecas, componentes, estilos)
import { useState, useEffect } from 'react';
import { useQuery } from '@tanstack/react-query';

// Interfaces/Types no topo
interface ComponentProps {
  title: string;
  data: any[];
}

// Componente com nome descritivo
const ExampleComponent = ({ title, data }: ComponentProps) => {
  // State e hooks
  const [isActive, setIsActive] = useState(false);
  
  // Efeitos
  useEffect(() => {
    // Lógica do efeito
  }, []);
  
  // Funções auxiliares
  const handleClick = () => {
    setIsActive(!isActive);
  };
  
  // Renderização condicional
  if (!data || data.length === 0) {
    return <div>Nenhum dado disponível</div>;
  }
  
  // Retorno do componente
  return (
    <div>
      <h2>{title}</h2>
      {/* Resto do JSX */}
    </div>
  );
};

export default ExampleComponent;
```

## 📝 Documentação e Comentários

### Documentação em Código

- Adicione JSDoc para componentes, funções e métodos públicos:

```typescript
/**
 * Busca informações detalhadas sobre uma partida específica
 * @param matchId - ID único da partida a ser buscada
 * @returns Detalhes da partida ou null se não encontrada
 */
async function getMatchById(matchId: number): Promise<Match | null> {
  // Implementação
}
```

- Use comentários para explicar blocos complexos de código
- Evite comentários óbvios que apenas repetem o que o código já expressa
- Atualize a documentação em README.md quando fizer alterações significativas

## 💬 Comunicação

### Issues

- Use o rastreador de issues do GitHub para relatar bugs ou solicitar novas funcionalidades
- Forneça o máximo de detalhes possível ao criar uma issue
- Use etiquetas apropriadas (bug, feature, enhancement, etc.)

### Pull Requests

- Vincule o PR à issue correspondente, se houver
- Forneça uma descrição clara das alterações
- Inclua capturas de tela para alterações visuais
- Responda aos comentários e revise o código quando solicitado

## 👷 Diretriz para Mensagens de Commit

Siga o padrão [Conventional Commits](https://www.conventionalcommits.org/):

```
<tipo>(<escopo opcional>): <descrição>

[corpo opcional]

[rodapé opcional]
```

Tipos comuns:
- **feat**: Nova funcionalidade
- **fix**: Correção de bug
- **docs**: Alterações na documentação
- **style**: Mudanças que não afetam o significado do código (espaços, formatação, etc)
- **refactor**: Refatoração de código
- **test**: Adição ou correção de testes
- **chore**: Atualizações de tarefas de build, configurações, etc

Exemplos:
```
feat(bot): adiciona comando para ver estatísticas por mapa
fix(ui): corrige sobreposição de texto nos cards de partidas
docs: atualiza instruções de instalação
```

## 🏅 Processo de Review

### Critérios para Aprovação

- O código segue as convenções do projeto
- Não há erros de TypeScript ou ESLint
- A funcionalidade ou correção funciona conforme esperado
- Não há regressões nas funcionalidades existentes
- Documentação atualizada, se necessário

### Processo de Merge

- Os PRs precisam de pelo menos uma aprovação
- A branch deve estar atualizada com a `main` antes do merge
- Os PRs serão mesclados usando squash merge para manter o histórico limpo

## 🚀 Implantação

O processo de implantação é automatizado através do Replit. Qualquer código mesclado na branch `main` será automaticamente implantado no ambiente de produção.

### Verificações pré-implantação

- A aplicação é construída e testada automaticamente
- Verificações de tipo são executadas
- Linting é verificado

## 🎉 Reconhecimento de Contribuições
