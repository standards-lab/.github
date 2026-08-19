# Standards Lab

Reference architectures for modern, inner-source enterprise development. The intent is to incubate
an ecosystem of reusable, well-organized patterns teams adopt and build on rather than re-deriving
the same foundations project by project. Modern means the next generation of primitives for what
software emits — the library, the binary, the container image — not any one deployment venue. The
organization develops named target standards, each a complete reference architecture built and
proven by use across co-evolving levels, declaring its own dependency line and deployment targets;
each repository is a worked example for others to follow.

## The principles

- Software interfaces with a technology at the resolution its purpose requires.
- Dependencies flow downward only; interfaces are defined where they're consumed.
- A minimal, deliberate dependency footprint. Each target standard declares the dependency line its
  repositories hold: `go-minimal` draws it at the standard library — no frameworks, raw drivers and
  plain SQL over ORMs, a web-platform-native client. A standard built on a framework is its own
  target standard.
- Every capability presents two tiers: the technology's common standard, and the provider's native
  API — first-class and contained.
- Independent, artifact-keyed releases per library and service. Cross-language counterparts arrive
  as derived standards; a .NET standard derived from `go-minimal` is anticipated.

## Roadmap

The first target standard, `go-minimal`: one cohesive reference architecture built across
co-evolving levels, its services emitted as container images deployable wherever containers run —
cloud or on premises:

- **Harness** — distributable Claude Code plugins that codify organizational processes.
- **Libraries** — layered capability libraries, where the standard first appears as code.
- **Service template** — a minimal runnable service that new services are seeded from.
- **Reference service** — a web service that composes the libraries and demonstrates each capability in
  place, grown in documented layers.

## Shipped

- [`claude-plugins`](https://github.com/standards-lab/claude-plugins) — the plugin marketplace, hosting
  `marathon`.
- [`go-core`](https://github.com/standards-lab/go-core) — the base SDK of the `go-minimal` standard:
  layered configuration, process lifecycle, and logging.
- [`go-libraries`](https://github.com/standards-lab/go-libraries) — the Go capability libraries: the base
  module of the library level.
- [`go-service-template`](https://github.com/standards-lab/go-service-template) — the service template
  baseline: the minimal runnable service new services are seeded from.
