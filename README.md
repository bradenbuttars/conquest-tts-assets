# Conquest TTS assets

Image assets for a Tabletop Simulator mod of *Conquest: The Last Argument of Kings*
and *Conquest: First Blood*.

This repository exists purely as an image host. Tabletop Simulator fetches object
textures over plain HTTP at load time, and the mod previously served everything from
a single third-party file host — roughly 1,110 URLs from one origin, with no retry in
the client. One rate-limit decision there takes every card and token in the mod down
at once. Serving from a CDN removes that single point of failure.

## Layout

- `cards/` — card faces and 2D unit token art, downscaled for sane texture memory.
  The originals were print masters (many at 2480x3508, A4 at 300dpi); at TTS's actual
  render and zoom sizes they cost about 6x the video memory for no visible gain.
- `boards/` — faction reference boards composited for the mod.

## Use

Files are served via jsDelivr, pinned to a tag so URLs never shift:

```
https://cdn.jsdelivr.net/gh/<owner>/conquest-tts-assets@<tag>/cards/<file>
```

## Provenance

Game artwork is © Para Bellum Wargames and is reproduced here only to host the
textures used by a free, non-commercial fan mod. Board composites in `boards/` are
assembled from that artwork. No ownership is claimed. Takedown requests will be
honoured immediately — open an issue or contact the repository owner.

This repository is unrelated to any employer of the repository owner.
