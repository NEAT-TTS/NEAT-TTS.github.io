# NEAT-TTS demo page

Live site: https://neat-tts.github.io/

Same layout as the [F5-TTS](https://swivid.github.io/F5-TTS/) and [WavTTS](https://wavtts.github.io/) demo pages
(Bootstrap 5.1.3 + `custom.css` / `normalize.css`, copied byte-for-byte). Static HTML, no build step.

## Layout

```
index.html          # title / Model Overview / EN & ZH zero-shot / Main Results / Ablation Studies
.nojekyll           # disables Jekyll
css/                # bootstrap.min.css, custom.css, normalize.css
figs/overview.png   # Figure 1 (model overview, rendered from NEAT_TTS_Model.pdf p.1)
figs/gema_induced_velocity.png  gema_flow_ratio.png  inference_schedule.png  cfg_strength_zh.png
audios/en/prompt/NN.wav   audios/en/gen/NN.wav
audios/zh/prompt/NN.wav   audios/zh/gen/NN.wav
```

## Placeholders

Missing audio files and figures are shown as dashed filename blocks. Drop the file at the shown path
and refresh; no code changes needed.

| Placeholder | Where |
| --- | --- |
| Code / Paper links | commented-out `<h5>` line under the subtitle (hidden during anonymous review) |
| Target text | `Text` column of each table |
| Audio | 5 rows x (prompt, gen) x (en, zh) = 20 files |

To add a section (e.g. cross-lingual, speed control, baselines), copy one `shadow-lg` card,
give the `<h2>` a new `id`, and add it to the Contents list.

## Audio

GitHub Pages does not support Git LFS and caps single files at 100 MB. Keep samples short;
if you switch to mp3, update the `src` / `data-file` extensions too.

## Publishing

Push to `main`. Pages builds from `main` / root in about 10–60 seconds.
