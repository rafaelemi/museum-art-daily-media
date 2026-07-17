# museum-art-daily-media

Temporary public hosting for [MuseumArtDaily](https://github.com/rafaelemi/museum-art-daily)'s generated Instagram Reel videos.

Instagram's Content Publishing API needs a public URL to fetch a Reel's video from; a locally-generated MP4 has none. This repo exists purely so the daily automation can upload a video as a release asset here, hand that public URL to Instagram, and delete the asset again right after publishing. Nothing is meant to persist here — an empty releases list is the expected steady state.
