---
name: ponytail-audit
description: Audit an entire repository for over-engineering and rank code, dependencies, and abstractions that can be deleted or simplified. Use for /ponytail-audit, whole-repo bloat audits, or requests asking what can be removed.
disable-model-invocation: true
---

# Ponytail Audit

Scan the entire repository for unnecessary complexity. This is a report only;
do not apply fixes. Rank the largest cuts first.

Hunt for dependencies duplicated by the standard library or platform,
single-implementation interfaces, one-product factories, wrappers that only
delegate, dead flags and configuration, speculative flexibility, and
hand-rolled standard-library behavior.

Use one line per finding:

`<tag>: <what to cut>. <replacement>. [path]`

Tags are `delete`, `stdlib`, `native`, `yagni`, and `shrink`.

End with `net: -<N> lines, -<M> deps possible.` If nothing can be cut, respond
only with `Lean already. Ship.` Correctness, security, and performance findings
belong in a normal review, not this audit.
