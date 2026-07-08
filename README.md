<div align="center">

# SuperQuery — Web

### Query at super speed.

**`RUST-NATIVE` · `SUBQUERY COMPATIBLE`**

The official website and documentation portal for **SuperQuery** — a
high-integrity indexing framework designed for the most demanding blockchain
data pipelines. The performance of Rust, the familiarity of SubQuery.

[Live site](https://superquery.vercel.app/) ·
[SuperQuery core](https://github.com/blockSuperquery)

</div>

---

## About

This repository contains the SuperQuery marketing site and documentation portal,
built with [Nuxt](https://nuxt.com) and [Nuxt UI](https://ui.nuxt.com). It
presents the SuperQuery platform:

- **Native performance** — mappings compile to native Rust code: no interpreter,
  no GC pauses, predictable tail latency under load.
- **High integrity** — deterministic indexing with ACID-compliant PostgreSQL
  storage and reorg-safe historical state.
- **SubQuery compatible** — reuse your GraphQL schema and project manifest; a
  migration path, not a rewrite.
- **Observable** — first-class Prometheus metrics, health endpoints, and
  structured tracing for production fleets.

For the indexing engine itself, see the SuperQuery core (Rust) repository.

## Tech Stack

- [Nuxt](https://nuxt.com) — Vue meta-framework
- [Nuxt UI](https://ui.nuxt.com) — component library
- [pnpm](https://pnpm.io) — package manager
- Deployed on [Vercel](https://vercel.com)

## Setup

Install dependencies:

```bash
pnpm install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
pnpm dev
```

## Production

Build the application for production:

```bash
pnpm build
```

Locally preview the production build:

```bash
pnpm preview
```

See the [Nuxt deployment documentation](https://nuxt.com/docs/getting-started/deployment)
for more information. Production builds deploy automatically to Vercel on push to
`main`.

## Renovate integration

Dependency updates are managed by [Renovate](https://github.com/apps/renovate/installations/select_target).

## License

See [LICENSE](LICENSE).
