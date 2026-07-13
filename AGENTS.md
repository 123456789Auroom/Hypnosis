# HypnoGrowth Agent — Development Guide

## Overview

AI-driven growth agent for Ишвара даса hypnotherapy practice.
Handles: SEO, content creation, social media, landing pages, competitor research, checklists, email campaigns.

## Architecture

```
HypnoGrowth/
├── SOUL.md                  # Agent persona & voice
├── AGENTS.md                # This file
├── README.md                # How to use
├── context/                 # Client context (brand, services, clients)
│   ├── about-me.md          # Ишвара даса bio & approach
│   ├── brand-voice.md       # Tone, style, do/don't
│   ├── ideal-client.md      # ICP, pain points, objections
│   ├── services.md          # Services, pricing, process
│   ├── competitor-analysis.md # Market & competitor data
│   ├── seo-keywords.md      # Keyword research
│   └── content-calendar.md  # 90-day content plan
├── content/                 # Published content
│   ├── blog/                # SEO articles
│   ├── social/              # Telegram, Instagram posts
│   ├── checklists/          # Lead magnets (PDF-ready)
│   ├── landing/             # Landing page HTML/CSS
│   ├── email/               # Email sequences
│   └── forum/               # Forum posts (VC.ru, Пикабу, etc.)
└── research/                # Research output
    └── keywords/            # Keyword analysis results
```

## Agent Config

Load `SOUL.md` as system prompt for all content tasks.
Load context files from `context/` as needed per task.

## Key Skills

| Skill | Purpose |
|-------|---------|
| `ai-seo` | SEO strategy, keyword targeting, AI Overviews optimization |
| `content-to-pipeline` | Content → leads → sales pipeline |
| `social-media-content-system` | Post creation, hooks, content calendar |
| `claude-design` | Landing page HTML/CSS |
| `popular-web-designs` | Design system references |
| `taste-skill-frontend-design` | Anti-slop design standards |
| `humanizer` | Remove AI-sounding language |
| `positioning-icp` | Positioning & ICP refinement |
| `deep-research` | Competitor/market research |
| `web-quality-audit` | Website quality audit |
| `social-selling` | Social selling strategy |
| `sketch` | Quick design mockups |

## External Tools

- **OpenSERP** — self-hosted SERP API (Google, Yandex, Bing)
  - Docker: `docker run -p 7000:7000 karust/openserp`
  - API: `http://localhost:7000/search?q=...`
- **Kimi WebBridge** — real browser automation (Chrome)
- **GitHub Pages / Netlify** — free hosting for landing page

## Content Pipeline

### SEO Article
1. Research keyword (OpenSERP)
2. Analyze top-5 results
3. Write article (SOUL.md voice + brand-voice.md rules)
4. Add H2/H3 structure for AI Overviews
5. Add CTA at the end
6. Publish to blog/

### Telegram Post
1. Choose topic from content-calendar.md
2. Write hook (first line must stop scroll)
3. Write pain → recognition → insight → action
4. Add CTA
5. Publish to Telegram channel

### Checklist
1. Identify pain point from ideal-client.md
2. Write 5-7 actionable items
3. Make it useful even without booking
4. Add CTA at the bottom
5. Format as PDF-ready markdown

## Quality Checklist (for every piece)

- [ ] Does it start with pain, not credentials?
- [ ] Is it in client's language?
- [ ] Does it avoid "airy" or "fluffy" language?
- [ ] Does it have a clear CTA?
- [ ] Would you read this at 3am if you couldn't sleep?
- [ ] Is medical disclaimer at the bottom (if needed)?
- [ ] Is it anonymous (no real name, no face)?

## First 7 Days Checklist

- [ ] Landing page (mobile-first, free hosting)
- [ ] Telegram channel (first 5 posts)
- [ ] Checklist #1: "5 signs you need a hypnotherapist"
- [ ] First SEO article: "What is hypnotherapy"
- [ ] Second SEO article: "Hypnosis for anxiety"
- [ ] Register on VC.ru + Пикабу + Дзен
- [ ] First forum post

## Marketing Philosophy

**Position:** Premium hypnotherapy for people who've tried "regular" therapy and didn't get results.
**Price:** 30 000 ₽+ filters out non-serious clients. This is a feature, not a bug.
**Channel:** Telegram + SEO. No paid ads until organic proves the funnel works.
**Content:** Quality > quantity. 3 great checklists > 10 mediocre ones.
