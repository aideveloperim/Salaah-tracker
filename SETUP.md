# Salaah Tracker — Setup & Deployment Notes

## Live URL

**https://aideveloperim.github.io/Salaah-tracker**

---

## GitHub Repository

**https://github.com/aideveloperim/Salaah-tracker**

---

## How to enable GitHub Pages (first time only)

1. Go to github.com/aideveloperim/Salaah-tracker
2. Click the **Settings** tab
3. Click **Pages** in the left sidebar
4. Under **Branch** → click the dropdown that says **None** → select **main**
5. Click **Save**
6. Wait 60 seconds then open the live URL above

---

## How to update the app after making changes

Run this in Terminal:

```bash
cd "/Users/imranmanjra/Library/Mobile Documents/com~apple~CloudDocs/Claude/Salah Tracker"
git add index.html
git commit -m "Update"
git push
```

GitHub Pages will update automatically within 60 seconds.

---

## Add to iPhone Home Screen

1. Open the live URL in Safari on your iPhone
2. Tap the **Share** icon (box with arrow)
3. Tap **Add to Home Screen**
4. Tap **Add**

---

## GitHub Personal Access Token

- Token name: Salaah-Tracker
- Expires: Sun 2 Aug 2026
- Stored securely — do not share

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The full app — prayers, dashboard, history |
| `SETUP.md` | This file |

---

## Netlify (no longer used)

The Netlify site was deleted. GitHub Pages is used instead — it is completely free with no credit limits.

---

## Troubleshooting: site stuck on an old version after pushing

If you push a change, wait well past 60 seconds, and the live site still shows the old version — this isn't just deploy lag. Check what GitHub actually did:

1. Go to github.com/aideveloperim/Salaah-tracker → **Actions** tab
2. Look at the most recent **"pages build and deployment"** run
3. If it shows a red ✗ (failed), the automatic deploy broke — retrying the same push won't fix it

**What happened on 3 Jul 2026:** GitHub's Pages hosting got stuck in a bad internal state for this site. Every deploy — including a brand new push — failed at the final publish step with `Deployment failed, try again later`. Re-running the failed job didn't help (it got stuck in a broken "queued" state that GitHub itself couldn't even cancel).

**The fix:** recreate the Pages site configuration from scratch (Settings → Pages → change branch to **None**, Save, then set it back to **main**, Save). This resets GitHub's internal record for the site without touching any code. The very next push deployed cleanly afterwards.

---

## Status

- GitHub Pages enabled on `main` branch ✓
- App loading on iPhone ✓
- Added to iPhone Home Screen ✓
