# Migaki Co

Static site for Migaki Co, founded by Benjamin Armstrong. The studio offers websites and Meta ads for local businesses. The GitHub repository and Netlify project names are unchanged.

There is no package manager and no build step. Netlify publishes the repository root as-is.

## Pages

- `/` — studio homepage: positioning, web design and Meta ads, concept work, approach, and a contact call to action. No prices are published.
- `/packages/` — a project plus a monthly retainer, the scope, and a custom-quote call to action. No prices are published.
- `/contact/` — how to request a free homepage mock. Email and phone are not listed.
- `/services` and `/services/` — Netlify redirects these to `/packages/`. The local static server does not apply that redirect.

## Deploy from Git on Netlify

`netlify.toml` sets the publish directory to the repository root and leaves the build command unset.

1. In Netlify, import [zaddybnj/Hikari](https://github.com/zaddybnj/Hikari).
2. Use these build settings:
   - **Build command:** leave empty
   - **Publish directory:** `.`
   - **Production branch:** `main`
3. Pushes to `main` publish production. Pull requests can create preview deploys through the existing Netlify link.

No environment variables are required. Do not commit API tokens. The Netlify CLI stores link state in `.netlify/`, which is listed in `.gitignore`.

Site visibility, access control, domains, and billing are managed in Netlify and are outside this repository.

## Preview locally

From the repository root:

```bash
python3 -m http.server 8765
```

Open [http://127.0.0.1:8765/](http://127.0.0.1:8765/), [http://127.0.0.1:8765/packages/](http://127.0.0.1:8765/packages/), and [http://127.0.0.1:8765/contact/](http://127.0.0.1:8765/contact/).

## Content to keep

- The contact pages do not list an email address or phone number. Leave them that way until real contact details are provided.
- The work section is unsolicited concept work. Keep it labeled as such. These mocks are not client case studies or endorsements.
