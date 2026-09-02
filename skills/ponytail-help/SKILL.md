---
name: ponytail-help
description: Display a concise reference for the Ponytail skills available in Claude Code. Use for /ponytail-help, Ponytail help, or questions about Ponytail commands and modes.
disable-model-invocation: true
---

# Ponytail Help

Display this reference without changing files or claiming to persist a mode:

| Skill | Purpose |
|---|---|
| `/ponytail-lite` | Build the requested scope and name a lazier alternative. |
| `/ponytail` | Enforce YAGNI, standard library, native features, then minimum code. |
| `/ponytail-ultra` | Prefer deletion and challenge unnecessary requirements. |
| `/ponytail-review` | Review the current changes only for over-engineering. |
| `/ponytail-audit` | Audit the entire repository for removable complexity. |
| `/ponytail-debt` | Inventory `ponytail:` shortcuts and upgrade triggers. |
| `/ponytail-help` | Show this card. |

Claude Code skills apply when invoked or selected by the model. They do not
persist a global intensity setting across messages. Invoke the desired intensity
again when starting a new thread.
