# Site instructions

Only report to me in ASD-STE100 Simplified Technical English.

This site uses Seite. Edit pages and posts in `content/`, page layouts in `templates/`, and files that keep their URL in `public/`. Use `seite check --strict` before you finish a site change. The GitHub Actions workflow builds the site after a push to `main`.

### Custom Template: Atom Autodiscovery

Your custom `templates/base.html` does not include Atom feed autodiscovery.
Add an Atom autodiscovery link next to your existing RSS link:

```html
<link rel="alternate" type="application/atom+xml" title="{{ site.title }}" href="{{ lang_prefix }}/atom.xml">
```

## MCP Setup per Agent

<!-- seite:agent-setup -->
| Agent | MCP config | One-time step |
|---|---|---|
| Codex CLI | `.codex/config.toml` | Trust the project when Codex asks (untrusted projects ignore the file, including its tool auto-approval); check with `/mcp` |
<!-- /seite:agent-setup -->

## Context Rules

<!-- seite:context-rules -->
Detailed guides live in `.agents/rules/`. Before editing, read the guides for the files you touch:

- `templates/**`: `seo-requirements.md`, `templates.md`, `i18n.md`, `features.md`, `design-prompts.md`
- `content/**`: `i18n.md`, `shortcodes.md`, `features.md`, `private-collections.md`
- `data/i18n/**`: `i18n.md`
- `data/**`: `data-files.md`
- `templates/shortcodes/**`: `shortcodes.md`
- `seite.toml`: `config-reference.md`, `private-collections.md`
<!-- /seite:context-rules -->
