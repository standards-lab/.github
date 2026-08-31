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
- A repository is scoped to one concern of its standard, in five tiers: Core SDK, application
  SDKs, infrastructure libraries, templates, and reference architectures.

## Roadmap

The first target standard, `go-minimal`: one cohesive reference architecture built across
co-evolving levels, its services emitted as container images deployable wherever containers run —
cloud or on premises:

- **Harness** — distributable Claude Code plugins that codify organizational processes.
- **Core SDK** — the process-level packages every program in the standard builds on, where the
  standard first appears as code.
- **Application SDKs and infrastructure libraries** — peers on the Core SDK: an application SDK per
  program shape, and one library per technology, each presenting the technology's common standard
  and the provider's native API — first-class and contained.
- **Templates** — a minimal runnable application per application SDK that new services are seeded
  from.
- **Reference architectures** — a web service that composes the SDKs and infrastructure libraries
  and demonstrates each capability in place, grown in documented layers.

## Shipped

- [`claude-plugins`](https://github.com/standards-lab/claude-plugins) — the plugin marketplace, hosting
  `marathon` and its `marathon-roadmap` extension.
- [`docs`](https://github.com/standards-lab/docs) — the documentation landing zone: the canonical
  home for the organization's architectures, standards, and principles.
- [`go-core`](https://github.com/standards-lab/go-core) — the Core SDK of the `go-minimal` standard:
  layered configuration, process lifecycle, and logging.
- [`go-database`](https://github.com/standards-lab/go-database) — the SQL infrastructure library:
  the standard tier in the base module, with the PostgreSQL provider as a sub-module.
- [`go-web-sdk`](https://github.com/standards-lab/go-web-sdk) — the Application SDK for web
  services: the HTTP server, routing, problem responses, probes, and middleware.
- [`go-web-sdk-template`](https://github.com/standards-lab/go-web-sdk-template) — the web service
  template: scaffolds an initial `go-minimal` web service with `gonew`.
