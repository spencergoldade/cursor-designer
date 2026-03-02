## Navigation and IA (example)

Copy this file to `design/ia/navigation.md` in your project and customize. IA **principles** are in `.cursor/rules/core/design-core.mdc`; **implementation rules** (patterns, labeling) are in `.cursor/rules/frontend/ia-navigation-and-structure.mdc`.

- **Goal**: Capture a simple sitemap and naming conventions that match user mental models.

### Sitemap

- `Home` – Overview of key tasks and recent items.
- `Projects` – List of projects the user can browse and manage.
- `Team` – Manage teammates, invitations, and roles.
- `Billing` – Plans, invoices, and payment methods.
- `Settings` – Personal preferences and account-level settings.

### Guidelines

- Use **noun-based labels** in the present tense (for example, `Team`, not `Manage team`).
- Keep navigation depth to about **three levels or fewer**.
- Use the same label everywhere for the same concept (nav, headings, buttons).
- For deeper structures, add breadcrumbs like: `Projects / Acme Redesign / Assets`.

