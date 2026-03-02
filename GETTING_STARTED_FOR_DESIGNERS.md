## Getting started as a designer

This guide walks through a single, realistic scenario so you can see how to use these rules without reading everything at once.

### Scenario: improve a sign-up form

You’ve joined a project that already has a basic sign-up form. You want to make it clearer, more accessible, and friendlier without breaking anything.

1. **Open the form in Cursor**
   - Find the sign-up form component in your codebase (for example, `SignUpForm.tsx`) and open it in Cursor.
2. **Skim the “If you’re new or overwhelmed” section**
   - In this repo’s `README.md`, read the “If you’re new or overwhelmed” section to see which rules matter most at the start.
3. **Focus on three key rules**
   - Layout: `.cursor/rules/frontend/ui-layout-and-density.mdc`
   - Forms and validation: `.cursor/rules/frontend/ux-forms-and-validation.mdc`
   - Accessibility: `.cursor/rules/frontend/accessibility-frontend.mdc`
4. **Review the current form against those rules**
   - Check spacing and grouping of fields using `ui-layout-and-density.mdc`.
   - Check labels, error messages, and validation using `ux-forms-and-validation.mdc`.
   - Check keyboard navigation, focus states, and semantics using `accessibility-frontend.mdc`.
5. **Make one small improvement at a time**
   - Example changes:
     - Clarify a label (for example, “Email” → “Work email”).
     - Add inline error text that explains what to fix.
     - Ensure the submit button has a clear, action-based label (for example, “Create account”).
6. **Optionally refine copy**
   - If you want to improve microcopy, open `.cursor/rules/frontend/ux-writing-and-microcopy.mdc` and adjust messages to be clearer and more human.
7. **Repeat for other forms**
   - Once you’re comfortable with this flow, you can repeat the same steps for other forms and gradually explore more rules (flows, IA, research, experimentation) as your work requires them.

