# lumberjack-site

Static website for the Lumberjack workout app, served by GitHub Pages at https://lumberjack.fit.

| Page | URL | Purpose |
| --- | --- | --- |
| `index.html` | `/` | Landing page |
| `privacy.html` | `/privacy` | Privacy Policy (Play Console privacy policy URL) |
| `terms.html` | `/terms` | Terms of Service |
| `support.html` | `/support` | Support contact and FAQ |
| `delete-account.html` | `/delete-account` | Web account deletion (Play Console account deletion URL) |
| `404.html` | n/a | Not-found page, served automatically by GitHub Pages |

Link between pages with extensionless paths (`/privacy`) so URLs stay stable.

## Contact addresses

| Address | Where |
| --- | --- |
| `privacy@lumberjack.fit` | `privacy.html` (data rights requests, Contact section) |
| `support@lumberjack.fit` | `terms.html`, `support.html`, `delete-account.html` (fallback for people who can't sign in) |
| `info@lumberjack.fit` | Footer on every page (general inquiries) |

## Before going live

Fill the placeholders: `{{OPERATOR_NAME}}`, `{{EFFECTIVE_DATE}}` and `{{GOVERNING_LAW}}` in the
legal pages. The Firebase web config in `delete-account.html` is already filled in. Search for `TODO(maintainer)` too. `lumberjack.fit` must also be added to
Firebase Console → Authentication → Settings → Authorized domains, or sign-in on the delete page fails.

Plain HTML + CSS, no build step. Colors, type and corner radii mirror the app's theme
(`app/src/main/java/com/lumberjack/workout/ui/theme` in the app repo), with dark as the default
and a light scheme via `prefers-color-scheme`.

## Preview locally

```
python -m http.server 8000
```

then open http://localhost:8000.

## Publish

Repo → Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.

## Fonts

`fonts/` bundles Barlow Condensed (Copyright 2017 The Barlow Project Authors) and Instrument Sans
(Copyright 2022 The Instrument Sans Project Authors), both under the
[SIL Open Font License 1.1](https://openfontlicense.org).
