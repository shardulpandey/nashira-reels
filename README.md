# Nashira reels

Web-optimised copies of the UGC clips used by the shoppable reel rail on
shopnashira.com. Source footage lives in the brand Drive; these are the
compressed H.264 versions the storefront actually loads.

Encoded with `encode.py`: **compression only**. Original resolution, aspect
ratio and frame rate are untouched - nothing is cropped out of frame and
nothing is re-sampled. H.264 at CRF 28, AAC 96k, and `+faststart` so playback
can begin before the file is fully down.

Five 4K clips came out above the jsDelivr 20 MB ceiling at CRF 28, so
`squeeze.py` stepped their CRF up (32-44) until each fit. Still no resize -
only the quality knob moved. See `squeezed.json`.

## Using a clip

Paste the jsDelivr URL into the reel block's **MP4 URL** field in the theme
editor. Do not link `raw.githubusercontent.com` - it is not a CDN and GitHub
rate-limits hotlinking.

```
https://cdn.jsdelivr.net/gh/shardulpandey/nashira-reels@main/clips/<file>.mp4
https://cdn.jsdelivr.net/gh/shardulpandey/nashira-reels@main/posters/<file>.jpg
```

`urls.json` in this repo lists every clip with its creator folder.

49 clips, 365 MB total.
