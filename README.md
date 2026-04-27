# Lokuma Design Engine — Backup Image Library

Stock imagery used by the engine's image resolver fallback chain
([`tools/image_resolver.py`](https://github.com/Mumu090909/lokuma-design-engine/blob/main/tools/image_resolver.py))
when AI generation fails or returns an inappropriate image.

Each subfolder is a topical category. Filenames preserve the original
provider's ID (e.g. `pixabay_2562646.jpg`, `unsplash_AFBFw7apV1o.jpg`)
so attribution can be traced back when needed.

## Licensing — read this before reusing

This repository is **a curation, not original artwork**. Two layers of rights apply:

### 1. The individual images

Each image belongs to its original photographer / contributor. None of the
images in this repository are owned, authored, or licensed by Lokuma. They
are sourced from public stock libraries under their respective licenses:

- **pixabay.com** files (`pixabay_*.jpg`) — Pixabay Content License. Free
  for commercial and non-commercial use, attribution not required, but you
  may not sell unaltered copies or imply endorsement by the original
  contributor. Full terms: https://pixabay.com/service/license-summary/
- **unsplash.com** files (`unsplash_*.jpg` and IDs like `AFBFw7apV1o.jpg`) —
  Unsplash License. Free for commercial and non-commercial use, attribution
  appreciated but not required, you may not compile a competing or similar
  service from the photos. Full terms: https://unsplash.com/license

Lokuma claims **no rights** to the images themselves. If you reuse any
single image, your rights and obligations come from the original source's
license — not from us.

### 2. The curation (selection, categorization, and structure)

The choice of which images to include, the 20-category taxonomy, and the
directory structure that maps engine prompts to image candidates are
**Copyright © Lokuma. All rights reserved.**

This curation work is published here so that the
[Lokuma Design Engine](https://github.com/Mumu090909/lokuma-design-engine)
has a deterministic fallback dataset. It is **not** licensed for
redistribution as a "stock image pack", a competing dataset for a different
generator, or any commercial reuse of the curation itself.

If you want to use the curation (or a derivative of it) outside the
Lokuma Design Engine, contact Lokuma for permission.

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
