# fuz_host

> host APIs for JS: filesystem, processes, and the OS, one import across runtimes

fuz_host (`@fuzdev/fuz_host`) is the host layer for the fuz stack: the
filesystem, process, and OS APIs that code needs beyond web standards.
Experimental: the package is a shell, and its API is not designed yet.

For coding conventions, see Skill(fuz-stack).

## Scope

- **Host APIs only.** Anything a web standard covers (`fetch`, `URL`,
  streams, `crypto`, timers, …) is used directly, not wrapped here.
- **One specifier, every runtime.** Each module is meant to resolve through
  package `exports` conditions: a native implementation where the runtime
  provides one ([Gro](https://github.com/fuzdev/gro)'s builtins), and a
  plain TypeScript implementation on Node elsewhere.
- **Zero dependencies.** It sits at the bottom of the stack beside
  [fuz_util](https://github.com/fuzdev/fuz_util), which stays
  runtime-agnostic and does not import this package.

## Gro commands

```bash
gro check     # typecheck, test, lint, format check (run before committing)
gro typecheck # typecheck only (faster iteration)
gro test      # run tests with vitest
gro build     # build the library and the docs site
gro sync      # regenerate files, update package.json exports
```

## Layout

- `src/lib/` — the published modules (`dist/` is built from these); the
  current `example.ts` is a placeholder until the first host module lands
- `src/routes/` — the docs site (host.fuz.dev), with API docs generated
  from `src/lib/` by the `svelte-docinfo` Vite plugin
- `vite.config.ts` — Vite and SvelteKit config

## Project standards

- TypeScript strict mode, `erasableSyntaxOnly`
- tsv (`gro format`) with tabs, 100 char width
