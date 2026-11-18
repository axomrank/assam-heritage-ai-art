# Assam Heritage AI Art: gallery of Assamese history, legend and culture artworks

> Gallery of 58 AI-generated artworks of Assamese history, legends, culture and architecture, with comparison, tagging and review tools. All are labelled as interpretations.

**[Live site](https://axomrank.github.io/assam-heritage-ai-art/)** · [Part of AxomRank](https://github.com/axomrank)

## At a glance

- **58 AI-generated artworks** in five categories: History and Royalty, Folklore and Legends, Sacred and Culture, Traditional Architecture, and Notable Figures
- **Side-by-side comparison** with linked zoom and pan, ratings, tags and correction flags
- **Personal reviews** stay in the browser and can be exported or imported as JSON
- These are **interpretations, not historical likenesses**

## Quick start

```bash
python -m pip install pillow
python build_gallery.py
```

## Overview

An offline-capable collection of **58 AI-generated artworks**, with subject/category browsing, original and personal tags, ratings, historical-review flags, and synchronized side-by-side image comparison.

## Use the gallery

Open `index.html` or the GitHub Pages site. Choose two **Compare this image** boxes and click **Compare**. Zoom with the linked slider or scroll wheel; drag either image to pan both. Select an artwork to rate it, add comma-separated tags, flag details for correction, or record notes. Existing artwork IDs are preserved as direct links (`#sukapha-portrait`, for example).

Categories remain History & Royalty, Folklore & Legends, Sacred & Culture, Traditional Architecture, and Notable Figures. Subjects and source tags come from the original catalogue, with titles and descriptions preserved. No unverified chronology has been invented. All 58 files remain, including one exact duplicate pair; `duplicate-review.html` lets you compare exact copies, perceptual-similarity suggestions, and same-subject variants, then export choices without deleting files automatically.

Personal reviews stay in this browser. **Export personal reviews** saves portable JSON; **Import personal reviews** merges matching entries, replacing reviews for matching IDs and image checksums. Local files and the hosted website use separate browser storage. The storage key and export schema are separate from the AHOM library, so the two galleries do not overwrite each other's notes.

## Assets and metadata

- `images/`: 58 original artworks with original filenames and folders unchanged.
- `data/gallery.json`: original gallery metadata, retained unchanged.
- `catalog.json` / `catalog.js`: review catalogue, original checksums and offline browser data.
- `thumbnails/`: lightweight WebP previews; originals load on demand.
- `gallery.js`, `gallery.css`, `gallery-template.html`: the gallery interface.
- `build_gallery.py`: verifies original checksums and rebuilds thumbnail/catalogue outputs (requires Pillow).
- `backup_library.py`: creates a verified local ZIP with SHA-256 sidecar under ignored `backups/`.

These images are AI-generated interpretations, not historical photographs, verified likenesses, or evidence of historical appearance. Source captions, identity associations, costumes, architecture and cultural details may need review. A personal review checkbox records your review and does not establish historical accuracy.

## Rebuild and back up

```sh
python -m pip install pillow
python build_gallery.py
python backup_library.py
```

The backup script verifies original image checksums, ZIP integrity and archived image checksums. Copy the ZIP and SHA-256 sidecar to another drive or cloud storage. Export personal review JSON separately and retain it alongside the backup; the script cannot access browser storage.

Other repository material, including Instagram cards and college research documents, remains unchanged and is not mixed into the 58-artwork gallery. GitHub Pages deploys via the existing workflow.

## Roadmap: future improvements

- [ ] Remove the exact duplicate pair after review (`duplicate-review.html`)
- [ ] Write an expert review note for each artwork (costume, architecture, identity)
- [ ] Add Assamese titles and descriptions
- [ ] Move the college literary research documents to assam-history-sources or a separate repo
- [ ] Add a license statement for the generated images

## For AI agents and contributors

Read [AGENTS.md](AGENTS.md). Keep original image bytes and ids, and run `build_gallery.py` after changes.

Commit as the `axomrank` account. Keep changes small and reviewable, and run the repository's checks before pushing.

## Part of AxomRank

[AxomRank](https://axomrank.pages.dev) offers free, bilingual preparation for Assam government exams. Related repositories:

- **Learn:** [axomrank.github.io](https://github.com/axomrank/axomrank.github.io) (the AxomRank learning app), [floor-test-simulator](https://github.com/axomrank/floor-test-simulator) (parliamentary majority simulator)
- **Explore Assam history:** [ahom-kingdom-history](https://github.com/axomrank/ahom-kingdom-history) (illustrated Ahom kingdom website and 41 reign lessons), [assam-history-map](https://github.com/axomrank/assam-history-map) (year-by-year historical map), [assam-history-characters](https://github.com/axomrank/assam-history-characters) (character sheets for Assam's history), [assam-visual-archive](https://github.com/axomrank/assam-visual-archive) (gallery of Assam scenes and photographs)
- **Open data:** [assam-exam-pyq](https://github.com/axomrank/assam-exam-pyq) (2,398 previous-year questions with answers), [assam-exam-syllabus](https://github.com/axomrank/assam-exam-syllabus) (syllabi for 12 recruitment boards), [assam-maps](https://github.com/axomrank/assam-maps) (map portal and GIS layers), [assam-history-sources](https://github.com/axomrank/assam-history-sources) (Kamarupa inscriptions and primary sources)
- **Publishing and brand:** [axomrank-blog](https://github.com/axomrank/axomrank-blog) (exam guides built from real papers), [assam-history-books](https://github.com/axomrank/assam-history-books) (13-book history of Assam), [axomrank-brand-assets](https://github.com/axomrank/axomrank-brand-assets) (brand kit and social media library)

## License and contact

No license file yet, so all rights are reserved by default.

Corrections and questions: open an issue in this repository. AxomRank is run by Angsuman Das (sole proprietor).
