# Cursor Design Rules – UX, UI, IA, and Accessibility

This repo provides a **design-first Cursor rules template** that helps the AI maintain high standards across UX, UI, information architecture, accessibility, and research-driven design in any web app stack.

Rules are curated by **Spencer Goldade ([spencergoldade.ca](https://spencergoldade.ca))**.

[![Support on Ko-fi](https://img.shields.io/badge/Ko--fi-Support%20this%20project-FF5E5B?style=flat-square&logo=ko-fi&logoColor=white)](https://ko-fi.com/spencerg1350)

**Support this project on [Ko-fi](https://ko-fi.com/spencerg1350)!**

## Table of Contents

- [If you are new or overwhelmed](#if-you-are-new-or-overwhelmed)
- [What this repo is (and is not)](#what-this-repo-is-and-is-not)
- [Rule categories and how they apply](#rule-categories-and-how-they-apply)
- [Quickstart: add these rules to your project](#quickstart-add-these-rules-to-your-project)
- [Profiles: core, lean, and full](#profiles-core-lean-and-full)
- [Minimal setup for your first project](#minimal-setup-for-your-first-project)
- [How the tiers work](#how-the-tiers-work)
- [Example: how these rules change a simple form](#example-how-these-rules-change-a-simple-form)
- [Adapting and extending](#adapting-and-extending)
- [Using this with other rule libraries](#using-this-with-other-rule-libraries)
- [License and attribution](#license-and-attribution)

## If you are new or overwhelmed

- **You only need a few rules to start.** Begin with:
  - **Always-on core**:
    - [.cursor/rules/core/design-core.mdc](.cursor/rules/core/design-core.mdc) – a tiny set of UX, UI, IA, and accessibility principles.
    - [.cursor/rules/core/cursor-behavior-constraints.mdc](.cursor/rules/core/cursor-behavior-constraints.mdc) – what Cursor must and must not do during design work.
  - **Frontend basics** (lean product profile):
    - [.cursor/rules/frontend/ui-layout-and-density.mdc](.cursor/rules/frontend/ui-layout-and-density.mdc) – spacing and layout.
    - [.cursor/rules/frontend/ux-forms-and-validation.mdc](.cursor/rules/frontend/ux-forms-and-validation.mdc) – forms and errors.
    - [.cursor/rules/frontend/accessibility-frontend.mdc](.cursor/rules/frontend/accessibility-frontend.mdc) – keyboard and screen-reader basics.
    - [.cursor/rules/frontend/ux-flows-and-feedback.mdc](.cursor/rules/frontend/ux-flows-and-feedback.mdc) – flows, feedback, and state.
- **Everything else is optional at first.** You can add more rules later as your project and comfort level grow.
- For a step-by-step example, see [Getting started for designers](GETTING_STARTED_FOR_DESIGNERS.md).

## What this repo is (and is not)

- **Is**: A drop-in **design and UX guardrail** for Cursor.
  - Keeps Cursor honest on UX, IA, accessibility, and research practices.
  - Works alongside other rule libraries that focus on code style, agent workflows, or specific languages.
- **Is not**: A replacement for framework- or language-specific rules.
  - You can pair this with code-focused rule repos (for example, TypeScript or agentic rules) without conflict.

Compared to more code/agent-centric libraries (such as `sparesparrow/cursor-rules`), this repo focuses on:

- UX, UI, IA, and accessibility patterns that apply across stacks.
- Content, research, experimentation, and design QA guidance.

## Rule categories and how they apply

All rules live under `.cursor/rules/` (including subfolders) and use Cursor’s modern rule system:

- **Always-on core** – tiny, cross-cutting design principles that apply to every interaction.
  - [.cursor/rules/core/design-core.mdc](.cursor/rules/core/design-core.mdc) – balanced UX, UI, IA, and accessibility principles.
  - [.cursor/rules/core/cursor-behavior-constraints.mdc](.cursor/rules/core/cursor-behavior-constraints.mdc) – what Cursor should and should not do during design work.
- **Auto-attached frontend and flows** – focused rules that attach based on file globs (for example, `["**/*.tsx"]`):
  - Layout and components: [.cursor/rules/frontend/ui-layout-and-density.mdc](.cursor/rules/frontend/ui-layout-and-density.mdc), [.cursor/rules/frontend/ui-components-and-states.mdc](.cursor/rules/frontend/ui-components-and-states.mdc), [.cursor/rules/frontend/ui-visual-language.mdc](.cursor/rules/frontend/ui-visual-language.mdc).
  - Flows, forms, and a11y: [.cursor/rules/frontend/ux-flows-and-feedback.mdc](.cursor/rules/frontend/ux-flows-and-feedback.mdc), [.cursor/rules/frontend/ux-forms-and-validation.mdc](.cursor/rules/frontend/ux-forms-and-validation.mdc), [.cursor/rules/frontend/accessibility-frontend.mdc](.cursor/rules/frontend/accessibility-frontend.mdc).
  - IA and content: [.cursor/rules/frontend/ia-navigation-and-structure.mdc](.cursor/rules/frontend/ia-navigation-and-structure.mdc), [.cursor/rules/frontend/ux-writing-and-microcopy.mdc](.cursor/rules/frontend/ux-writing-and-microcopy.mdc).
- **Agent-requested binders** – deep-dive guides Cursor pulls in when relevant (no globs):
  - Security and enterprise: [.cursor/rules/binders/security-ux-patterns.mdc](.cursor/rules/binders/security-ux-patterns.mdc), [.cursor/rules/binders/enterprise-ia-patterns.mdc](.cursor/rules/binders/enterprise-ia-patterns.mdc).
  - Cross-platform and experimentation: [.cursor/rules/binders/cross-platform-ux-consistency.mdc](.cursor/rules/binders/cross-platform-ux-consistency.mdc), [.cursor/rules/binders/experimentation-and-metrics.mdc](.cursor/rules/binders/experimentation-and-metrics.mdc).
  - Research and QA: [.cursor/rules/binders/ux-research-usage.mdc](.cursor/rules/binders/ux-research-usage.mdc), [.cursor/rules/binders/design-quality-testing.mdc](.cursor/rules/binders/design-quality-testing.mdc).

For **core, lean, and full profiles** and a **"What to copy where"** table, see the [Profiles: core, lean, and full](#profiles-core-lean-and-full) section under Quickstart.

### Which rules to use for what

- **Adjusting spacing or layout**:
  - Use [.cursor/rules/frontend/ui-layout-and-density.mdc](.cursor/rules/frontend/ui-layout-and-density.mdc).
- **Designing or refining forms**:
  - Use [.cursor/rules/frontend/ux-forms-and-validation.mdc](.cursor/rules/frontend/ux-forms-and-validation.mdc) and [.cursor/rules/frontend/accessibility-frontend.mdc](.cursor/rules/frontend/accessibility-frontend.mdc).
- **Writing or improving copy and messages**:
  - Use [.cursor/rules/frontend/ux-writing-and-microcopy.mdc](.cursor/rules/frontend/ux-writing-and-microcopy.mdc).
- **Working on navigation or IA**:
  - Use [.cursor/rules/frontend/ia-navigation-and-structure.mdc](.cursor/rules/frontend/ia-navigation-and-structure.mdc).
- **Planning research or using findings**:
  - Use [.cursor/rules/binders/ux-research-usage.mdc](.cursor/rules/binders/ux-research-usage.mdc).
- **Running experiments or A/B tests**:
  - Use [.cursor/rules/binders/experimentation-and-metrics.mdc](.cursor/rules/binders/experimentation-and-metrics.mdc).
- **Enterprise structures, security, and cross-platform UX**:
  - Use [.cursor/rules/binders/enterprise-ia-patterns.mdc](.cursor/rules/binders/enterprise-ia-patterns.mdc), [.cursor/rules/binders/security-ux-patterns.mdc](.cursor/rules/binders/security-ux-patterns.mdc), and [.cursor/rules/binders/cross-platform-ux-consistency.mdc](.cursor/rules/binders/cross-platform-ux-consistency.mdc) when you hit those needs.

You can adjust or extend this list as your project evolves.

### Binder index (when to use each)

| Binder | When to invoke |
|--------|----------------|
| [design-quality-testing.mdc](.cursor/rules/binders/design-quality-testing.mdc) | Reviewing a feature before release, writing test plans, or doing design/UX QA. |
| [ux-research-usage.mdc](.cursor/rules/binders/ux-research-usage.mdc) | Interpreting research findings or connecting evidence to design decisions. |
| [experimentation-and-metrics.mdc](.cursor/rules/binders/experimentation-and-metrics.mdc) | Planning or evaluating A/B tests, experiments, or UX metrics. |
| [cross-platform-ux-consistency.mdc](.cursor/rules/binders/cross-platform-ux-consistency.mdc) | Aligning experiences across web, mobile, or other platforms. |
| [enterprise-ia-patterns.mdc](.cursor/rules/binders/enterprise-ia-patterns.mdc) | Designing IA for multi-product, multi-tenant, or large enterprise environments. |
| [security-ux-patterns.mdc](.cursor/rules/binders/security-ux-patterns.mdc) | Working on auth, permissions, account recovery, or other security-sensitive UX. |

Binders assume your project may have `design/*` docs (e.g. [design/tokens/colors.example.md](design/tokens/colors.example.md), [design/ia/navigation.example.md](design/ia/navigation.example.md), [design/content/voice-and-tone.example.md](design/content/voice-and-tone.example.md)). They focus on process and advanced patterns; core principles and frontend rules stay in `.cursor/rules/core/*` and `.cursor/rules/frontend/*`.

## Quickstart: add these rules to your project

1. **Choose a profile**
   - For most teams, start with the **lean product profile** (core + a small set of frontend rules).
   - For teaching, audits, or very mature teams, you can jump straight to the **full design-ops profile**.
2. **Copy the rules directory**
   - Copy the `.cursor/rules/` directory from this repo into the root of your project.
   - If you only want a subset, copy just the files for the profile you chose.
3. **Adjust file globs to match your stack**
   - Open each `.mdc` file that has a `globs` field (for example, `["**/*.tsx"]`) and update it to match your file layout:
     - React / Next.js: `["**/*.tsx"]`
     - Vue: `["**/*.vue"]`
     - Svelte: `["**/*.svelte"]`
     - Mixed monorepo: patterns like `["apps/*/src/**/*.tsx", "packages/ui/**/*.tsx"]`.
4. **(Optional) Hook rules to your design docs**
   - Create or connect design docs in your project (recommended locations):
     - `design/tokens/colors.*`
     - `design/tokens/typography.*`
     - `design/tokens/spacing.*`
     - `design/ia/navigation.*`
     - `design/content/voice-and-tone.*`
     - `design/research/*`
   - You can also copy and adapt the `.example` files under `design/` from this repo as a starting point.
5. **Restart or reload Cursor**
   - Once the `.cursor/rules/` directory is present, Cursor will automatically start applying these rules according to their frontmatter.

### Profiles: core, lean, and full

This section is the single, authoritative description of how to adopt these rules. It supersedes any older “minimal vs full profiles” wording elsewhere in this file.

- **Core profile (always-on foundation)**:
  - [.cursor/rules/core/design-core.mdc](.cursor/rules/core/design-core.mdc)
  - [.cursor/rules/core/cursor-behavior-constraints.mdc](.cursor/rules/core/cursor-behavior-constraints.mdc)
- **Lean product profile (recommended starting point for most web apps)**:
  - All **core profile** rules, plus:
  - [.cursor/rules/frontend/ui-layout-and-density.mdc](.cursor/rules/frontend/ui-layout-and-density.mdc)
  - [.cursor/rules/frontend/ux-forms-and-validation.mdc](.cursor/rules/frontend/ux-forms-and-validation.mdc)
  - [.cursor/rules/frontend/accessibility-frontend.mdc](.cursor/rules/frontend/accessibility-frontend.mdc)
  - [.cursor/rules/frontend/ux-flows-and-feedback.mdc](.cursor/rules/frontend/ux-flows-and-feedback.mdc)
- **Full design-ops profile (mature teams, teaching, and audits)**:
  - All rules under `.cursor/rules/**` (core, frontend, and binders).

#### What to copy where

When wiring this into a host app:

| Source in this repo                                   | Where it lives in your project     | Notes                                              |
| ----------------------------------------------------- | ----------------------------------- | -------------------------------------------------- |
| `.cursor/rules/core/*`                               | `.cursor/rules/core/*`             | **Always copy** – core design principles.          |
| `.cursor/rules/frontend/*`                           | `.cursor/rules/frontend/*`         | Copy the files for the profile you choose.         |
| `.cursor/rules/binders/*`                            | `.cursor/rules/binders/*`          | Optional deep dives; add when you hit those needs. |
| `design/tokens/*.example.md`                         | `design/tokens/*.md`               | Copy, drop `.example`, then customize.             |
| `design/ia/navigation.example.md`                    | `design/ia/navigation.md`          | Copy and adapt to your product’s IA.               |
| `design/content/voice-and-tone.example.md`           | `design/content/voice-and-tone.md` | Copy and define your brand voice.                  |
| `design/research/findings.example.md` (and siblings) | `design/research/*.md`             | Copy and use as a research log template.           |

#### Profile examples

**Example: Next.js app (lean product profile)**  
Copy the **lean product profile** rules (core + four frontend rules). Optionally add design docs:

- Rules: `core/design-core.mdc`, `core/cursor-behavior-constraints.mdc`, `frontend/ui-layout-and-density.mdc`, `frontend/ux-forms-and-validation.mdc`, `frontend/accessibility-frontend.mdc`, `frontend/ux-flows-and-feedback.mdc`.
- Design (optional): copy [design/tokens/colors.example.md](design/tokens/colors.example.md), [design/tokens/typography.example.md](design/tokens/typography.example.md), [design/tokens/spacing.example.md](design/tokens/spacing.example.md) to your project as `design/tokens/*.md` and customize. Set frontend rule `globs` to `["**/*.tsx"]` (or your app’s component paths).

See [profiles/next-lean.md](profiles/next-lean.md) for a file list you can copy from.

**Example: Design-only workshop**  
No frontend code; focus on principles and design docs only.

- Rules: only **core profile** – `core/design-core.mdc`, `core/cursor-behavior-constraints.mdc`.
- Design: copy [design/tokens/colors.example.md](design/tokens/colors.example.md), [design/tokens/typography.example.md](design/tokens/typography.example.md), [design/tokens/spacing.example.md](design/tokens/spacing.example.md), [design/ia/navigation.example.md](design/ia/navigation.example.md), [design/content/voice-and-tone.example.md](design/content/voice-and-tone.example.md) (and optionally [design/research/findings.example.md](design/research/findings.example.md)) into your project's `design/` folder and rename/customize.

See [profiles/design-only.md](profiles/design-only.md) for a file list.

### Minimal setup for your first project

If you want a very small starting point:

1. Copy these templates into your project and rename them (for example, remove `.example`):
   - [design/tokens/colors.example.md](design/tokens/colors.example.md)
   - [design/tokens/typography.example.md](design/tokens/typography.example.md)
   - [design/tokens/spacing.example.md](design/tokens/spacing.example.md)
2. Adjust **only**:
   - Your color palette.
   - Your base typography size and font family.
3. Leave the spacing scale as-is to begin with; you can refine it later as your design system matures.

## How the tiers work

- **Always-on** (`alwaysApply: true`)
  - Loaded into every conversation.
  - Kept intentionally small; only truly universal design principles belong here.
- **Auto-attached** (`globs: [...]`, `alwaysApply: false`)
  - Loaded only when you edit matching files (for example, frontend components).
  - This is where most of the UI/UX/IA/a11y detail lives.
- **Agent-requested**
  - No `globs`; Cursor pulls these in when it believes they are relevant based on their `description`.
  - Think of them as deep-dive binders for specialized topics such as security UX or enterprise IA.

## Example: how these rules change a simple form

Without these rules, a sign-up form might look like:

```tsx
// Before: minimal validation and weak messaging
<form>
  <label>Email</label>
  <input type="email" />
  <button>Submit</button>
</form>
```

With `ux-forms-and-validation.mdc`, `accessibility-frontend.mdc`, and `ux-writing-and-microcopy.mdc`, Cursor is guided toward something closer to:

```tsx
// After: clearer labels, inline validation, accessible structure
<form aria-describedby="signup-help">
  <p id="signup-help">Create an account to save your work and access it on any device.</p>

  <label htmlFor="email">Work email</label>
  <input
    id="email"
    type="email"
    aria-invalid={hasEmailError}
    aria-describedby={hasEmailError ? "email-error" : undefined}
  />
  {hasEmailError && (
    <p id="email-error" role="alert">
      Use a valid email address like name@company.com.
    </p>
  )}

  <button type="submit">Create account</button>
</form>
```

The exact implementation will vary by project, but the rules push Cursor toward:

- Clear, action-based labels.
- Inline, human-readable error messages.
- Keyboard- and screen-reader-friendly structure.

## Adapting and extending

- Start by using this ruleset as-is, then:
  - Add project-specific examples and file references (for example, `client/src/hooks/useDataCache.ts`).
  - Tighten or relax rules based on your team’s maturity and domain.
  - Periodically review and prune rules—**stale rules are worse than none**.
- To extend the rules safely:
  - Prefer updating existing `.mdc` files with project-specific notes over creating many overlapping files.
  - Keep always-on rules minimal and move detailed guidance into auto-attached or agent-requested binders.

If you share improvements or adaptations, please keep the original curation credit to **Spencer Goldade ([spencergoldade.ca](https://spencergoldade.ca))** and add your own as co-curators.

## Using this with other rule libraries

You can safely combine this design-first ruleset with other Cursor rule libraries (for example, ones focused on TypeScript, agent workflows, or security).

- **Directory layout example**
  - Design rules (this repo): `.cursor/rules/core/*`, `.cursor/rules/frontend/*`, `.cursor/rules/binders/*`.
  - Code and agent rules (another repo): `.cursor/rules/code/*`, `.cursor/rules/agents/*`, etc.
- **How they interact**
  - Cursor loads rules from all `.cursor/rules/**/*.mdc` files.
  - When guidance overlaps, the model sees both; keep each rule focused (design vs code) to reduce conflicts.
- **Tips**
  - Let this repo own UX, UI, IA, accessibility, and research patterns.
  - Let other libraries own language/framework specifics (for example, TypeScript style, API patterns, agent orchestration).
  - If you add project-specific rules, follow the authoring checklist in [.cursor/rules/binders/design-quality-testing.mdc](.cursor/rules/binders/design-quality-testing.mdc) and use clear file names like `project-<domain>.mdc`.

### Optional lean profile for teaching

For workshops or very small projects, you can start with a **lean profile**:

- Copy only the **lean product profile** rules into `.cursor/rules` (core + four frontend basics).
- Keep this repo nearby as a reference for when you are ready to add more rules or binders.
- See [LEAN_PROFILE_NOTES.md](LEAN_PROFILE_NOTES.md) for a short, implementation-focused checklist that points back to the profiles in this README.

## License and attribution

This project is licensed under the terms of the **GPLv3** license. See the [LICENSE](LICENSE) file for details.

In plain language:

- You can copy, modify, and redistribute these rules.
- If you redistribute a modified version of this repo or ship it as part of a public project, you must keep the same license terms and preserve attribution.

For private or internal projects, you can generally copy these rules into your repo as long as you respect the GPLv3 terms. Consult your own legal counsel if you are unsure how GPLv3 applies to your use case.

When adapting these rules, please retain credit to **Spencer Goldade ([spencergoldade.ca](https://spencergoldade.ca))** and add your own names as co-curators where appropriate. If this has been useful, you can [support my work on Ko-fi](https://ko-fi.com/spencerg1350).
