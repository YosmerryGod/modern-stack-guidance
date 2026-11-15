# Frontend Engineering Skill

Build accessible, responsive, secure, maintainable interfaces using the project's existing framework and modern browser capabilities.

## Inspect first
Check framework/package versions, routing, rendering strategy, styling system, design tokens, component conventions, and supported browsers.

## HTML and accessibility
- Use semantic HTML for meaning, not appearance.
- Ensure controls have accessible names, visible focus, keyboard operation, and correct states.
- Associate labels and validation errors with form controls.
- Never communicate state through color alone; respect reduced-motion preferences.
- Prefer native semantics; use ARIA only when HTML cannot express the required behavior.

## CSS and responsive design
- Prefer layouts that adapt to available space; use container queries for component-level adaptation when supported.
- Use Grid and Flexbox for primary layout; avoid brittle positioning.
- Reuse the existing design tokens and styling system.
- Avoid global leakage, specificity escalation, and duplicated declarations.
- Check target-browser support before adopting cutting-edge features.

## JavaScript and browser APIs
- Prefer mature native browser APIs when they satisfy the requirement.
- Avoid blocking the main thread with expensive synchronous work.
- Model loading, empty, success, and error states explicitly.
- Clean up listeners, subscriptions, observers, and asynchronous work as required.
- Avoid unsafe HTML injection; sanitize rich HTML with a vetted sanitizer only when truly needed.

## React and Next.js
- Follow installed major versions and existing project conventions.
- Keep server/client boundaries explicit; keep secrets and privileged access server-side.
- Use stable keys and correct effect dependencies.
- Do not use effects for values that can be derived during render.
- Avoid premature memoization; profile or identify a concrete cost first.
- Validate route inputs and authorize protected operations on the server.
- Understand caching and invalidation before changing data-fetching behavior.

## Performance and validation
- Measure user-perceived performance; consider LCP, INP, and CLS.
- Reduce unnecessary JavaScript, image weight, layout shifts, and request waterfalls.
- Run lint, type-check, relevant component/flow tests, and production build when applicable.
- Check keyboard navigation, accessible names, and responsive layouts for changed interactions.

## Guardrails
Do not redesign unrelated UI, introduce dependencies for native capabilities, or claim browser compatibility without checking the target matrix.

Upstream reference: https://github.com/GoogleChrome/modern-web-guidance
