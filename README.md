# what-the-cat-site

The public pages for the **What the Cat** Android app — currently just the
privacy policy that the Google Play listing links to.

- `index.html` — the privacy policy, served by GitHub Pages at
  <https://faelperetta.github.io/what-the-cat-site/>

The app itself lives in a separate, private repository. Nothing here is part of
the app: it is a static page with no scripts, no analytics and no third-party
resources beyond the Google Fonts stylesheet.

## Keeping it true

The policy describes the app's behaviour, so it has to be updated *before* a
release that changes any of this:

- the app stores everything in its own private storage and makes no network
  requests;
- there is no account, no analytics, no advertising and no tracking;
- `android:allowBackup` is `true`, so Android's own device backup may include
  the app's data — the "Device backup" section covers that and must be removed
  if backup is ever turned off;
- adding optional sign-in and cloud sync means rewriting the policy and giving
  it a new effective date.

## Publishing

GitHub Pages serves the default branch from the repository root. A push to
`main` is a deploy; there is no build step.
