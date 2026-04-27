# Lokuma Design Engine — Backup Image Library

Stock imagery used by the engine's image resolver fallback chain
([`tools/image_resolver.py`](https://github.com/Mumu090909/lokuma-design-engine/blob/main/tools/image_resolver.py))
when AI generation fails or returns an inappropriate image.

Each subfolder is a topical category. Filenames preserve the original
provider's ID (e.g. `pixabay_2562646.jpg`, `unsplash_AFBFw7apV1o.jpg`)
so attribution can be traced back when needed.

## Provenance

All images are sourced from public stock libraries with permissive licenses:

- **pixabay.com** — Pixabay License (free for commercial use, no attribution required)
- **unsplash.com** — Unsplash License (free for commercial and non-commercial use, attribution appreciated)

If you redistribute this collection, please respect the original licenses.

## Categories

```
abstract/          architecture/      automotive/        beauty/
cafe/              ecommerce/         education/         fashion/
fitness/           food/              healthcare/        kids-family/
nature/            portrait/          real-estate/       restaurant/
team/              wellness/          workspace/         agriculture/
```

## Usage from the engine

The engine clones (or downloads) this repo into
`<engine-root>/assets/backup_images/`. The image resolver looks up files
by category and filename pattern; no manifest file is required — directory
structure is the contract.

To set up a fresh engine checkout:

```bash
# Inside your lokuma-design-engine clone:
git clone https://github.com/Mumu090909/lokuma-design-engine-assets.git assets/backup_images
```
