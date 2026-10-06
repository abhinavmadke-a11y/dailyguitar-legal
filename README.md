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

## There are two copies of this policy, and they must not drift

The same policy is published twice:

| URL | Source |
| --- | --- |
| https://abhinavmadke-a11y.github.io/dailyguitar-legal/ | `legal/index.html` in the app repo, uploaded to the `dailyguitar-legal` repo |
| https://dailyguitar-ten.vercel.app/privacy | `app/privacy/page.tsx` in the `dailyguitar-website` repo |

Both were updated on 7 October 2026 and currently say the same thing. **Pick one
for the store listings and keep the other pointing at it**, because two live
privacy policies that disagree is exactly the contradiction App Review looks
for — and they did disagree until this date, when the GitHub Pages copy still
said the app had no accounts.

## Keeping it accurate

The policy describes the app's actual behaviour, verified against the source on
7 October 2026, and against `ios/Runner/PrivacyInfo.xcprivacy`, which is the
machine-readable declaration Apple reads from inside the bundle. The two have to
agree with each other **and** with the App Privacy answers in App Store Connect;
`docs/app-store-release.md` is the script that keeps all three in step.

- Microphone audio is analysed on-device and never recorded, stored, or
  transmitted. On a song from the library the microphone is off by default.
- Sign-in with Google or Apple, storing email, name, and avatar URL in
  `profiles`.
- Lesson progress, cleared chord shapes, song attempts, and the onboarding
  answers sync to Supabase against the account.
- A Firebase push token and a practice schedule, for reminders.
- Usage analytics via PostHog, against an install-local identifier that is not
  joined to the account. Session replay is **off**.
- Crash and performance reports via Sentry, with `sendDefaultPii` left false.
- Play-alongs are YouTube embeds; nothing is downloaded or re-hosted.
- Account deletion from inside the app, through the `delete-account` Edge
  Function.

If any of that changes in the app, this policy, the website copy, the privacy
manifest, and the App Store Connect answers all have to change with it.

## Contact

Abhinav Madke, on behalf of 999 Online Inc. — abhinav.madke@999venturestudio.com

---

© 2026 999 Online Inc. All rights reserved.
