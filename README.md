# dailyguitar-legal

This repository is a **redirect**. It used to hold a copy of the privacy policy
for **Daily Guitar: Chords & Lessons**, the iOS and Android app published by
999 Online Inc. (trading as 999 Venture Studio).

## Where the policy actually is

| | |
| --- | --- |
| Privacy policy | https://dailyguitar-ten.vercel.app/privacy |
| Terms of use | https://dailyguitar-ten.vercel.app/terms |
| Source | `app/privacy/page.tsx` and `app/terms/page.tsx` in the `dailyguitar-website` repo |

Those are the two pages the **app itself** links to, from the notice under the
sign-in and sign-up buttons (`LegalLinks` in `lib/services/legal_links.dart`),
and from the rows on the profile screen. Use the same URLs in App Store Connect
and Google Play Console.

## Why this is a redirect and not a copy

There were two live privacy policies and they drifted. The app grew Google and
Apple sign-in; the copy on the Daily Guitar site was updated to match; this one
went on saying *"There are no accounts and no advertising"* and *"we do not
require an account, and there is nothing to sign in to"* for weeks, on an app
that will not get past its welcome screen without one.

App Review reads the policy against the app and against the App Privacy answers
in App Store Connect. A policy denying the existence of the accounts the app
insists on is a contradiction, and two of them is two chances to have it.

**Do not paste the policy text back into `index.html`.** The address is what has
to keep working, not the copy. It was submitted to the stores once and the
README called it permanent, so it has to resolve forever even though nothing
points at it any more — an old listing, a cached crawl, or a link in somebody's
email will still arrive here.

## How the redirect works

GitHub Pages serves static files and cannot send a 301, so `index.html` carries
three things, and the third is the one that matters:

1. `<meta http-equiv="refresh">` — moves an ordinary browser immediately.
2. `<link rel="canonical">` — tells crawlers which page is the real one.
3. **A visible link in the body** — for anybody the refresh does not move: a
   reviewer with a strict browser, a text-mode client, a bot. If the refresh
   ever stops working this is still a page that gets you to the policy.

Published from the repository root on `main`, Settings → Pages → *Deploy from a
branch*. Pages redeploys within a minute of a commit and caches aggressively, so
check with a hard refresh (`Cmd+Shift+R`) or a private window.

## Keeping it accurate

Nothing to keep accurate here any more, which is the point. What the policy has
to stay in step with is in the app repo: `ios/Runner/PrivacyInfo.xcprivacy`, the
App Store Connect privacy questionnaire, and Google Play's Data safety form.
`docs/app-store-release.md` is the one document that holds all three together.

## Contact

Abhinav Madke, on behalf of 999 Online Inc. — abhinav.madke@999venturestudio.com

---

© 2026 999 Online Inc. All rights reserved.
