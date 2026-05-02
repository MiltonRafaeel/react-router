# React Router (Tutorial) — Invoices App

Projeto de estudo feito em **React + TypeScript + Vite**, seguindo o tutorial do **React Router** para praticar:

- rotas aninhadas (nested routes)
- rotas de índice (index routes)
- parâmetros de rota (dynamic params)
- query string (`search params`)
- navegação programática (`useNavigate`)
- página 404 (fallback com `*`)

## Links

- Repositório: [MiltonRafaeel/react-router](https://github.com/MiltonRafaeel/react-router)
- Documentação / tutorial utilizado: [React Router v6.3.0 — Tutorial](https://reactrouter.com/6.3.0/getting-started/tutorial)

> Observação: no `package.json` deste repositório a versão instalada é `react-router-dom@6.4.1`, mas a base do conteúdo segue o tutorial acima.

## Funcionalidades implementadas

- **Layout base (`App`)** com navegação e `<Outlet />` para renderizar as rotas filhas
- **Welcome (rota index `/`)**
- **Expenses (`/expenses`)**
- **Invoices (`/invoices`)**
  - lista de invoices carregada de um “banco” em memória (`src/data.ts`)
  - filtro por nome via query string `?name=...` usando `useSearchParams`
  - links que **preservam** a query string ao navegar (componente `QueryLink`)
  - destaque de link ativo via `NavLink` + classes CSS
- **Invoice Details (`/invoices/:invoiceId`)**
  - leitura do parâmetro `invoiceId` via `useParams`
  - botão **Delete** remove a invoice do array em memória e navega de volta preservando a query string
- **NotFound (`*`)** para qualquer rota inexistente

## Rotas

| Rota | Descrição |
|------|-----------|
| `/` | Welcome (index route) |
| `/expenses` | Página Expenses |
| `/invoices` | Lista de invoices + filtro `?name=` |
| `/invoices/:invoiceId` | Detalhe de uma invoice |
| `*` | NotFound |

## Stack

- React 18
- TypeScript
- Vite
- React Router DOM 6
- Yarn
- ESLint
- CSS

## Como rodar localmente (Yarn)

```bash
# 1) Clonar
git clone https://github.com/MiltonRafaeel/react-router.git

# 2) Entrar na pasta
cd react-router

# 3) Instalar dependências
yarn

# 4) Rodar em desenvolvimento
yarn dev
