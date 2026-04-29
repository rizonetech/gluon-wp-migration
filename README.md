# Gluon WP Migration

WordPress site migration plugin — a fork of [All-in-One WP Migration](https://wordpress.org/plugins/all-in-one-wp-migration/) with the [Unlimited Extension](https://servmask.com/products/unlimited-extension) merged in. Same export/import pipeline, no upload size cap, no paid-tier UI, GPL-2.0-or-later end to end.

> **Status:** scaffold only. Plugin code is still being ported. Not ready for use. See the migration plan in the parent workspace at [`todo/gluon-wp-migration/`](../../todo/gluon-wp-migration/) (private).

## Heritage and licensing

This plugin is a derivative work of two GPLv2-licensed plugins by ServMask Inc.:

- **All-in-One WP Migration** — base plugin
- **All-in-One WP Migration Unlimited Extension** — removes the upload cap, adds retention features

Both upstreams are GPL-2.0-or-later. This fork preserves that license. Modifications include rebrand of the application layer (class/function/constant prefixes, text domain, hook names, asset handles, menu slugs, CSS classes, JS namespace, cookie/nonce names, WP-CLI command, backups folder, archive extension), removal of paid-tier upsell UI, an admin UI redesign, and the merge of the two plugins into one. Vendored third-party libraries under `lib/vendor/` (servmask + bandar) retain their original copyright headers unchanged.

A full attribution and modification record will live in [`NOTICE.md`](NOTICE.md) once the plugin scaffold is populated.

## Updates

This plugin uses **GitHub-based updates** via [`YahnisElsts/plugin-update-checker`](https://github.com/YahnisElsts/plugin-update-checker), not the wp.org plugin directory. Releases are published as versioned ZIP assets on this repository.

## License

[GPL-2.0-or-later](LICENSE) — matches WordPress and the upstream plugins.
