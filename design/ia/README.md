# Information architecture (IA) in this ruleset

IA guidance is split across a few places so that principles, implementation rules, and your product’s concrete decisions stay clear.

| Layer | Where it lives | Role |
| ----- |----------------|------|
| **Principles** | `.cursor/rules/core/design-core.mdc` | High-level IA principles (shallow hierarchies, stable nav, noun-based labels). Always-on. |
| **Implementation rules** | `.cursor/rules/frontend/ia-navigation-and-structure.mdc` | Frontend patterns for navigation, labeling, and structure when editing UI. |
| **Your sitemap and names** | `design/ia/navigation.md` (or `navigation.example.md` as template) | Your product’s sections, route groupings, and naming. Copy from `navigation.example.md` and customize. |
| **QA checks** | `.cursor/rules/binders/design-quality-testing.mdc` | Checklist to verify IA consistency before release; references the above. |

When in doubt: principles in core, implementation detail in the frontend rule, your concrete IA in `design/ia/navigation.*`.
