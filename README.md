# Academy Manager — Public Pages

This folder contains the **Privacy Policy** and **Support** pages required by the App Store, ready to host on GitHub Pages.

## Files

- `index.md` — landing page with links to the other two
- `privacy.md` — privacy policy
- `support.md` — support / FAQ page
- `_config.yml` — Jekyll config (uses GitHub's Cayman theme)
- `README.md` — this file (not published)

## One-time setup (10 minutes)

### 1. Replace the placeholder email

Open `privacy.md` and `support.md` and replace **`support@academymanager.app`** with the email address you actually want users to write to.

```bash
# from inside this folder
sed -i '' 's/support@academymanager.app/your-real-email@example.com/g' privacy.md support.md
```

### 2. Push to GitHub

```bash
cd /Users/hashimalmahmeed/claude/academymanager-site

git init
git add .
git commit -m "Initial pages"

# Create a new repo on github.com first (e.g. "academymanager-site"),
# then connect this folder to it:
git branch -M main
git remote add origin https://github.com/<your-username>/academymanager-site.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. On github.com, open your new repo → **Settings** → **Pages** (left sidebar)
2. **Source:** *Deploy from a branch*
3. **Branch:** `main` / `/(root)` → **Save**
4. Wait ~1 minute. GitHub shows the live URL at the top of the same page, e.g.:
   - `https://<your-username>.github.io/academymanager-site/`

### 4. Verify

Open these URLs in a browser — they must load (no 404):

- Landing: `https://<your-username>.github.io/academymanager-site/`
- Privacy: `https://<your-username>.github.io/academymanager-site/privacy.html`
- Support: `https://<your-username>.github.io/academymanager-site/support.html`

### 5. Use them in App Store Connect

- **App Information → Privacy Policy URL** → privacy URL
- **App Information → Support URL** → support URL

## Updating later

Edit any markdown file, commit, push. GitHub re-publishes within a minute.

```bash
git add privacy.md
git commit -m "Update privacy policy"
git push
```

When you make changes that affect what data you collect, also bump the **Effective date** at the top of `privacy.md`.
