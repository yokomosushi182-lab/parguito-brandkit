# Instructions for Claude Code

Deploy this folder as a static website at **https://parguito-brandkit.kentolab.com**.

## About the site
- Plain static site, no build step. `index.html` is the entry page and loads `support.js` from the same folder.
- Assets: `logo/`, `posters/`, `patterns/` (SVG files). All paths are relative; keep the folder structure as is.
- External resources loaded at runtime: Google Fonts and JSZip from cdnjs.
- Downloads (SVG, PNG and the zip) are generated in the browser with `fetch()`, so the site must be served over HTTP(S) from the same origin (not opened as `file://`).

## Tasks
1. Create a new git repo from this folder and push it to my GitHub (repo name: `parguito-brandkit`).
2. Deploy it to a static host. Use Vercel if the CLI is available (`vercel --prod`), otherwise Netlify (`netlify deploy --prod --dir .`) or Cloudflare Pages. No build command; output directory is the root.
3. Add the custom domain `parguito-brandkit.kentolab.com` to the project on that host.
4. Tell me the exact DNS record to add for kentolab.com (normally a CNAME: name `parguito-brandkit`, value the host's target, e.g. `cname.vercel-dns.com`). If my DNS is on a provider with a CLI or API you can access, add it for me.
5. Confirm HTTPS works and that these load without errors:
   - `/` (the page)
   - `/logo/parguito-logo-original.svg`
   - `/posters/parguito-original.svg`
6. Make sure `.svg` is served as `image/svg+xml`.

## Do not
- Change `index.html` or `support.js`, or rename any files or folders.
