# Hikari Co

Static marketing site for Hikari Co, founded by Benjamin Armstrong. It describes websites and Meta ads for Tulsa family-activity businesses.

The site is a single file, `index.html`, with CSS in the page. There is no image directory, no package manager, and no build step.

## Deploy from Git on Netlify

`netlify.toml` sets the publish directory to the repository root and leaves the build command unset, so Netlify copies the files as they are.

1. In Netlify, choose **Add new site** → **Import an existing project**.
2. Connect GitHub if it is not already connected, then select [zaddybnj/Hikari](https://github.com/zaddybnj/Hikari).
3. Use these build settings (they match `netlify.toml`):
   - **Build command:** leave empty
   - **Publish directory:** `.`
   - **Production branch:** `main`
4. Deploy. Netlify serves `index.html` at the site root.

After the repository is linked, pushes to `main` publish production and pull requests get deploy previews. No environment variables are required for this page.

Do not commit API tokens. The Netlify CLI stores link state in `.netlify/`, which is listed in `.gitignore`.

## Preview locally

From the repository root:

```bash
python3 -m http.server 8765
```

Open [http://127.0.0.1:8765/](http://127.0.0.1:8765/).

## Content to keep

- The contact section has no email address or phone number. Leave it that way until real contact details are provided.
- The example section is a set of unsolicited concept mocks. Keep the line: “Unsolicited concept mocks; not affiliated with or endorsed by these businesses.”
