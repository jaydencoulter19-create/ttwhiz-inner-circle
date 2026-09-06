# TikTok Wiz — Inner Circle (pitch page)

Single self-contained `index.html`. No build step, no dependencies.

## What each rep sees
- All edits (prices, column names, card text, layout) save to **their own browser** (localStorage). Nothing is shared between reps.
- When you push an update, reps automatically get the new default copy/numbers/columns for anything they **haven't** personally edited, and keep everything they **have** edited (3-way merge on load).

## Deploy on Replit
1. Create a Repl from this GitHub repo (or drag `index.html` into a new **HTML/CSS/JS** Repl).
2. Click **Deploy → Static**. Public directory: `.`
3. You get a `your-app.replit.app` URL. Add a custom domain under the deployment's **Domains** tab (point a CNAME from your DNS).

## Push updates
```bash
git add -A
git commit -m "Update copy/prices"
git push
```
Then hit **Redeploy** in Replit (or enable auto-deploy on push). Reps refresh and see the update while keeping their own edits.
