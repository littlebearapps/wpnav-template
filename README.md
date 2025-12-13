# WP Navigator Project Template

A starter template for managing WordPress sites with AI assistants using [WP Navigator](https://wpnav.ai).

## Quick Start

1. **Use this template** - Click "Use this template" to create your own repository
2. **Install the plugin** - Download and activate WP Navigator on your WordPress site
3. **Configure credentials** - Run `npx wpnav configure` to connect to your site
4. **Take a snapshot** - Run `npx wpnav snapshot site` to capture your site state
5. **Start collaborating** - Open this folder in Claude Code or Codex and ask for help!

## Project Structure

```
my-wp-project/
├── wpnavigator.jsonc       # What you WANT your site to look like (your intent)
├── snapshots/              # What your site looks like NOW (read from WordPress)
│   ├── site_index.json     # Full site structure
│   └── pages/              # Individual page snapshots
├── roles/                  # Custom AI roles (optional)
├── docs/                   # Project documentation
├── sample-prompts/         # Ready-to-use AI prompts
└── .gitignore              # Ignores credentials
```

## How It Works

1. **Your WordPress site** - Where your real content and pages live
2. **This project folder** - Stores snapshots (current state) and manifest (desired state)
3. **Your AI assistant** - Reads these files, helps you plan changes
4. **WP Navigator** - Safely applies changes to WordPress

The AI never talks directly to your live site - it only edits files in this folder.
You stay in control.

## Commands

```bash
npx wpnav configure       # Set up WordPress connection
npx wpnav status          # Check connection status
npx wpnav snapshot site   # Capture site structure
npx wpnav diff            # Compare manifest vs WordPress
npx wpnav sync --dry-run  # Preview changes (safe)
npx wpnav sync            # Apply changes to WordPress
```

## Example AI Prompts

Start a conversation with your AI assistant:

> "Read wpnavigator.jsonc and help me review my site configuration"

> "I want to add a new About page with a team section and contact form"

> "Review my site's SEO settings and suggest improvements"

See `sample-prompts/` for more ready-to-use prompts.

## Documentation

- [WP Navigator Docs](https://wpnav.ai/docs)
- [CLI Reference](https://wpnav.ai/docs/cli)
- [Getting Started Guide](https://wpnav.ai/start)

## Support

- [Help Center](https://wpnav.ai/help)
- [GitHub Issues](https://github.com/littlebearapps/wp-navigator-mcp/issues)
- [Community Discussions](https://github.com/littlebearapps/wp-navigator-mcp/discussions)

---

Made with WP Navigator by [Little Bear Apps](https://littlebearapps.com)
