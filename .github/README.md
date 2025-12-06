# Projeto ReduxApp

## Visão Geral

Este projeto é uma aplicação React moderna, criada com Vite, que utiliza Redux Toolkit e Redux Saga para gerenciamento de estado global e efeitos assíncronos. O objetivo é fornecer um painel de login, gerenciamento de endereços e navegação entre páginas, com estrutura modular e foco em simplicidade.

## Funcionalidades

- Login de usuário (simulado, sem backend)
- Cadastro e remoção de endereço do usuário
- Listagem de usuários via API pública (jsonplaceholder)
- Navegação entre páginas usando React Router
- Estado global com Redux Toolkit
- Efeitos assíncronos com Redux Saga

## Estrutura de Pastas

```
src/
  App.jsx            # Rotas principais
  main.jsx           # Ponto de entrada
  components/
    header/          # Cabeçalho reutilizável
  pages/
    Home/            # Painel principal
    Login/           # Página de login
    address/         # Gerenciamento de endereço
  redux/
    user/            # Slice e saga do usuário
    store.js         # Configuração da store
    root-reducer.js  # Combinação de reducers
    sagas.js         # Root saga
```

## Principais Tecnologias

- [React](https://react.dev/)
- [Vite](https://vitejs.dev/)
- [Redux Toolkit](https://redux-toolkit.js.org/)
- [Redux Saga](https://redux-saga.js.org/)
- [React Router DOM](https://reactrouter.com/)
- [Axios](https://axios-http.com/)

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/diatsilva007/projeto-redux
   cd seu-repo
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```

## Scripts Disponíveis

- `npm run dev`: Inicia o servidor de desenvolvimento Vite
- `npm run build`: Gera build de produção
- `npm run preview`: Visualiza build de produção localmente

## Fluxo de Dados

- O estado do usuário e dos formulários é mantido globalmente via Redux Toolkit
- Efeitos assíncronos (ex: busca de usuários) são tratados com Redux Saga
- Não há persistência real de dados; login e cadastro são simulados

## Exemplos de Uso

### Login

```jsx
const dispatch = useDispatch();
dispatch(createUser({ name, email }));
```

### Buscar usuários

```jsx
dispatch(fetchUsers());
```

### Adicionar endereço

```jsx
dispatch(addAddress({ location, number }));
```

## Observações

- O nome do projeto sugere Redux, mas a versão original não utilizava Redux. Agora, Redux Toolkit e Saga estão integrados.
- Para adicionar autenticação real, será necessário criar contexto global ou integrar backend/API.
- Siga o padrão de módulos CSS e componentização já existente.

## Licença

Este projeto está sob a licença MIT.
