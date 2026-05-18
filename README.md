# PolyShopping Backend

Fastify API for the PolyShopping demo. This is a plain pnpm workspace, no Nx required.

## Requirements

- Node.js 20+
- pnpm 10+

## Install

```sh
pnpm install
```

## Run

```sh
pnpm dev
```

The API listens on `http://localhost:3000` by default.

Useful endpoints:

- `GET /api/products`
- `GET /api/products/:id`
- `GET /docs`

Override host or port if needed:

```sh
HOST=0.0.0.0 PORT=3001 pnpm dev
```

## Build

```sh
pnpm build
pnpm start
```

`pnpm build` compiles all workspace packages with TypeScript project references. `pnpm start` runs the compiled API from `apps/api/dist/main.js`.

## Test And Lint

```sh
pnpm test
pnpm lint
```

## Workspace Layout

```text
apps/api                  Fastify app
packages/api-products     HTTP routes for products
packages/service-products Product business logic
packages/data-products    In-memory product data
packages/api-types        Shared API types
```
