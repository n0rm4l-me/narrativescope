# NarrativeScope

> *"Google Translate translates language. NarrativeScope translates perspective."*

AI-powered tool that tracks how the same geopolitical event is reported across different media ecosystems — and explains where narratives diverge.

## Live Demo

**[→ View Demo](https://n0rm4l-me.github.io/narrativescope/)**

| Language | Demo | Pitch |
|---|---|---|
| English | [→ Demo](https://n0rm4l-me.github.io/narrativescope/) | [→ Pitch](https://n0rm4l-me.github.io/narrativescope/pitch-en.html) |
| Russian / Русский | [→ Демо](https://n0rm4l-me.github.io/narrativescope/demo-ru.html) | [→ Питч](https://n0rm4l-me.github.io/narrativescope/pitch-ru.html) |
| Chinese / 中文 | [→ 演示](https://n0rm4l-me.github.io/narrativescope/demo-zh.html) | [→ 提案](https://n0rm4l-me.github.io/narrativescope/pitch-zh.html) |

## The Problem

When a missile strikes a city, Russian state media, Ukrainian outlets, and Western sources describe the same event in entirely different ways — different facts, different framing, different omissions. Readers have no tool to understand these differences systematically.

## How It Works

```
RSS feeds (50+ sources)
        ↓
Keyword filter → drops ~85% of articles
        ↓
Event clustering via Vertex AI Embeddings
        ↓
Triggered when 3+ sources cover the same event
        ↓
Gemini analysis: shared facts / framing differences / omissions
        ↓
Multilingual output (EN, RU, ZH, DE, FR, UA)
```

## Example: Zaporizhzhia NPP Blackout — May 27, 2026

| Source | Framing | Omits |
|---|---|---|
| **Russian media** (TASS, RT) | Ukrainian strike caused the blackout | Russia controls the plant since 2022 |
| **Ukrainian media** (Ukrinform) | Consequence of Russian occupation | Alternative explanations |
| **Western media** (BBC, Reuters) | Under investigation, no attribution | Ground-level civilian impact |

**AI Summary:** All three cited the same IAEA statement — a rare convergence. But they diverge sharply on causation. Russia controls the plant yet frames itself as victim. Key divergence: occupier-vs-defender framing applied to the same physical infrastructure.

## Tech Stack

- **Google Cloud Run** — serverless event processing
- **Vertex AI Embeddings** — multilingual event clustering
- **Gemini 2.5 Pro / Flash** — narrative analysis and translation
- **Firestore** — database
- **Firebase Hosting + Cloud CDN** — frontend delivery
- **Next.js** — frontend framework

## Status

Prototype built and tested on real news data (May 27–29, 2026):
- ✅ 103 AI agents run in research test
- ✅ 21 sources fetched and cross-verified
- ✅ 6 high-confidence verified claims
- ✅ Live demo available

## Contact

Open to: grant, license, or acquisition.

Pitch for **Google News Initiative** — [full proposal](https://n0rm4l-me.github.io/narrativescope/pitch-en.html)
