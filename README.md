# SMNetworks

**Network Security · Infrastructure · AX/DX Consulting**

Official website for **SMNetworks Company**.

Technical Director: **magnox netnox**  
Specialties: Network Security, Xen / Hyper-V, Nutanix, enterprise infrastructure  
Clients & track record: Lotte Group, Shinhan, and other major Korean enterprise infrastructures  
Location: Quan 7, Ho Chi Minh City, Vietnam  
Since: 2008 (Korea–Vietnam enterprise infrastructure)

---

## Live Site

This repository is intended to be deployed on **Cloudflare Pages**.

- Static single-page application (`index.html` at repository root)
- No build step required
- Recommended Cloudflare Pages settings:
  - **Framework preset**: None
  - **Build command**: *(leave empty)*
  - **Build output directory**: `/` (or leave empty)
  - **Root directory**: `/`

After connecting the GitHub repository to Cloudflare Pages, every push to `main` will automatically publish the site.

---

## Project Structure

```
.
├── index.html          # Complete SPA (React + Tailwind, self-contained)
├── README.md           # This file (English)
├── README.ko.md        # Korean version
├── LICENSE             # MIT
└── .gitignore
```

> **Note**  
> The `.agents/` directory and `AGENTS.md` (if present locally) contain auxiliary AI coding helpers (e.g. luna-chat-coder).  
> They are **not** part of the website codebase, are listed in `.gitignore`, and must never be included in the published site or production artifacts.

---

## Technology

- Single-file React application (pre-bundled)
- Tailwind CSS (utility classes inlined)
- Fully static — works on any static host, optimized for Cloudflare Pages / CDN
- Multilingual content (Korean / English / Vietnamese) controlled inside the application
- Brand mark: **SMN** (header and footer)
- Years of experience (since 2008) calculated automatically at runtime

---

## Local Preview

Because the site is a single static HTML file:

```bash
# Python
python -m http.server 8080

# or Node
npx serve .
```

Then open `http://localhost:8080`.

---

## Cloudflare Deployment Checklist

1. Log in to [Cloudflare Dashboard](https://dash.cloudflare.com) → **Workers & Pages** → **Create** → **Pages** → Connect to Git.
2. Select the repository `raonwglobal/smn`.
3. Configure:
   - Production branch: `main`
   - Build command: *(empty)*
   - Build output directory: `/` or empty
4. Deploy.
5. (Optional) Attach a custom domain and enable Cloudflare SSL / CDN features.

No Node.js, no package.json, no build pipeline is required.  
The large self-contained `index.html` is intentionally designed for zero-config static hosting.

---

## Contact

- Email: [magnox@nate.com](mailto:magnox@nate.com)
- LinkedIn: [magnox-netnox](https://www.linkedin.com/in/magnox-netnox-a856443a)

---

## License

MIT — see [LICENSE](LICENSE).
