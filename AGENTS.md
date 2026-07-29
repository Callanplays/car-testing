<!-- htsw:guides START -->
## HTSW + Housing guides for agents

These docs are managed by `htsw-docs sync`.

### Reference docs

- Housing (concepts, actions, conditions, variables, placeholders, house
  settings): start at `.htsw/housing/overview.md`.
- HTSW (HTSL syntax, actions, conditions, importables, tooling): start at
  `.htsw/htsw/overview.md`; the language reference is under
  `.htsw/htsw/htsl/` and the tooling guide is `.htsw/htsw/tooling.md`.
- How an HTSW project fits together (`import.json`, `.htsl`, `.snbt`, and
  `include`): `.htsw/agents/htsw-project-structure.md`.
- Common Housing patterns: `.htsw/agents/list-of-common-patterns.md`.

### HTSW tooling

The HTSW CLI (`htsw` command) should be available in the shell environment.
If it is not, ask the user to install it.

When writing, formatting, reviewing, or otherwise interacting with HTSW,
leverage the HTSW CLI to the fullest.

Make an attempt to test the code you write with `htsw run` unless that is
entirely inapplicable, in which case do not bend over backwards simply to
check the box of having "tested" the code.

Validate through `import.json`, normally `htsw check import.json` (or just
`htsw check`, which uses `./import.json`). Do not treat standalone
`.htsl` files as the validation target: they hold Housing Actions referenced
by an `import.json`, and `check` / `run` are built around
`import.json` / `*.import.json` entrypoints.

Testing will usually involve creating a temporary `.htsl` file specifically
to use as the `htsw:main` function in order to invoke other code. Ask the
user first unless there is already a clear precedent; they may request a
different testing procedure, or no tests at all.

When driving the live game (for example through the minecraft-mcp bridge),
imports can be queued and run in-game with the hidden `/htsw queue` command
family; see `.htsw/agents/htsw-import-queue.md`.

### Reading the docs

Many doc files have a table of contents (`<!--- TOC -->` ... `<!--- END -->`),
and each section covered by a TOC ends with a horizontal rule (`---`). Read
the TOC first and pull only the sections you need.
<!-- htsw:guides END -->
