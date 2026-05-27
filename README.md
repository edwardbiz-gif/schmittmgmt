# schmittmgmt-site

Tiny one-page corporate site for Schmitt Management. Exists to satisfy the
"company website" requirement on Salesmsg account completion and (later)
the A2P 10DLC brand registration.

## What's in here

- `index.html` — single self-contained page (no external assets). Includes
  the company overview plus the two compliance sections that 10DLC
  reviewers actively look for: SMS Communications Policy (opt-in language,
  STOP/HELP keywords, message frequency, "message and data rates may
  apply") and a Privacy Policy that specifically addresses SMS data
  handling.

## Deploy to GitHub Pages (one-time, ~3 minutes)

1. **Create a new public repo on GitHub** under your `edwardbiz-gif`
   account named `schmittmgmt`. Leave it empty (don't initialize with a
   README — we'll push these files).

2. **From this folder, push the contents:**

   ```powershell
   cd C:\Users\edwar\operations-system\schmittmgmt-site
   git init
   git add index.html README.md
   git commit -m "initial: corporate one-pager with SMS compliance sections"
   git branch -M main
   git remote add origin https://github.com/edwardbiz-gif/schmittmgmt.git
   git push -u origin main
   ```

3. **Enable Pages:** in the new repo on GitHub → Settings → Pages → Source:
   "Deploy from a branch" → Branch: `main`, folder: `/ (root)` → Save.

4. **Wait ~30 seconds** then open:

   ```
   https://edwardbiz-gif.github.io/schmittmgmt/
   ```

   That's the URL to paste into Salesmsg's "company website" field.

## Later: upgrade to a real domain

GitHub Pages on a github.io subdomain is acceptable for Salesmsg account
completion but slightly weakens the 10DLC brand application. Before
submitting the brand to Salesmsg, register a `.com` (e.g.,
`schmittmgmt.com` on Namecheap, ~$10/yr), add a `CNAME` file to this repo
with the domain, and point the DNS A records at GitHub's IPs. The same
HTML serves both URLs.

## Updates

To edit the page later, edit `index.html`, commit, push. GitHub Pages
republishes within ~30 seconds.
