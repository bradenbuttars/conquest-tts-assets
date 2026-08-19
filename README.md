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
- `rituals/` — Sorcerer Kings ritual cards, and the shared ritual card back.
- `elements/` — the public-domain paintings used as elemental headers on the
  ritual cards, kept here so the cards can be regenerated from source.

## Use

Files are served via jsDelivr, pinned to a tag so URLs never shift:

```
https://cdn.jsdelivr.net/gh/<owner>/conquest-tts-assets@<tag>/cards/<file>
```

## Attribution — elemental art

The four paintings behind the ritual card headers are public domain, from the
Metropolitan Museum of Art's Open Access collection, which releases images of
public-domain works under CC0:

| Element | Work | Artist |
|---|---|---|
| Fire | *An Eruption of Vesuvius* | Johan Christian Dahl |
| Water | *Northeaster* | Winslow Homer |
| Earth | *Bandits on a Rocky Coast* | Salvator Rosa |
| Air | *Clouds* | Thomas Cole |

Dual-element rituals combine two of these. The Met was chosen over other museum
APIs because its CC0 designation covers the images themselves, not only the
accompanying metadata.

## Attribution — elemental art

The ritual card headers use public-domain paintings from the Met's Open Access
collection, which releases images of public-domain works under CC0:

| Element | Work | Artist |
|---|---|---|
| Fire | *An Eruption of Vesuvius* | Johan Christian Dahl |
| Water | *Northeaster* | Winslow Homer |
| Earth | *Bandits on a Rocky Coast* | Salvator Rosa |
| Air | *Clouds* | Thomas Cole |

The faction boards — chant board, season wheel and both Spires pools — use each
faction's own artwork from its army book instead. Gallery paintings were the wrong
register beside the rest of the mod. That art is © Para Bellum, covered by the note
below.

## Provenance

Game artwork is © Para Bellum Wargames and is reproduced here only to host the
textures used by a free, non-commercial fan mod. Board composites in `boards/` are
assembled from that artwork. No ownership is claimed. Takedown requests will be
honoured immediately — open an issue or contact the repository owner.

This repository is unrelated to any employer of the repository owner.
