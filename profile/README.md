# standards-lab

Platform-agnostic reference architectures for modern cloud-native enterprise development. The intent is to
incubate an inner-source ecosystem that drives digital modernization across the enterprise — reusable,
well-organized patterns teams adopt and build on, rather than re-deriving the same foundations project by
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
- **Libraries** — layered, independently versioned capability libraries, where the standard first
  materializes as code.
- **Service template** — a minimal runnable service that new services are seeded from.
- **Reference service** — a web service that composes the libraries and demonstrates each capability in
  place, grown in documented layers.

## Shipped

- [`claude-plugins`](https://github.com/standards-lab/claude-plugins) — the plugin marketplace, hosting
  `marathon`.
