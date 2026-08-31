# Standards Lab

Standards Lab is a blueprint for formalizing an effective, modern, agentic software architecture
strategy: how an organization defines architectures, standards, and principles for inner-source
enterprise development, proves them in worked examples, and develops them with a harness whose
programming standards and workflow integrations are part of the architecture itself. Clear
architectural principles and standards, broken down into appropriately layered boundaries,
optimize the utility of agentic workflows in creating well-structured software — the same
structure that keeps a system legible to people is what lets agents build it well.

Modern means the next generation of primitives for what software emits — the library, the
binary, the container image — not any one deployment venue. The intent is to incubate an
inner-source ecosystem of reusable, well-organized patterns teams adopt and build on rather
than re-deriving the same foundations project by project:

- **Interoperable, domain-driven services.** Services scoped to a domain, composing across
  clear interfaces rather than accumulating into monoliths.
- **Data composition over rigid schema.** Data modeled for composition rather than locked into
  tightly coupled schema.
- **Software architecture above the transport layer.** The OSI model's lower layers are
  governed by mature standards — building and configuring networks, VNETs, VLANs, and firewalls
  is commodity practice. No comparable discipline governs the software built on the protocols
  above them; this effort defines one.

Each target standard is a complete reference architecture declaring its own dependency line and
deployment targets; an architecture or standard intended for production use graduates to its
own organization, whose name carries the standard's identity.

## Organization Contents

- [Documentation](https://github.com/standards-lab/docs) — the landing zone: the canonical home
  for the organization's architectures, standards, and principles.
  - [Elemental Architecture](https://github.com/standards-lab/docs/blob/main/architectures/elemental-architecture/index.md)
    — the compositional elements a program is built from and the rules that bind them,
    independent of technology.
  - [Principles](https://github.com/standards-lab/docs/blob/main/principles/index.md) — the
    organizational principles every standard enhances and never loosens.
- [Harness](https://github.com/standards-lab/claude-plugins) — `claude-plugins`, the plugin
  marketplace codifying the organization's development processes: the `marathon` workflow and
  its `marathon-roadmap` extension.
- [Go Elemental](https://github.com/standards-lab/docs/blob/main/standards/go-elemental/index.md)
  — the Go implementation of the Elemental Architecture on the standard library, the
  organization's first standard.
  - [`go-core`](https://github.com/standards-lab/go-core) — the Core SDK: layered
    configuration, the process lifecycle, and the logger.
  - [`go-database`](https://github.com/standards-lab/go-database) — the SQL infrastructure
    library, with the PostgreSQL provider as a sub-module.
  - [`go-web-sdk`](https://github.com/standards-lab/go-web-sdk) — the Application SDK for web
    services.
  - [`go-web-sdk-template`](https://github.com/standards-lab/go-web-sdk-template) — scaffolds
    an initial Go Elemental web service with `gonew`.
  - [`go-web-service`](https://github.com/standards-lab/go-web-service) — the holistic
    reference web service, grown in documented layers; versionless until its 1.0.
