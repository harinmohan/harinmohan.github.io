# Code 009 — Academic Portfolio

A multi-page academic portfolio starter for Dr. Harin M. Mohan.

## Included
- Six main tabs: Home, About, Research & Publications, Teaching & Outreach, Activities, Academic Calendar.
- Six-face continuously rotating photo cube on the Home page.
- Six research-area cards retained from the reference design.
- Structured content in `data/site-content.json`.
- Decap CMS admin scaffold in `/admin`.
- Google Calendar appointment link preconfigured.
- OpenAlex metrics workflow scaffold.
- Responsive navy / cyan / white visual system with restrained micro-interactions.

## Important before publishing
This is a deployable **starter package**, not a completed authenticated CMS deployment. The public pages can be hosted on GitHub Pages, but the admin CMS needs an OAuth service and configuration before login/publishing is secure. Do not put a GitHub token or OAuth client secret in browser files.

## Deploy public site
1. Back up your current `harinmohan.github.io` repository.
2. Upload the package contents to the repository root (do not upload the enclosing ZIP).
3. Keep GitHub Pages configured for `main` / root.
4. Add six personal photographs at:
   `assets/images/cube/photo-1.jpg` through `photo-6.jpg`.
   Use your own images; replace the six placeholder image references with matching files. Keep filenames lowercase and exact.
5. Test every page on desktop and mobile.

## Admin dashboard setup
The `/admin` folder contains Decap CMS and a GitHub backend configuration. Before enabling it:
1. Set up a trusted OAuth provider/service for Decap CMS.
2. Set `base_url` in `admin/config.yml` to that OAuth service.
3. Configure the OAuth application with the exact GitHub callback URL required by the selected service.
4. Restrict OAuth access to your GitHub account.
5. Keep client secrets and GitHub App private keys on the OAuth server only.
6. Test login, draft review and publishing before using the dashboard.

Do not deploy `/admin` as a working editor until OAuth is configured and tested. GitHub Pages is public hosting; a JavaScript password gate is not security.

## OpenAlex metrics
1. Identify and verify your OpenAlex author record.
2. In GitHub repository Settings → Secrets and variables → Actions → Variables, add `OPENALEX_AUTHOR_ID`.
3. Run the “Refresh OpenAlex metrics” workflow manually once.
4. Check `data/openalex-metrics.json` and confirm the author match before relying on the metrics.
The workflow refreshes weekly. Metrics are OpenAlex metrics, not Google Scholar metrics.

## Academic Calendar
The Google Calendar booking link is set to:
https://calendar.app.google/xx5qPjHzxkqibVWi7

To embed a calendar later, create a dedicated academic calendar, configure institutional sharing in Google Workspace, copy its embed URL, and update the Calendar Settings collection. Do not embed a personal calendar with private events. The booking link is independent of calendar embedding.

## Resume-derived content notes
Initial profile, education, work history, selected publications, award and patents were transcribed from the two-page resume supplied in the conversation. The PhD status is shown as awarded in 2026 based on the user's later correction. Verify all publication metadata, patent statuses/numbers and current designation before final public release. Resume had older phone/personal email details; these are intentionally not published. The site uses the user's previously supplied institutional contact email `harinmm@tkmce.ac.in`.

## Current known limitations
- Cube photo files are not included; upload six approved personal photographs.
- OpenAlex author ID has not yet been verified; metrics remain blank until configured.
- Academic Calendar embed is blank until a dedicated calendar embed URL is provided.
- Admin login is scaffolded but OAuth server setup is required.
- This package does not deploy itself or modify your GitHub repository.
