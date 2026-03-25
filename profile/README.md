## FastY Go

Minimal-dependency Go stack for building fast, server-rendered web applications.

**UI8Kit** — typed component kit built on [templ](https://templ.guide) and Tailwind CSS, inspired by shadcn/ui. Server-side HTML rendering with zero JavaScript frameworks.

```bash
go get github.com/fastygo/ui8kit@latest
```

### Principles

- **Fewer dependencies, fewer problems.** Every package in the stack is chosen for doing one thing well with minimal transitive imports.
- **Server-rendered by default.** HTML is built on the server, sent to the browser, done. Add interactivity only where it matters.
- **Type safety without ceremony.** Go structs as component props. Compile-time checks. No reflection, no interface{}.
- **Production from day one.** Embedded assets, single binary deploys, no build tools required at runtime.

### Stack

| Layer | What |
|-------|------|
| HTTP | fasthttp |
| Routing | fasthttp/router |
| Templates | a-h/templ |
| Components | **fastygo/ui8kit** |
| Styling | Tailwind CSS v4 |
| Storage | bbolt |
| Sessions | fasthttp/session |

### Get started

```go
import (
    "github.com/fastygo/ui8kit/ui"
    "github.com/fastygo/ui8kit/layout"
)
```

Documentation: [github.com/fastygo/ui8kit/docs](https://github.com/fastygo/ui8kit/tree/main/docs)

### Contributing

We welcome contributions of all sizes. See [CONTRIBUTING.md](https://github.com/fastygo/ui8kit/blob/main/CONTRIBUTING.md) in the ui8kit repository.

