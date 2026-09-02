---
name: ponytail-debt
description: Harvest ponytail comments into a debt ledger and flag shortcuts without upgrade triggers. Use for /ponytail-debt, Ponytail debt, shortcut inventories, or requests asking what Ponytail deferred.
disable-model-invocation: true
---

# Ponytail Debt

Search the repository for comment markers containing `ponytail:`, skipping
`.git`, dependency directories, and build output. Account for comment prefixes
used by the repository's languages.

Report one row per marker, grouped by file:

`<file>:<line> - <what was simplified>. ceiling: <limit>. upgrade: <trigger>.`

Tag a marker `no-trigger` if it names no ceiling, upgrade path, or trigger.

End with `<N> markers, <M> with no trigger.` If none exist, respond with
`No ponytail: debt. Clean ledger.` Read and report only unless the user asks to
persist the ledger.
