# Cursor Design Rules – UX, UI, IA, and Accessibility

This repo provides a **design-centric ruleset for Cursor** that helps the AI maintain high standards across UX, UI, information architecture, accessibility, and research-driven design.

Rules are curated by **Spencer Goldade (spencergoldade.ca)**.

## What you get

- A **tiered rules system** under `.cursor/rules/`:
  - **Always-on core** – tiny, cross-cutting design principles that apply to every interaction.
  - **Auto-attached zone rules** – focused rules that attach based on file globs (frontend, flows, IA, a11y, UX writing, research, testing).
  - **Agent-requested binders** – rich, cross-cutting guides for security UX, enterprise IA, cross-platform consistency, and experimentation.
- All rules are **design-system agnostic** and focus on **how to build**, not what features to build.

## File structure

Key files in `.cursor/rules/`:

- Always-on:
  - `design-core.mdc` – balanced UX, UI, IA, and accessibility principles.
  - `cursor-behavior-constraints.mdc` – what Cursor should and should not do during design work.
- Frontend and flows (auto-attached, example globs `**/*.tsx`):
  - `ui-layout-and-density.mdc`
  - `ui-components-and-states.mdc`
  - `ui-visual-language.mdc`
  - `ux-flows-and-feedback.mdc`
  - `ux-forms-and-validation.mdc`
  - `accessibility-frontend.mdc`
- IA, content, research, testing:
  - `ia-navigation-and-structure.mdc`
  - `ux-writing-and-microcopy.mdc`
  - `ux-research-usage.mdc`
  - `design-quality-testing.mdc`
- Agent-requested binders (no globs, pulled in when relevant):
  - `security-ux-patterns.mdc`
  - `enterprise-ia-patterns.mdc`
  - `cross-platform-ux-consistency.mdc`
  - `experimentation-and-metrics.mdc`

You can adjust or extend this list as your project evolves.

## How to add these rules to your project

1. **Copy the rules directory**
   - Copy the `.cursor/rules/` directory from this repo into the root of your project.
2. **Adjust file globs to match your stack**
   - Open each `.mdc` file that has a `globs` field (for example, `**/*.tsx`) and update it to match your file layout:
     - React / Next.js: `**/*.tsx`
     - Vue: `**/*.vue`
     - Svelte: `**/*.svelte`
     - Mixed monorepo: use patterns like `apps/*/src/**/*.tsx` or `packages/ui/**/*.tsx`.
3. **Hook rules to your design docs**
   - Create or connect design docs in your project (recommended locations):
     - `design/tokens/colors.*`
     - `design/tokens/typography.*`
     - `design/tokens/spacing.*`
     - `design/ia/navigation.*`
     - `design/content/voice-and-tone.*`
     - `design/research/*`
   - The rules tell Cursor to read these before making design decisions and to propose minimal templates if they do not exist.
4. **Restart or reload Cursor**
   - Once the `.cursor/rules/` directory is present, Cursor will automatically start applying these rules according to their frontmatter.

## How the tiers work

- **Always-on** (`alwaysApply: true`)
  - Loaded into every conversation.
  - Kept intentionally small; only truly universal design principles belong here.
- **Auto-attached** (`globs: ...`, `alwaysApply: false`)
  - Loaded only when you edit matching files (for example, frontend components).
  - This is where most of the UI/UX/IA/a11y detail lives.
- **Agent-requested**
  - No `globs`; Cursor pulls these in when it believes they are relevant based on their `description`.
  - Think of them as deep-dive binders for specialized topics.

## Adapting and extending

- Start by using this ruleset as-is, then:
  - Add project-specific examples and file references (for example, `client/src/hooks/useDataCache.ts`).
  - Tighten or relax rules based on your team’s maturity and domain.
  - Periodically review and prune rules—**stale rules are worse than none**.

If you share improvements or adaptations, please keep the original curation credit to **Spencer Goldade (spencergoldade.ca)** and add your own as co-curators.

