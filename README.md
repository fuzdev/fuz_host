# @fuzdev/fuz_host

> host APIs for JS: filesystem, processes, and the OS, one import across runtimes

fuz_host is the host layer for the [fuz stack](https://www.fuz.dev/): the
filesystem, process, and OS APIs that code needs beyond web standards,
behind one import that works across runtimes. Where a runtime provides
native builtins ([Gro](https://github.com/fuzdev/gro)), the import resolves
to them; elsewhere it resolves to a plain TypeScript implementation on
Node.

**Experimental**: there is no API yet.

Docs: [host.fuz.dev](https://host.fuz.dev/)

## develop

```bash
npm i
gro dev   # the docs site
gro check # typecheck, test, lint, format check
```

## license

[MIT](LICENSE)
