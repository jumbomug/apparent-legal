# apparent-legal

Public legal and support pages for the Apparent Family iOS app, served by
GitHub Pages at https://apparentfamily.com (custom domain since 2026-10-18;
the old jumbomug.github.io/apparent-legal/ addresses redirect here, and every
build before the move links to them).

- `/`: support page (App Store "Support URL")
- `/privacy.html`: privacy policy (App Store "Privacy Policy URL"), rendered from
  the app repo's `docs/legal/PRIVACY_POLICY.md` by `npm run legal:render`
- `/privacy/`: forwards to `/privacy.html`
- `/age-suitability.html`: age suitability statement

The source of truth for the policy lives in the app repo; change it there,
re-render, push here, then run `npm run legal:hosted` in the app repo.
