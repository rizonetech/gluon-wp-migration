# Gluon WP Migration

A WordPress site migration plugin: export your site (database, files, themes, plugins, uploads) to a single archive, restore it onto another WordPress install. No upload-size cap, no premium tier, no upsell UI.

> **Status:** scaffold only. Implementation has not started yet. Not ready for use. The plan lives in the parent (private) workspace at `todo/gluon-wp-migration/`.

## Highlights (planned for v1.0.0)

- **Single plugin, no paid extension.** Full functionality in the free download.
- **Per-file integrity verification.** Every entry in an archive carries a SHA-256 hash; restores verify before extracting and abort cleanly on mismatch.
- **Optional AES-256-GCM encryption.** Passphrase-derived key via libsodium. Lose the passphrase, lose the backup — by design.
- **Resumable exports and imports.** Survives PHP timeouts, low memory limits, and closed browser tabs. Picks up from the last checkpoint.
- **First-class WP-CLI.** Every operation scriptable from the command line. JSON output supported.
- **Selective backup and restore.** Pick categories (database, uploads, themes, plugins) on either side; pull a single file out of an old archive without restoring the whole thing.
- **Built-in scheduler.** Cron-driven backups with configurable retention. No paid add-on.
- **REST API.** `/wp-json/gwpmig/v1/...` for headless dashboards and CI/CD integration. Application-password auth supported.
- **Modern admin UI.** Built with `@wordpress/components`. Mobile-responsive. WCAG 2.1 AA.
- **Helpful errors.** Stable error codes (`GWPMIG_E_*`), actionable messages, one-click diagnostic dump.
- **One-way `.wpress` import.** Existing All-in-One WP Migration users can restore their old archives into Gluon. Future backups are saved as `.gwpack` (Gluon's own format).

See [`docs/`](docs/) for the format spec, error code reference, and architecture documents (added as design firms up).

## Updates

This plugin uses **GitHub-based updates** via [`rizonetech/gluon-update-checker`](https://github.com/rizonetech/gluon-update-checker) — Gluon's own focused, modern self-update library, written as an independent alternative to [`YahnisElsts/plugin-update-checker`](https://github.com/YahnisElsts/plugin-update-checker). It enforces strict SemVer 2.0, supports a 5-channel release system (`stable` / `rc` / `beta` / `alpha` / `nightly`), takes an atomic backup before every install and rolls back on failure, and sends zero telemetry — every byte that leaves your site is a documented public GitHub API request.

Each tagged release on this repository is published as a versioned ZIP asset; the update checker reads the channel you've subscribed to and offers updates through the standard WordPress admin **Updates** screen, the same way wp.org-hosted plugins do. The plugin sets the WordPress `Update URI` header so the wp.org plugin directory can never accidentally serve a different plugin with the same slug.

## License

[GPL-2.0-or-later](LICENSE) — matches WordPress.
