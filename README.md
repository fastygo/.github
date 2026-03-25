<p align="center">
  <kbd>
    <img src="https://raw.githubusercontent.com/fastygo/.github/refs/heads/main/profile/fastygo.png" width="256" alt="FastY Go" />
  </kbd>
</p>

<h2 align="center">FastY Go</h2>

<p align="center">
  Ship fast. Ship lean. Ship in Go.
</p>

---

## What this is

FastY Go is a collection of production-ready tools and example applications that demonstrate how to build modern web services in Go with a minimal, high-performance stack — no frameworks, no ORMs, no bloat.

## Stack

| Concern | Solution | Why |
|---------|----------|-----|
| HTTP server | fasthttp | Consistent low-latency under high concurrency |
| Routing | fasthttp/router | Zero-allocation path matching |
| Templates | a-h/templ | Type-safe HTML components compiled to Go |
| UI components | [fastygo/ui8kit](https://github.com/fastygo/ui8kit) | Tailwind CSS primitives in the style of shadcn/ui |
| Styling | Tailwind CSS v4 | Utility-first, design-token driven |
| Storage | bbolt | Embedded key-value store, single-file database |
| Sessions | fasthttp/session | Server-side sessions with pluggable backends |

One binary. No runtime dependencies. Deploy anywhere.

## UI8Kit

The component library at the center of FastY Go applications:

```bash
go get github.com/fastygo/ui8kit@latest
```

```go
import (
    "github.com/fastygo/ui8kit/ui"
    "github.com/fastygo/ui8kit/layout"
)

templ Page() {
    @layout.Shell(layout.ShellProps{Title: "Dashboard", BrandName: "FastY"}) {
        @ui.Stack(ui.StackProps{}) {
            @ui.Title(ui.TitleProps{Order: 1}, "Welcome")
            @ui.Button(ui.ButtonProps{Variant: "primary"}, "Get started")
        }
    }
}
```

Typed props. Server-rendered HTML. Embedded CSS. Dark mode. Zero JavaScript frameworks.

Full documentation: [ui8kit/docs](https://github.com/fastygo/ui8kit/tree/main/docs)

## Principles

**Minimal dependencies.** Every package earns its place. Transitive imports are counted, not ignored.

**Server-rendered by default.** HTML is assembled on the server and sent to the browser. Client-side interactivity is opt-in, not assumed.

**Single binary deployment.** CSS, icons, and templates compile into the Go binary. No asset pipelines in production. No Node.js on the server.

**Explicit over magical.** Go structs as props, not string maps. Compile-time errors, not runtime surprises. Readable code over clever abstractions.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](https://github.com/fastygo/ui8kit/blob/main/CONTRIBUTING.md) for setup instructions and commit conventions.

## License

MIT
