# donal.us

This is Donal Heidenblad's personal site. [Seite](https://seite.sh/) builds the static files. GitHub Pages serves them at [donal.us](https://donal.us).

## Work locally

Install Seite, then run:

```sh
seite check --strict
seite serve
```

The source pages are in `content/`. Templates are in `templates/`. Files in `public/` keep their paths in the built site. `seite build --strict` writes the site to `dist/`.

The GitHub Actions workflow builds and publishes the site after a push to `main`. In the repository's Pages settings, set **Build and deployment → Source** to **GitHub Actions**. Keep the custom domain set to `donal.us` in those settings.
