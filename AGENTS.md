<!-- htsw:guides START -->
## HTSW + Housing docs

These docs are managed by `htsw-docs sync`.

Before working on any HTSW or Housing task, read the relevant documentation
linked below and use it as the source of truth.

Use the Housing concept docs for game behavior, the HTSW reference for syntax
and formats, and the agent workflows for validation and live imports.

### Overview

Hypixel Housing is a gamemode on the Hypixel Network. Each player is given a
 plot to build on, expand, create games, and more. Almost anything is possible!
 Player's can also visit other people's houses and see what creations they've
 made.

The basis of Hypixel Housing are player houses. Players can create houses and
 open them to the public for others to join.

Hypixel Housing allows clients of both 1.8.9 and 1.21 to join. Internally, the
 servers run a heavily modified version of the 1.8.9 Minecraft server software.
 This means that most features of newer Minecraft versions are inaccessible in
 Housing.

HTSW is a near zero-abstraction framework and collection of formats for
 representing Housing entities as text. It consists of two main formats:
 `import.json` and HTSL.

HTSL (Housing Text Scripting Language) is the markup language used by HTSW to
 represent Housing actions in a textual format.

### Documentation

#### Housing concepts

- Actions and action containers: `.htsw/housing/actions.md`
- Conditions: `.htsw/housing/conditions.md`
- Functions: `.htsw/housing/functions.md`
- Houses: `.htsw/housing/house.md`
- Regions: `.htsw/housing/regions.md`
- Systems: `.htsw/housing/systems.md`
- Variables: `.htsw/housing/variables.md`

#### HTSW reference

- Importables: `.htsw/htsw/importables.md`
- Tooling and CLI: `.htsw/htsw/tooling.md`
- Basic syntax: `.htsw/htsw/htsl/basic-syntax.md`
- Actions: `.htsw/htsw/htsl/actions.md`
- Conditions: `.htsw/htsw/htsl/conditions.md`

#### Agent workflows

- Project structure and validation: `.htsw/agents/htsw-project-structure.md`
- Live import queue: `.htsw/agents/htsw-import-queue.md`
- Common Housing patterns: `.htsw/agents/list-of-common-patterns.md`

#### Essential commands

- Validate the entry `import.json` or `*.import.json` with `htsw check`.
- Use `htsw run` for local simulation.
- Follow the live import queue guide when in-game tools are available.
<!-- htsw:guides END -->
