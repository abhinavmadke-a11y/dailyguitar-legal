# dailyguitar-legal

Public legal documents for **Daily Guitar: Chords & Lessons**, the iOS and Android
guitar-learning app published by 999 Online Inc. (trading as 999 Venture Studio).

This repository exists so the documents have a stable, publicly reachable home. Apple and
Google both require a privacy policy URL that loads without a sign-in, and app store reviewers
check it during review.

## What's here

| File | Published at | Purpose |
| --- | --- | --- |
| `index.html` | the Pages URL below | Privacy policy for Daily Guitar |

## Live URL

https://abhinavmadke-a11y.github.io/dailyguitar-legal/

This URL is submitted to App Store Connect and Google Play Console. **Treat it as permanent.**
Renaming the repository, renaming `index.html`, making the repo private, or turning off Pages
will break the link, and a broken privacy policy URL is grounds for rejection or removal.

## How it's published

GitHub Pages, serving the repository root on the `main` branch. There is no build step and no
dependencies — `index.html` is a single self-contained file with its styles inline, so it works
on any host if this ever needs to move.

Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)`.

## Updating a document

1. Edit the file — either in the browser (open it, click the pencil icon) or by re-uploading
   via **Add file → Upload files** with the same filename.
2. Commit to `main`.
3. Pages redeploys automatically, usually within a minute. Progress is visible under the
   **Actions** tab.
4. Check the live URL with a hard refresh (`Cmd+Shift+R`) or in a private window — Pages caches
   aggressively and a normal reload will show the old version.

When the privacy policy changes in a way that affects users, also update the "last updated" date
at the top of `index.html`, and keep the App Privacy answers in App Store Connect consistent
with it.

## Keeping it accurate

The privacy policy describes the app's actual behaviour, which was verified against the source:

- Microphone audio is analysed on-device and never recorded, stored, or transmitted.
- Lesson progress, theme, and first-launch state are stored locally via `SharedPreferences`.
- The only outbound data is the in-app support form (name, email, message, optional image) via
  Supabase, and crash and performance reports via Sentry.

If any of that changes in the app, this policy has to change with it — and so may the App
Privacy answers in App Store Connect.

## Contact

Abhinav Madke, on behalf of 999 Online Inc. — abhinav.madke@999venturestudio.com

---

© 2026 999 Online Inc. All rights reserved.
