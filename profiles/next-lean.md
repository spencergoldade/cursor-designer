# Next.js app – lean product profile

Use this when you want the **lean product profile** in a Next.js (or similar React) app. It gives you core design principles plus the frontend rules that attach to component files.

## Rules to copy

From this repo into your project’s `.cursor/rules/`:

- `core/design-core.mdc`
- `core/cursor-behavior-constraints.mdc`
- `frontend/ui-layout-and-density.mdc`
- `frontend/ux-forms-and-validation.mdc`
- `frontend/accessibility-frontend.mdc`
- `frontend/ux-flows-and-feedback.mdc`

Ensure each frontend `.mdc` file has `globs: ["**/*.tsx"]` (or your app’s component paths, e.g. `["app/**/*.tsx", "components/**/*.tsx"]`).

## Design docs (optional)

Copy and customize into your project’s `design/` folder:

- `design/tokens/colors.example.md` → `design/tokens/colors.md`
- `design/tokens/typography.example.md` → `design/tokens/typography.md`
- `design/tokens/spacing.example.md` → `design/tokens/spacing.md`

Optionally: `design/ia/navigation.example.md` → `design/ia/navigation.md`, and `design/content/voice-and-tone.example.md` → `design/content/voice-and-tone.md`.

## Reference

For full profile definitions and “What to copy where”, see the main [README](../README.md) section “Profiles: core, lean, and full”.
