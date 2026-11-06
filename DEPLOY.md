# Deploy to parguito-brandkit.kentolab.com

1. Upload this whole folder to a static host (Netlify Drop, Vercel, Cloudflare Pages or GitHub Pages). `index.html` is the entry point.
2. In the host, add the custom domain `parguito-brandkit.kentolab.com`.
3. In your DNS for kentolab.com, add:
   - Type: CNAME
   - Name: parguito-brandkit
   - Value: the hostname your host gives you (e.g. `your-site.netlify.app`)
4. Wait for DNS to propagate and enable HTTPS (automatic on most hosts).
