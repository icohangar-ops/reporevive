# RepoRevive — Video Presentation (2:51) · Narration Script & Splice Guide

**File:** `RepoRevive_Video_Presentation.mp4` — 1920×1080, 30 fps, H.264 + AAC, 2:51
**Voice:** TTS `jam` @ 1.45× (regenerate anytime: `scripts/reporevive/tts_scenes.py`)
**Rebuild:** `scripts/reporevive/build_video.py` (scenes → concat)

## Scene timecodes

| # | Time | Slide | Narration |
|---|------|-------|-----------|
| 1 | 0:00–0:13 | Cover | Every codebase has a skeleton in the closet. RepoRevive — powered by IBM Bob 2.0 — audits legacy repositories, plans the fixes, and renovates your code, live. |
| 2 | 0:13–0:29 | Problem | Most of the world's software is legacy: outdated dependencies, hidden CVEs, near-zero test coverage, and architecture that lives only in the heads of developers who left. Static tools flood you with warnings — they can't prioritize, can't explain, and can't fix anything. |
| 3 | 0:29–0:48 | Solution | RepoRevive runs three orchestrated phases. Audit: the Inspector agent scores your repo's health from zero to one hundred. Plan: the Architect agent turns findings into a prioritized, verifiable backlog. Renovate: the Executor fixes issues while the Validator checks every change. |
| 4 | 0:48–1:05 | Phase 1 · Audit | The audit is evidence-based — tree-sitter AST analysis, dependency scanning, coverage and complexity metrics, documentation checks — merged into a transparent six-dimension score, with a risk heatmap ranking every file by churn, complexity, and test gap. |
| 5 | 1:05–1:19 | Phase 2 · Plan | The Architect converts the audit into a dependency-ordered backlog. Every task is small, verifiable, and carries acceptance criteria — with score points attached, so renovation never becomes a rewrite. |
| 6 | 1:19–1:34 | Phase 3 · Renovate | The Executor lands one task at a time, running builds and tests through its shell. The Validator reviews every diff. Watch the dashboard — as each task merges, the health score climbs. Progress you can measure, not guess. |
| 7 | 1:34–1:49 | Architecture | Under the hood: a Next.js dashboard, the GitHub API for ingestion, tree-sitter for parsing — and IBM Bob 2.0 orchestrating every agent, from clone to analysis to score to serve. |
| 8 | 1:49–2:09 | Bob 2.0 | Bob 2.0 is the brain. Agent mode drives full-repo reasoning. Parallel subagents audit dependencies, complexity, and docs at once. Document understanding reads lockfiles and CI configs. Four agents — Inspector, Architect, Executor, Validator — one orchestrated team. |
| 9 | 2:09–2:23 | Business value | Minutes of automated audit replace weeks of archaeology, and every fix carries score points — real ROI. For maintenance teams, agencies, and open-source maintainers, that's real time and real money. |
| 10 | 2:23–2:33 | Demo flow | In the live demo we paste a real repository, run the audit, approve a task, and renovate it — with the score climbing on screen. |
| 11 | 2:33–2:41 | 48-hour plan | Built in forty-eight hours by four builders — version one of the renovation platform legacy code deserves. |
| 12 | 2:41–2:51 | Closing | RepoRevive. Legacy code, revived. Find the public repo in our submission — and bring your codebase back to life. |

## ⚠️ Hackathon rule check — live demo requirement

The rules require the video to contain **≥ 90 seconds of real product demo**. This cut is a
narrated pitch (slides), so before final submission, splice in your screen recording:

1. **Record the demo** — 1920×1080 (or higher), 30 fps, mp4/mov:
   - Beat 1: paste a real GitHub URL → Inspector audit runs (activity feed + heatmap render)
   - Beat 2: Architect plan appears → approve one task
   - Beat 3: Executor lands the fix → health score climbs on the dashboard
2. **Send the recording back** — it gets spliced between scene 3 (0:48) and scene 9,
   replacing scenes 4–8 (≈ 80s) or trimming narration to hit the 90s demo floor:
   `0:00–0:48 pitch → 0:48–2:18 LIVE DEMO (90s) → 2:18–2:51 value + close`.
3. **Optional (recommended):** re-record the narration with a human voice using the exact
   script above — judges rate Presentation, and a team voice beats TTS.

## Assets used per scene

- Slide frames: `download/slides/png/slide_01..12.png` (2560×1440, 2× renders)
- Charts: `weights.png` (slide 4), `diagram.png` (slide 7)
- Narration WAVs: `scripts/reporevive/video/narr_01..12.wav`
