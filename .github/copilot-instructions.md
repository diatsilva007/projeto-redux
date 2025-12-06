# Copilot Instructions for reduxapp

## Visão Geral

Este projeto é uma aplicação React moderna utilizando Vite, React Router e módulos CSS. O objetivo é fornecer um painel de login, gerenciamento de endereços e navegação entre páginas, com estrutura modular e foco em simplicidade.

## Estrutura Principal

- **src/App.jsx**: Define as rotas principais usando `createBrowserRouter`.
- **src/main.jsx**: Ponto de entrada, injeta o `RouterProvider`.
- **src/components/header/**: Componente de cabeçalho reutilizável, com navegação condicional baseada em autenticação (placeholder para lógica de usuário).
- **src/pages/**: Contém as páginas principais (`Home`, `Login`, `address`), cada uma com seu próprio módulo CSS.

## Fluxo de Dados e Navegação

- Navegação controlada por React Router (`react-router-dom`).
- Não há Redux implementado, apesar do nome do projeto.
- O estado do usuário e dos formulários é mantido localmente via `useState`.
- Não há persistência real de dados; ações como login e cadastro de endereço apenas fazem `console.log`.

## Convenções e Padrões

- **Módulos CSS**: Cada página/componente tem seu próprio arquivo `.module.css` para escopo de estilos.
- **Componentização**: O cabeçalho é importado e usado em múltiplas páginas.
- **Funções de navegação**: Uso de `useNavigate` e `Link` para transições de página.
- **Estrutura de pastas**: Cada página em `src/pages/Nome/` com `index.jsx` e `nome.module.css`.

## Comandos de Desenvolvimento

- `npm run dev`: Inicia o servidor de desenvolvimento Vite.
- `npm run build`: Gera build de produção.
- `npm run preview`: Visualiza build de produção localmente.

## Pontos de Atenção para Agentes AI

- Não há backend ou API; simulações de login/cadastro são locais.
- O nome do projeto sugere Redux, mas não há Redux configurado.
- Para adicionar autenticação real, será necessário criar contexto global ou integrar Redux.
- Siga o padrão de módulos CSS e componentização já existente.
- Exemplos de navegação e manipulação de estado local podem ser encontrados em `src/pages/Login/index.jsx` e `src/pages/address/index.jsx`.

## Dependências Externas

- `react`, `react-dom`, `react-router-dom`, `localforage`, `match-sorter`, `sort-by`.
- Vite para build e desenvolvimento.

## Exemplos de Padrões

```jsx
// Exemplo de navegação
const navigate = useNavigate();
navigate("/painel");

// Exemplo de uso de módulo CSS
import styles from "./login.module.css";
<div className={styles.container}>...</div>;
```

Consulte os arquivos em `src/pages/` e `src/components/` para exemplos de padrões recomendados.
