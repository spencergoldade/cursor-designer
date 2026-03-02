# Binders (agent-requested rules)

These rules have no `globs`; Cursor pulls them in when relevant based on their `description`. Use them when you need deep dives on specific topics.

| File | When to invoke |
|------|----------------|
| `design-quality-testing.mdc` | Reviewing a feature before release, writing test plans, or doing design/UX QA. |
| `ux-research-usage.mdc` | Interpreting research findings or connecting evidence to design decisions. |
| `experimentation-and-metrics.mdc` | Planning or evaluating A/B tests, experiments, or UX metrics. |
| `cross-platform-ux-consistency.mdc` | Aligning experiences across web, mobile, or other platforms. |
| `enterprise-ia-patterns.mdc` | Designing IA for multi-product, multi-tenant, or large enterprise environments. |
| `security-ux-patterns.mdc` | Working on auth, permissions, account recovery, or other security-sensitive UX. |

When `design/*` docs exist (e.g. `design/tokens/colors.md`, `design/ia/navigation.md`, `design/content/voice-and-tone.md`), follow them as the source of truth. These binders add process and advanced patterns; they do not replace core or frontend rules.
