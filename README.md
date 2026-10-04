# Nekuvio Badges

Generated badge assets and metadata for the **Nekuvio** Nuvio addon.

This repository contains the files used by Nuvio to display Nekuvio-specific badges, along with generated TypeScript metadata consumed by Nekuvio when building stream responses.

## Structure

```text
.
├── generate.py
├── nuvio/
│   ├── badges/
│   │   └── ...
│   └── nekobt-badges.json
└── src/
    └── generated/
        └── nekobt-metadata.ts
```

### `generate.py`

The generator that produces all generated files in the repository.

### `nuvio/`

Files consumed by Nuvio:

* `nekobt-badges.json` — badge definitions and metadata.
* `badges/` — badge assets referenced by the generated JSON.

### `src/generated/`

Generated TypeScript consumed by Nekuvio.

* `nekobt-metadata.ts` — metadata used by Nekuvio when generating stream responses and badge markers.

## Generation

The repository's generated files should not be edited manually.

Changes to badge definitions or metadata should be made in `generate.py`, followed by running the generator and committing the resulting files.

The generated files are committed because `nuvio/` is directly consumed as a public GitHub-hosted resource.

## Related project

The main application is maintained in the [Nekuvio repository](https://github.com/dormindev/Nekuvio).

Nekuvio consumes the generated TypeScript metadata, while Nuvio consumes the generated JSON and badge assets from this repository.
