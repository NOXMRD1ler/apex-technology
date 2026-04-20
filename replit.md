# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.

## Artifacts

### Apex Technology (`artifacts/apex-technology`)
- **Type**: react-vite, preview at `/`
- **Stack**: React + Vite + TypeScript + Tailwind CSS + Wouter + Framer Motion
- **Description**: Premium black-and-white website for Apex Technology, a 4-person IT studio offering bespoke web development.
- **Features**:
  - Role-based auth (Client vs Developer) stored in localStorage via Context API
  - Public pages: Home, Services, About, Portfolio, Process, Contact
  - Client features: Chat with developers, multi-step order form, profile
  - Developer features: /our-projects workspace with shared board + client orders
  - Hamburger mobile menu, toast notifications, smooth framer-motion animations
  - Monochrome design: #0a0a0a background, #ffffff text, Space Grotesk + JetBrains Mono fonts
  - All data (auth, messages, orders) stored in localStorage for demo
