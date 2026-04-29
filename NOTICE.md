# Notice

## Acknowledgement of prior art

[All-in-One WP Migration](https://wordpress.org/plugins/all-in-one-wp-migration/) by ServMask Inc. is the dominant prior art in WordPress site migration and the reason this category of plugin exists at scale. Gluon WP Migration is an **independent implementation** that draws inspiration from AIOWPM's behavior and feature set but **shares no source code, format internals, identifiers, or assets** with it. Where AIOWPM and Gluon end up doing similar things (both are WordPress migration plugins, after all), the resemblance is functional, not derivative.

For users coming from AIOWPM: Gluon includes a one-way reader for `.wpress` archives so existing backups can be imported. Gluon writes its own `.gwpack` format for new backups.

## Third-party libraries

Bundled third-party libraries (under `vendor/`, vendored via Composer) retain their original copyright and license notices in their respective directories. License inventory is published in [`docs/licenses.md`](docs/licenses.md) (added during build).

The plugin itself is licensed under [GPL-2.0-or-later](LICENSE).
