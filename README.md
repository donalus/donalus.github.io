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

## Work with an agent

Install Seite 0.20.0 or newer and make sure `seite` is in your `PATH`. Open this project in Codex and trust it when Codex asks. The project files then connect Codex to the Seite MCP server and run `seite check` when a Codex turn ends. The Seite skills are in `.agents/skills/`.

To start a Codex session with site context from Seite, run:

```sh
seite agent --with codex
```

Use `seite agent --with codex --once "write a draft post about ..."` for one task. Review agent changes before you commit them.
