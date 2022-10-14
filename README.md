# nuxt3@3.0.0-rc.12

[#7726](https://github.com/nuxt/framework/pull/7726) includes `workspaceDir` in tsconfig include. In the context of a monorepo that isn't solely Nuxt oriented, `vue-tsc` expands to the entire repo subsequently reporting issues from unrelated project paths. In larger monorepos, this can be a significant performance hit particularly where pipelines are run in parallel.

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/cuebit/nuxt-rc12-monorepo?file=md!README.md)

### Typecheck

```bash
pnpm install && pnpm start
```

Observe typecheck fails in `app/nuxt1` but passes in `app/nuxt2`.
