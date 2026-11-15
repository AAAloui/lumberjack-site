# lumberjack-site

Static landing page for the Lumberjack workout app, served by GitHub Pages.

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
