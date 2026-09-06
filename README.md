# HADF Team Portal — Final Refined Edition

This folder is the recommended team distribution of the **Hackathon Agentic Development Framework (HADF)** portal.

## What is included

- `index.html` — interactive Learn + Event portal (self-contained CSS/JS/content)
- `handbook.html` — dedicated in-browser reader for the full canonical handbook
- `assets/HADF_MASTER_TEAM_HANDBOOK.pdf` — the complete 146-page source-of-truth PDF
- `manifest.webmanifest` + `sw.js` — install/offline support when served over HTTP/HTTPS
- `HADF_TEAM_PORTAL_FINAL_STANDALONE.html` — same portal file for direct local opening
- architecture/coverage/component documentation

## Best way to use it on PC + phone

### Option A — GitHub Pages (recommended for the team)
1. Create a GitHub repository, e.g. `hadf-team-portal`.
2. Extract this ZIP and upload/push the **contents of this folder** to the repository root.
3. GitHub → repository **Settings** → **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and `/ (root)`, then **Save**.
6. GitHub gives you a URL similar to `https://USERNAME.github.io/hadf-team-portal/`.
7. Share that one URL with the team. It works on PC, Android, iPhone and tablet.

Because the PDF is committed under `assets/`, the **Full Handbook** buttons open the actual canonical PDF from the same website.

### Option B — local network during practice/hackathon
From this folder on the host laptop:

```bash
python -m http.server 8080 --bind 0.0.0.0
```

On the laptop open `http://localhost:8080`.

To open on a phone connected to the same Wi-Fi:
1. On Windows run `ipconfig`.
2. Find the Wi-Fi adapter's IPv4 address, e.g. `192.168.0.105`.
3. On the phone open `http://192.168.0.105:8080`.
4. If Windows Firewall asks, allow Python on **Private networks**.

### Option C — direct local file
Double-click `HADF_TEAM_PORTAL_FINAL_STANDALONE.html` or `index.html`.
Most portal features work directly. For the most reliable PDF embedding, install/offline caching, and phone sharing, use Option A or B.

## Full handbook behavior
- **Read handbook in browser** opens `handbook.html`.
- **Open PDF directly** launches the browser/native PDF viewer.
- **Save PDF offline** saves the source PDF.
- On phones, native PDF viewing is recommended if inline embedding is cramped.

## Offline use
When hosted over HTTP/HTTPS, the service worker caches the portal and PDF after first successful load. Browser support and storage policies vary; keep the PDF downloaded locally as a fallback for event day.

## Recommended event setup
- Every member bookmarks the hosted portal URL.
- Every member also saves the PDF locally.
- One laptop keeps a local-network copy available as fallback.
- Do not make last-minute structural changes to the portal during the event.
