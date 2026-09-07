# Standards Lab

Standards Lab is a blueprint for formalizing an effective, modern, agentic software architecture
strategy: how an organization defines architectures, standards, and principles for inner-source
enterprise development, proves them in worked examples, and develops them with a harness whose
programming standards and workflow integrations are part of the architecture itself. Clear
architectural principles and standards, broken down into appropriately layered boundaries,
optimize the utility of agentic workflows in creating well-structured software — the same
structure that keeps a system legible to people is what lets agents build it well.

Modern means the next generation of primitives for what software emits — the library, the
binary, the container image — not any one deployment venue. Each primitive is a modular
boundary: the artifact where maintenance is contained, vulnerabilities and technical debt are
mitigated, and a capability becomes reusable. Layered appropriately, the boundaries compose
into an ecosystem of reusable components: foundations are solved once and adopted rather than
re-derived project by project, and capacity shifts toward creating, innovating, and leading the
standard forward. The boundaries also keep ownership and change legible: lines of effort and
responsibility attach to tangible artifacts, and a small, deliberate dependency surface stays
pinned and current, so the organization drives change rather than reacts to it. Examples of the
patterns the ecosystem incubates:

- **Interoperable, domain-driven services.** Services scoped to a domain, composing across
  clear interfaces rather than accumulating into monoliths.
- **Data composition over rigid schema.** Data modeled for composition rather than locked into
  tightly coupled schema.
- **Software architecture above the transport layer.** An enterprise typically operationalizes
  the OSI model's lower layers well — building and configuring networks, VNETs, VLANs, and
  firewalls is settled practice — while holding the higher, data-driven layers to no comparable
  internal discipline, despite the commercial sector's mature standards for the software built
  on them. The blueprint establishes that discipline.

Standardization is emergent rather than decreed: a convention becomes a standard once working
code proves it, promoted to the lowest level at which it is generic. Each target standard is a
complete reference architecture declaring its own dependency line and deployment targets; an
architecture or standard intended for production use graduates to its own organization, whose
name carries the standard's identity — the outermost modular boundary, where a standard's
evolution finds its owner. The blueprint is informative, not prescriptive: the same arrangement
can serve any discipline that benefits from an agentic development workflow, and how others
structure their own architectures and standards is their own to decide.

## Organization Contents

- [Documentation](https://github.com/standards-lab/docs) — the landing zone: the canonical home
  for the Elemental Architecture, its standards, and its principles.
  - [Elemental Architecture](https://github.com/standards-lab/docs/blob/main/architecture.md)
    — the compositional elements a program is built from and the rules that bind them,
    independent of technology.
  - [Principles](https://github.com/standards-lab/docs/blob/main/principles/index.md) — the
    architecture's principles, which every standard enhances and never loosens.
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
- [`sqlate`](https://github.com/standards-lab/sqlate) — the SQL templating library: authored
  `.sql` files made dynamic and composable, with its own guide. A standalone library adjacent
  to Go Elemental, which its libraries consume.
