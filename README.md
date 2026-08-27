# TWICE Wire

An independent, unofficial English-language fan hub for TWICE/ONCE — news translation, release reviews, official-only video curation, a live signal tracker, and a fan quiz, built to run on Google AdSense.

**Not affiliated with, endorsed by, or sponsored by JYP Entertainment, VARO Entertainment, or the members of TWICE.**

## What's in this repo

This is a single static page — `index.html` — with everything (HTML, CSS, JS) inlined. No build step, no dependencies, no backend. It's meant to be served as-is by GitHub Pages. This repo follows the same template as [Bangtan Wire](https://fhzl0117-hue.github.io/bangtan-wire/), [Blackpink Wire](https://fhzl0117-hue.github.io/blackpink-wire/), [Stray Kids Wire](https://fhzl0117-hue.github.io/stray-kids-wire/), [aespa Wire](https://fhzl0117-hue.github.io/aespa-wire/), [ENHYPEN Wire](https://fhzl0117-hue.github.io/enhypen-wire/), and [SEVENTEEN Wire](https://fhzl0117-hue.github.io/seventeen-wire/) — part of the "Wire" series, one dedicated site per artist.

The page is organized into six "desks," each mapped to a content pillar:

| Desk | Section id | What it does |
|---|---|---|
| 01 · News | `#news` | Translated & summarized news dispatches, each linking to its original source |
| 02 · Review | `#reviews` | Album / track reviews, text only |
| 03 · Screening Room | `#screening` | Official YouTube embeds only — never re-uploaded video |
| 04 · Signal | `#signal` | A live timer that counts down to confirmed future dates, or counts up ("time since") from the latest news when nothing future-dated is confirmed yet — auto-converted to the visitor's local timezone |
| 05 · Quiz | `#quiz` | A lightweight interactive quiz, no backend, no data collection |
| 06 · Market | `#market` | Links to official stores (affiliate links go here) |

## A note on accuracy: the JYP contract changes

As of this build, Jeongyeon (August 10, 2026) and Chaeyoung (August 13, 2026) have each ended their *exclusive* contract with JYP Entertainment to manage solo work independently — Jeongyeon through VARO Entertainment, Chaeyoung through her own "Lil Fantasy" banner. **Neither has left TWICE.** Both explicitly stated the group is unaffected and that group promotions continue under JYP as before. Jihyo and Tzuyu have been separately reported (unconfirmed as of this writing) to be weighing similar arrangements. Keep this distinction — agency change vs. group departure — sharp and accurate in any future edit; don't let it drift into "member leaves TWICE" framing, and don't understate it either. Cross-check any update against at least one of Forbes, Soompi, Korea Times, or Korea Herald before publishing.

## manifest.json — K-Wire Network auto-discovery

This repo carries a `manifest.json` at its root so it's automatically picked up by [K-Wire Network](https://fhzl0117-hue.github.io/), the directory hub for the whole "Wire" series. No manual edit to the hub repo is needed — its page fetches this file on every visit and lists this site automatically.

## Updating content

Everything is plain HTML — open `index.html` in any editor and look for the section with the matching `id` (e.g. `<section ... id="news">`) to update copy. There's no CMS yet; each dispatch, review, or signal-desk date is a hand-edited block. See the comments inside the `<script>` tag at the bottom for how the quiz and countdown/elapsed timers work if you need to change their logic — the Signal desk timer auto-detects whether a `data-target` date is in the future (shows "time left") or the past (shows "time since"), so it works either way without further edits.

**Before adding new dates or news items,** verify the underlying facts against a real source and keep the "Read the original source" link pointing at it — that link is what keeps this page compliant with content policies (Google AdSense does not allow re-publishing copyrighted material, and this page's whole design is built around linking out and summarizing instead of reposting).

**Before adding any new YouTube embed,** verify it against the official channel using the oEmbed check: fetch `https://www.youtube.com/oembed?url=https://www.youtube.com/watch?v=<ID>&format=json` and confirm `author_name` matches JYP Entertainment (or the relevant member's own verified channel) — a search result titled "Official M/V" is not proof by itself.

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.
