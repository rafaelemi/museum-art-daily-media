# Music

Drop real, public-domain (or otherwise properly licensed) instrumental
tracks here — `.mp3`, `.wav`, `.m4a`, `.ogg`, or `.flac`.

`reel.py`'s `pick_external_track` checks this folder on every Reel build.
If it finds at least one file here, it picks one at random and uses it
instead of composing its own MIDI. If the folder is empty (or missing),
nothing changes — the existing 6-piece composed-MIDI library is used as
before.

**Naming convention:** the filename (extension stripped, underscores/dashes
turned into spaces) becomes the credited piece name in captions. Name files
the way you'd want them credited, e.g.:

```
Erik Satie - Gymnopedie No 1.mp3
Claude Debussy - Clair de Lune.mp3
```

**Length:** tracks should run longer than ~30s — a random window is trimmed
out of the file rather than always starting at 0:00 (so a quiet intro
doesn't end up being the entire clip's music), so anything shorter than
the target Reel length will always start from 0:00 regardless.

**A note on tempo:** composed pieces have their cut/reveal/punch timing
snapped to the piece's actual beat grid (see `PIECE_BEAT_S` in `reel.py`).
Uploaded tracks don't have a known tempo, so their Reels fall back to
fixed-duration cut timing instead of beat-synced cuts. Nothing crashes
either way — it's just a smaller visual-polish difference.

**On licensing:** two real recordings are here as a working example —
Randolph Hokanson's public-domain-composition performances (Beethoven
Piano Sonata No. 27, Mendelssohn's "Spinner's Song"), sourced from
Wikimedia Commons under CC BY-SA 2.0. That license requires attribution,
which is why the performer name and license are baked right into the
filename — since the filename becomes the credited caption line, that's
attribution handled for free. If you add more tracks under a license that
requires credit, do the same: put the credit directly in the filename
rather than relying on a separate note that could get lost.
