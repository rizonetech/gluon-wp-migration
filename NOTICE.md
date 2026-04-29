# Notice — attribution and modifications

> **Status:** stub. The full content lands when [`todo/gluon-wp-migration/TODO-01-scaffold-and-copy.md`](../../todo/gluon-wp-migration/TODO-01-scaffold-and-copy.md) Section 1.4 is executed (private workspace).

## Upstream works

This plugin is a derivative work of two GPL-2.0-or-later plugins published by **ServMask Inc.**:

- **All-in-One WP Migration** — `https://wordpress.org/plugins/all-in-one-wp-migration/`
- **All-in-One WP Migration Unlimited Extension** — `https://servmask.com/products/unlimited-extension`

Copyright in those upstream works belongs to ServMask Inc. and the original contributors. Their license (GPL-2.0-or-later) is preserved in this fork via [`LICENSE`](LICENSE).

## Modifications (high level)

Gluon WP Migration is a substantially modified derivative work. Modifications include:

- **Rebrand of the application layer** — class/function/constant prefixes, text domain, hook/filter names, asset handles, CSS classes, JS namespace, cookie/nonce names, admin menu slugs, WP-CLI command, backups folder name, and the outer archive file extension. Internal archive format remains compatible with the upstream `.wpress` format.
- **Merge of the two upstream plugins** into a single plugin (no paid-tier separation, no separate "extension" plugin).
- **Removal of paid-tier UI** — premium upsell calls-to-action, upgrade screens, and links to paid extensions.
- **Admin UI redesign** so the plugin is visibly distinct from the upstream.
- **GitHub-based update channel** via `plugin-update-checker` (not the wp.org plugin directory).

A complete change record will be maintained alongside the rebrand work as it is implemented.

## Vendored third-party libraries

Code under `lib/vendor/` (notably the `servmask/` and `bandar/` libraries from the upstream plugins) is **structurally untouched**. Original copyright headers, file structure, and class names within `lib/vendor/` are preserved. Only the outer wrappers and require paths in the application layer are modified.
