# standards-lab

Platform-agnostic reference architectures for modern cloud-native enterprise development. The intent is to
incubate an inner-source ecosystem that drives digital modernization across the enterprise — reusable,
well-organized patterns teams adopt and build on, rather than re-deriving the same foundations project by
project. The standard is built and proven one priority at a time; each is a worked example for others to
follow.

## The standard

- The lowest practical level of abstraction, with no frameworks by default. Frameworks appear only as
  optional variants.
- Dependencies flow downward only; interfaces are defined where they're consumed.
- Independent, artifact-keyed releases per library and service, with cross-language symmetry as a
  first-class convention.
- Strict CQRS, RFC 9457 problem responses, a three-phase configuration lifecycle, and a layered service
  lifecycle that composes components through cold start, hot start, and graceful shutdown.
- A clear role boundary: the developer owns production source; the agent owns tests, documentation, and
  project-management artifacts.
- Naming is deliberate; consistency is a requirement, not a preference.

## Roadmap

- **Shared agent harness plugins** — flexible, layered, distributable Claude Code plugins that codify
  organizational processes. Shipped: the `marathon` workflow plugin.
- **Shared library design** — how to layer and design shared, versioned libraries, where the standard
  first materializes as code.
- **Web service domain design** — a reference domain demonstrating compositional data architecture and a
  CQRS-oriented API interface.

## Shipped

- [`claude-plugins`](https://github.com/standards-lab/claude-plugins) — the plugin marketplace, hosting
  `marathon`.
