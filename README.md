# Solitaire Finz Mart — Website

Static site for Solitaire Finz Mart (DSA & Financial Advisory, Bhiwandi, Maharashtra).

## Pages

- `index.html` — Home page. Contains the Home view plus two embedded in-page tools:
  Legal Evaluation (`#legal`) and Technical Evaluation (`#technical`), switchable
  without a page reload.
- `legal.html` — Privacy Policy & Terms of Service.
- `admin.html` — Staff dashboard shell with a lightweight PIN gate and quick links
  into the two tools. **The PIN gate is client-side only and not secure** — see the
  note on the login screen. Replace it with real authentication (e.g. Supabase Auth)
  before using this for anything sensitive.

## Deploying with GitHub Pages

1. Push these files to a GitHub repository (root of the repo, or a `/docs` folder).
2. In the repo, go to **Settings → Pages**.
3. Under **Source**, choose the branch (e.g. `main`) and folder (`/root` or `/docs`).
4. Save — GitHub will publish the site at `https://<username>.github.io/<repo-name>/`.

No build step is required; these are plain static HTML files.

## Notes

- The Legal Evaluation and Technical Evaluation tools currently keep data in-browser
  for the session only (no backend), so reports aren't yet persisted or shared across
  devices. Wiring these to a shared backend (e.g. Supabase) would let the Admin
  dashboard show real application counts instead of placeholders.
- Before going live, change the PIN in `admin.html` (`ADMIN_PIN` near the bottom of
  the file) and treat it as a convenience gate, not a security boundary.
