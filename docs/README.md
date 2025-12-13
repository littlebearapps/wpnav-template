# WP Navigator Project Documentation

This folder contains documentation for your WP Navigator project.

## Key Files

| File | Purpose |
|------|---------|
| `wpnavigator.jsonc` | Your site's configuration and intent manifest |
| `snapshots/site_index.json` | Current site structure (generated) |
| `snapshots/pages/*.json` | Individual page snapshots (generated) |
| `.wpnav.env` | WordPress credentials (git-ignored) |

## Workflow

1. **Snapshot** - Capture what your site looks like now
   ```bash
   npx wpnav snapshot site
   ```

2. **Edit Manifest** - Update `wpnavigator.jsonc` with your desired changes

3. **Diff** - See what would change
   ```bash
   npx wpnav diff
   ```

4. **Sync** - Apply changes (always preview first!)
   ```bash
   npx wpnav sync --dry-run  # Preview
   npx wpnav sync            # Apply
   ```

## Working with AI

When asking AI assistants for help:

1. **Share context** - Point them to `wpnavigator.jsonc` and relevant snapshots
2. **Be specific** - Describe exactly what you want to achieve
3. **Review changes** - Always check proposed manifest edits before syncing
4. **Use dry-run** - Preview with `npx wpnav sync --dry-run` first

## Safety

- Credentials are stored locally in `.wpnav.env` (never committed to git)
- All changes go through `wpnav sync` (never direct to WordPress)
- Pre-sync snapshots are created automatically for rollback
- Use `npx wpnav rollback` if something goes wrong

## Resources

- [CLI Reference](https://wpnav.ai/docs/cli)
- [Manifest Schema](https://wpnav.ai/docs/manifest)
- [Troubleshooting](https://wpnav.ai/docs/troubleshooting)
