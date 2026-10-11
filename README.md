# NEAT-TTS project page

Live site: https://neat-tts.github.io/

Built on the [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template)
(same layout as the Resonate / MeanAudio project pages). Static HTML, no build step.

## Layout

```
index.html                  # hero / teaser / Overall Architecture / Main Results / footer
.nojekyll                   # disables Jekyll so static/ is served as-is
static/css, static/js       # template assets (all local)
static/images/              # put figures here
static/audio/               # audio samples (not shown on the page yet)
```

## Filling in the placeholders

| Placeholder | Where |
| --- | --- |
| Title, authors, affiliations | hero section in `index.html` |
| arXiv / Code links | `publication-links` block (`href="#"` for now) |
| Teaser figure | `static/images/fig1_teaser.png`, then replace the `.ph-note` block with an `<img>` |
| Architecture figure | `static/images/fig2_architecture.png`, same as above |
| Results table | `results-table` in the Main Results section |
| Social card | `static/images/og.png` (1200x630) |

## Audio

Do not commit large audio files. GitHub Pages does not support Git LFS and caps single files at 100 MB.
Encode samples as mono mp3/opus (64–96 kbps) before committing; host large sets on HuggingFace or GitHub Releases.

## Publishing

Push to `main`. Pages builds from `main` / root in about 10–60 seconds.
