# Standards Lab

Platform-agnostic reference architectures for modern cloud-native enterprise development. The intent is to
incubate an inner-source ecosystem for digital modernization across the enterprise — reusable,
well-organized patterns teams adopt and build on rather than re-deriving the same foundations project by
project. The standard is built and proven by use, across co-evolving levels; each level is a worked
example for others to follow.

## The standard

- The lowest practical level of abstraction, with no frameworks by default. Frameworks appear only as
  optional variants.
- Dependencies flow downward only; interfaces are defined where they're consumed.
- Independent, artifact-keyed releases per library and service, with cross-language symmetry as a
  first-class convention.

## Roadmap

One cohesive, platform-agnostic reference architecture, built across co-evolving levels:

- **Harness** — distributable Claude Code plugins that codify organizational processes.
- **Libraries** — layered capability libraries, where the standard first appears as code.
- **Service template** — a minimal runnable service that new services are seeded from.
- **Reference service** — a web service that composes the libraries and demonstrates each capability in
  place, grown in documented layers.

## Shipped

- [`claude-plugins`](https://github.com/standards-lab/claude-plugins) — the plugin marketplace, hosting
  `marathon`.
- [`go-libraries`](https://github.com/standards-lab/go-libraries) — the Go capability libraries: the base
  module of the library level.
- [`go-service-template`](https://github.com/standards-lab/go-service-template) — the service template
  baseline: the minimal runnable service new services are seeded from.
