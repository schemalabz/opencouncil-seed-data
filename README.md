# OpenCouncil seed artifacts

This repository publishes the verified subset seed for local OpenCouncil development.
It has a new Git history. The old seed data repository remains private.

The latest release contains `manifest.json`, `subset.tar.zst`, and `verify-report.json`.
The archive contains a sample of released council records. It does not include user accounts.
The full production content archive is not published here.

Run `npm run db:deploy:seed` in [OpenCouncil](https://github.com/schemalabz/opencouncil) to load the latest release into an empty local database. The setup checks the archive size and SHA-256 hash against the manifest before restoring it.

For an older checkout, select a compatible release with `npm run seed -- restore --from https://github.com/schemalabz/opencouncil-seed-data/releases/download/<tag>`.

See the [database seeding guide](https://github.com/schemalabz/opencouncil/blob/main/docs/database-seeding.md) for requirements and commands. See the [seed pipeline](https://github.com/schemalabz/opencouncil/tree/main/packages/seed-pipeline) for production and verification rules.
