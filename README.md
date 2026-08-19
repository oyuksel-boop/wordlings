# Isabel Leyla's Wordlings

A gentle spelling game for long words, built for a P5 pupil in Scotland who finds
multisyllabic words tricky. No scores, no timers, no way to lose — every word you
spell hatches a little creature that lives on your island.

**Play:** https://USERNAME.github.io/REPO/ *(replace once Pages is live)*

## How it works

Each word is met twice:

1. **Put the chunks in order** — the whole word is shown and read aloud first, with
   the tricky bits (double letters, `-tion`, `-ough`) underlined. Then it hides and
   the syllable chunks come back shuffled.
2. **Spell it, chunk by chunk** — next time the same word comes round, it's letter
   tiles instead: only the letters of the current chunk plus two distractors, so a
   14-letter word is never faced all at once.

Support is always available and never penalised: 👀 shows the word for two seconds,
🔊 repeats it, 🐢 says it one chunk at a time. After two wrong taps the right piece
starts to glow.

This follows the evidence on multisyllabic words: chunk by vowels and morphemes
rather than rigid syllable rules, teach affixes explicitly, gamify the practice,
and always show the word in a sentence.

## Word packs

| Pack | Contents |
| --- | --- |
| Two-Chunk Town | 2-chunk words — *because, mountain, biscuit* |
| Three-Chunk Forest | 3-chunk words — *different, adventure, dinosaur* |
| Four-Chunk Mountain | 4-chunk words — *information, temperature, caterpillar* |
| Giant Word Sea | 5+ chunks — *imagination, responsibility, pronunciation* |
| Word Builder Lab | prefixes and suffixes — *un-*, *re-*, *mis-*, *-ful*, *-less*, *-ness* |
| My Own Words | whatever a grown-up adds |

All spellings are UK/Scottish (*colour, centre, organisation, favourite*).

## For grown-ups

The ⚙️ button on the front page opens a panel where you can:

- add this week's school spelling words (`ex-cel-lent`; leave the split blank and it
  guesses the syllables)
- change the reading voice and speed
- see which words are being found hardest

Progress is stored in the browser's local storage on that device only. Nothing is
sent anywhere, and there is no analytics, no account and no network call after the
page loads.

## Install on a phone

Open the link in Chrome → menu → **Add to Home screen**. It then runs full-screen
and works offline.

On Android, the spoken words need a text-to-speech voice installed:
*Settings → Additional settings → Languages & input → Text-to-speech output →
Google Text-to-speech → English (United Kingdom)*.

## Files

- `index.html` — the whole game, single file, no build step and no dependencies
- `manifest.webmanifest`, `sw.js`, `icon-*.png` — what makes it installable and offline-capable

To change the word list, edit the `WORDS` array near the top of the `<script>` block
in `index.html`. The format is `["word", "chunk|chunk|chunk", "A sentence.", "packId"]`.
Bump `CACHE` in `sw.js` after any edit so phones pick up the new version.
