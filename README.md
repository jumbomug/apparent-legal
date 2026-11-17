# apparent-legal

The apparentfamily.com website: the marketing site, the support page and the
legal pages for the Apparent Family iOS app, served by GitHub Pages at
https://apparentfamily.com (custom domain since 2026-10-18; the old
jumbomug.github.io/apparent-legal/ addresses redirect here, and every build
before the move links to them).

- `/`: the marketing site's home page (App Store "Marketing URL"), with
  `/what-we-left-out`, `/press` and `/about`; built by the app repo's
  `website/` and copied here by `npm run site:stage`
- `/support`: support page (App Store "Support URL")
- `/privacy.html`: privacy policy (App Store "Privacy Policy URL"), rendered from
  the app repo's `docs/legal/PRIVACY_POLICY.md` by `npm run legal:render`
- `/privacy/`: forwards to `/privacy.html`
- `/terms.html`: Terms of Use, rendered the same way from `docs/legal/TERMS_OF_USE.md`
- `/age-suitability.html`: age suitability statement

The source of truth for every page lives in the app repo; change it there,
re-render or re-stage, push here, then run `npm run legal:hosted` in the app
repo. The stage script never writes the legal pages, `CNAME` or this file.
