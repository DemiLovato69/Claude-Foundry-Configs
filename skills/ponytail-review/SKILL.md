---
name: ponytail-review
description: Review current changes exclusively for over-engineering and identify what can be deleted or replaced with standard-library or native features. Use for /ponytail-review, simplify review, or requests to find bloat in a diff.
disable-model-invocation: true
---

# Ponytail Review

Review the current changes for unnecessary complexity, not correctness. Do not
apply fixes.

Use one line per finding:

`<file>:L<line>: <tag>: <what to cut>. <replacement>.`

Tags:

- `delete`: dead code, unused flexibility, or speculative features.
- `stdlib`: hand-rolled behavior already in the standard library.
- `native`: code or a dependency duplicating a platform feature.
- `yagni`: an abstraction with one implementation, config nobody sets, or a layer with one caller.
- `shrink`: the same logic in fewer lines; show the shorter form.

End with `net: -<N> lines possible.` If nothing can be cut, respond only with
`Lean already. Ship.`

Do not flag the single small check Ponytail requires for non-trivial logic.
