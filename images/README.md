# Images

A small curated library of famous, high-resolution, unambiguously
public-domain paintings — used for the single-artwork "cinematic edit" Reel
format (`reel.build_single_artwork_reel` in the main repo), as an
alternative to always pulling from the live museum APIs. Sourced from
Wikimedia Commons, each confirmed `{{PD-old}}`/Public Domain with no
attribution required before being added here.

`daily_post.py`'s `pick_curated_artwork` reads `manifest.json`, skips
whatever's already in the main repo's `posted_ids.json` (namespaced
`curated:<slug>`), and downloads the chosen image.

**Adding a new piece:** drop the image in this folder and add an entry to
`manifest.json` with `slug`, `file`, `title`, `artist_line`, `date_display`,
`museum_name`, `museum_hashtag`, `credit_line`, `hashtag_terms`, and
`wiki_title` (the exact English Wikipedia article title, used for the
background-fact lookup — a miss just means no background fact, not a
crash).

**On licensing:** only add work that's public domain *everywhere relevant*
— not just under a US pre-1928 publication date. That ruled out some
famous 20th-century artists (e.g. Picasso, d. 1973) whose early work is
PD in the US but not yet in the EU, and who Wikimedia Commons itself mostly
excludes for that exact reason. When in doubt, check the artist's death
date against Commons' own licensing tags before adding, not just US rules.

**Composition note:** the cinematic edit's left/middle/right coverage
shots assume the artwork fills most of the frame with real detail
throughout (brushwork, texture) — very sparse or mostly-negative-space
paintings won't showcase as well in the tight regional pushes.
