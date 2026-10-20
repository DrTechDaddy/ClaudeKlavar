# ClaudeKlavar

Webpage to convert midi to Klavar notation, written by Claude AI

> **Work in progress.** This is an example/experiment, not a finished product or service.
> Known gaps: line and page breaks are chosen automatically (no custom phrase breaks yet), and the page needs an
> internet connection to load its two libraries.

## Use

Open `midi2klavar.html` in a normal browser (Chrome, Edge, Firefox). It is a single file with no build step,
but it loads two libraries from the jsDelivr CDN (d3 and @tonejs/midi), so it needs an internet connection.

1. Drop a `.mid` file onto the page (or a `toJSON()` file from `@tonejs/midi`).
2. Pick tracks, stem side per track (R / L / none), bars per column, beat size and head size.
3. Press **Print…** to get paged output; **Left-align pages** leaves the right margin free so sheets can overlap on a music stand.

## Notation

- Time runs bottom to top; one beat is a fixed height.
- Klavar staff: lines run down the black-key lanes; noteheads use Aikin 7-shape heads (do re mi fa sol la ti).
- Stems are horizontal; higher-pitched tracks point right, lower-pitched tracks point left (changeable per track).
- Optional duration tails (blue when heads are black). "Head size: fit to notes" shrinks heads so fast passages don't overlap.

## Folders

- `midi/` – input MIDI files
- `printout/` – generated PDF printouts
