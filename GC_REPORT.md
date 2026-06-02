# SuperInstance Organization GC Audit Report

**Date:** 2026-06-02  
**Total Repositories:** 500  
**Auditor:** Automated audit via GitHub API

---

## Executive Summary

The SuperInstance org contains **500 repositories** — an exceptionally large portfolio. The majority (322, or 64%) are `lau-*` mathematics crates from a sprint. Another 29 are `plato-*` crates, 38 are forks of major projects, and the remainder are specialized standalone projects.

**Key findings:**
- **322 lau-\* repos** represent a massive maintenance surface with questionable external adoption
- **38 forks** of major projects represent significant sync burden (~90-120 hrs/month)
- **Multiple published packages** exist (npm + PyPI) — these must be preserved
- Several repo families duplicate functionality across language ports

---

## Inventory by Category

### 1. ACTIVE FORKS (38 repos)

All forks were updated within the last 48 hours, suggesting active upstream syncing. Many carry unique branches for guardian/conservation features.

| Repo | Parent | Unique Branches | Stars | Verdict |
|------|--------|-----------------|-------|---------|
| zed | zed-industries/zed | Custom branches | 0 | **KEEP** — active dev |
| typst | typst/typst | 0.6–0.10 version branches | 0 | **KEEP** — version tracking |
| ollama | ollama/ollama | Multiple custom branches | 0 | **KEEP** |
| ratatui | ratatui-org/ratatui | Feature branches | 0 | **KEEP** |
| chroma | chroma-core/chroma | Version + feature branches | 0 | **KEEP** |
| qdrant | qdrant/qdrant | RBAC, quantization branches | 0 | **KEEP** |
| tauri | tauri-apps/tauri | Version branches 1.x | 0 | **KEEP** |
| vite | vitejs/vite | Many feature branches | 0 | **KEEP** |
| bun | oven-sh/bun | Feature + fix branches | 0 | **KEEP** |
| astro | withastro/astro | Legacy version branches | 0 | **KEEP** |
| workers-rs | cloudflare/workers-rs | Cache, bugfix branches | 0 | **KEEP** |
| dify | langgenius/dify | Admin APIs, test branches | 0 | **KEEP** |
| next.js | vercel/next.js | Feature branches | 0 | **KEEP** |
| serde | serde-rs/serde | **guardian** branch | 0 | **KEEP** — unique guardian work |
| meilisearch | meilisearch/meilisearch | Feature branches | 0 | **KEEP** |
| deno | denoland/deno | Custom test branches | 0 | **KEEP** |
| weaviate | weaviate/weaviate | ACORN optimization branches | 0 | **KEEP** |
| foundry | foundry-rs/foundry | Agent branches, benchmarks | 0 | **KEEP** |
| lapce | lapce/lapce | **coverage-gap** branch | 0 | **KEEP** |
| tokio | tokio-rs/tokio | Patch branches | 0 | **KEEP** |
| surrealdb | surrealdb/surrealdb | CLI, parser branches | 0 | **KEEP** |
| open-webui | open-webui/open-webui | **budget-guardian** branch | 0 | **KEEP** — unique budget work |
| aider | paul-gauthier/aider | **budget-enforcer** branch | 0 | **KEEP** — unique budget work |
| uv | astral-sh/uv | Forking, benchmark branches | 0 | **KEEP** |
| supabase | supabase/supabase | Migration branches | 0 | **KEEP** |
| codex | openai/codex | Extensible tests, voice branches | 0 | **KEEP** |
| baml | boundaryml/baml | Parser, graph branches | 0 | **KEEP** |
| gno | gnolang/gno | Bench, chain branches | 0 | **KEEP** |
| axum | tokio-rs/axum | Spoofing fixes, release branches | 0 | **KEEP** |
| grpc-rust | hyperium/grpc-rust | Benchmark, tip branches | 0 | **KEEP** |
| ruview-cathedral | (unknown) | ESP32, submodule branches | 0 | **MAYBE** — niche |
| hermes-construct | (unknown) | main only | 0 | **MAYBE** |
| cocapn-go | (unknown) | main/master | 0 | **MAYBE** |
| OpenConstruct | (unknown) | main only | 0 | **MAYBE** |
| bid-engine | (unknown) | main only | 0 | **MAYBE** |
| ab-testing | (unknown) | master only | 0 | **MAYBE** |
| sia | (unknown) | main only | 0 | **MAYBE** |
| llvm-project | llvm/llvm-project | main only | 0 | **ARCHIVE** — massive repo, no unique branches |

### 2. ACTIVE STANDALONE (Published & High-Value)

These repos have **published packages** or unique utility. **Do not archive.**

| Repo | Registry | Stars | Description | Verdict |
|------|----------|-------|-------------|---------|
| symmetry-math | npm, PyPI | 0 | Symmetry group theory | **KEEP** |
| griot-math | npm | 0 | Living memory mathematics | **KEEP** |
| griot-math-pypi | PyPI | 0 | Python port of griot-math | **KEEP** |
| kintsugi-math | npm, PyPI | 0 | Error recovery mathematics | **KEEP** |
| quipu-math | npm, PyPI | 0 | Incan knotted cord data structures | **KEEP** |
| songline-math | npm | 0 | Navigable knowledge graphs | **KEEP** |
| adinkra-math | npm | 0 | Adinkra symbolic encoding | **KEEP** |
| rhythm-math (rhythm-nation-math) | npm, PyPI | 0 | Rhythm mathematics | **KEEP** |
| flux-index | PyPI | 0 | Semantic code search | **KEEP** |
| flux-algebra | PyPI | 0 | Music algebra | **KEEP** |
| superinstance-math | PyPI | 0 | Pure-Python ML math libraries | **KEEP** |

### 3. PLATO CRATES (29 repos)

PLATO room architecture components. All have 1-2 stars (likely internal). All updated 2026-06-01.

| Repo | Stars | Verdict |
|------|-------|---------|
| plato-config | 2 | **KEEP** — most starred, Python |
| plato-mythos | 2 | **KEEP** — Recurrent-Depth Transformer |
| plato-alert | 1 | **KEEP** |
| plato-anomaly | 1 | **KEEP** |
| plato-backtest | 1 | **KEEP** |
| plato-capability | 1 | **KEEP** |
| plato-compress | 1 | **KEEP** |
| plato-correlate | 1 | **KEEP** |
| plato-distill | 1 | **KEEP** |
| plato-downsample | 1 | **KEEP** |
| plato-embed | 1 | **KEEP** |
| plato-event | 1 | **KEEP** |
| plato-filter | 1 | **KEEP** |
| plato-health | 1 | **KEEP** |
| plato-history | 1 | **KEEP** |
| plato-jepa | 1 | **KEEP** |
| plato-metrics | 1 | **KEEP** |
| plato-nervous | 1 | **KEEP** |
| plato-normalize | 1 | **KEEP** |
| plato-predict | 1 | **KEEP** |
| plato-ring | 1 | **KEEP** |
| plato-route | 1 | **KEEP** |
| plato-schema | 1 | **KEEP** |
| plato-spectral | 1 | **KEEP** |
| plato-threshold | 1 | **KEEP** |
| plato-transform | 1 | **KEEP** |
| plato-validate | 1 | **KEEP** |
| plato-window | 1 | **KEEP** |
| plato-mythos-bridge | 0 | **KEEP** — bridge component |

**Recommendation:** PLATO crates form a coherent system. Keep as-is, but consider consolidating into a monorepo (plato-kernel) with workspace crates to reduce repo count by 28.

### 4. COCAPN CRATES (13 repos)

Marine/sensor integration system spanning multiple languages.

| Repo | Stars | Language | Verdict |
|------|-------|----------|---------|
| cocapn-core | 2 | Rust | **KEEP** — core engine |
| cocapn-ada | 0 | Ada | **KEEP** — unique language port |
| cocapn-c | 0 | C | **KEEP** — bare metal |
| cocapn-escalation | 0 | Rust | **KEEP** |
| cocapn-forth | 0 | Forth | **KEEP** — unique |
| cocapn-lua | 0 | Lua | **KEEP** |
| cocapn-marine | 0 | Makefile | **KEEP** |
| cocapn-pushdown | 0 | Makefile | **KEEP** |
| cocapn-python | 0 | Python | **KEEP** |
| cocapn-wasm | 0 | Rust | **KEEP** |
| cocapn-zig | 0 | Zig | **KEEP** |
| cocapn-explain | 1 | Python | **KEEP** — agent explainability |
| cocapn-go (fork) | 1 | Go | **KEEP** |

### 5. LAU-* MATHEMATICS CRATES (322 repos)

The largest category. These were created during a mathematics sprint (all updated 2026-06-01). 

**Key stats:**
- 96 lau-* repos have 1 star (likely all internal/self-starred)
- 226 lau-* repos have 0 stars
- No evidence of external adoption or published packages
- All appear to be educational/research code

**Representative sample (with stars):**

| Repo | Stars | Topic |
|------|-------|-------|
| lau-leaderboard | 1 | Leaderboard system |
| lau-tutorial | 1 | Tutorial framework |
| lau-mission | 1 | Mission system |
| lau-construct | 1 | Construct framework |
| lau-blueprint | 1 | Blueprint system |
| lau-constellation | 1 | Constellation mapping |
| lau-ai-tutor | 1 | AI tutoring |
| lau-shell-kernel | 1 | Shell kernel |
| lau-vibe-compiler | 1 | Vibe compilation |
| lau-trading | 1 | Trading system |
| lau-weather | 1 | Weather |

**...and 312 more.**

#### LAU-* Sub-Categories

**Shell ecosystem (~15 repos):** lau-shell-kernel, lau-shell-interface, lau-shell-transport, lau-shell-lifecycle, lau-shell-spawn, lau-inter-shell, etc.

**Agent ecosystem (~10 repos):** lau-agent-shell, lau-agent-runtime, lau-agent-profile, lau-agent-unify, etc.

**Pure mathematics (~60 repos):** lau-algebraic-topology, lau-differential-topology, lau-algebraic-geometry, lau-sheaf-cohomology, lau-hodge-theory, lau-lie-algebra, etc.

**Applied domains (~30 repos):** lau-fluid-dynamics, lau-electromagnetism, lau-thermodynamics, lau-relativity, lau-robotics, etc.

**Infrastructure (~20 repos):** lau-bytecode, lau-construct-cli, lau-wasm-bridge, lau-ts-bridge, lau-tick-runtime, etc.

**Creative/experimental (~15 repos):** lau-vibe-field, lau-vibe-visualizer, lau-tensor-midi, lau-simd-vibe, etc.

### 6. OTHER STANDALONE REPOS

| Repo | Stars | Updated | Verdict |
|------|-------|---------|---------|
| SuperInstance | 4 | 2026-06-02 | **KEEP** — org profile, most starred |
| webgpu-profiler | 2 | 2026-05-29 | **KEEP** — unique utility |
| cocapn-core | 2 | 2026-06-02 | **KEEP** — listed above |
| AI-Writings | 1 | 2026-06-02 | **KEEP** — creative writing |
| SmartCRDT | 1 | 2026-05-29 | **KEEP** — CRDT research |
| superinstance-wiki | 1 | 2026-06-02 | **KEEP** — knowledge base |
| casting-call | 1 | 2026-06-01 | **KEEP** — model capabilities DB |
| conservation-checker | 1 | 2026-06-02 | **KEEP** |
| polln | 1 | 2026-05-29 | **KEEP** — visualization |
| .github | 0 | 2026-06-01 | **KEEP** — org profile |
| conservation-guardian | 0 | 2026-06-02 | **KEEP** |
| conservation-thesis | 0 | 2026-06-02 | **KEEP** |
| harness-toolkit | 0 | 2026-06-02 | **KEEP** |
| lever-runner | 0 | 2026-06-02 | **KEEP** |
| pincherOS | 0 | 2026-06-02 | **KEEP** |
| fleet-map | 0 | 2026-06-02 | **KEEP** |
| spacedrive | 0 | 2026-06-02 | **KEEP** |
| spacedrive-fleet | 0 | 2026-06-02 | **KEEP** |
| spacemap | 0 | 2026-06-02 | **KEEP** |
| negative-space-testing | 0 | 2026-06-02 | **KEEP** |
| crackle-runtime | 0 | 2026-06-02 | **KEEP** |
| iii-observability | 0 | 2026-06-02 | **KEEP** |
| token-wavelet | 0 | 2026-06-02 | **KEEP** |
| graphite-geometric-algebra | 0 | 2026-06-02 | **KEEP** |
| ecosystem-thesis | 0 | 2026-06-02 | **KEEP** (private) |
| fork-strategy-doc | 0 | 2026-06-02 | **KEEP** (private) |
| dify-budget-watchdog | 0 | 2026-06-02 | **KEEP** (private) |
| lever-runner-synthesis | 0 | 2026-06-02 | **KEEP** (private) |
| codex-budget-guard | 0 | 2026-06-02 | **KEEP** |
| rig-budget-guard | 0 | 2026-06-02 | **KEEP** |
| uv-cache-guardian | 0 | 2026-06-02 | **KEEP** |
| ratatui-spectral-dashboard | 0 | 2026-06-02 | **KEEP** |
| lapce-coverage-gap | 0 | 2026-06-02 | **KEEP** |
| screenpipe-conservation | 0 | 2026-06-02 | **KEEP** |
| liteparse-coverage | 0 | 2026-06-02 | **KEEP** |
| herdr-cocapn | 0 | 2026-06-02 | **KEEP** |
| handy-marine-voice | 0 | 2026-06-02 | **KEEP** |
| cathedral-probe | 0 | 2026-06-02 | **KEEP** |

### 7. LUAU-* GAME ENGINE REPOS (11 repos)

| Repo | Stars | Verdict |
|------|-------|---------|
| luau-math | 0 | **KEEP** — core math |
| luau-audio | 0 | **KEEP** |
| luau-biome | 0 | **KEEP** |
| luau-conservation | 0 | **KEEP** |
| luau-demo | 0 | **KEEP** |
| luau-genealogy | 0 | **KEEP** |
| luau-git-world | 0 | **KEEP** |
| luau-quest | 0 | **KEEP** |
| luau-recipe | 0 | **KEEP** |
| luau-scheduler | 0 | **KEEP** |
| luau-spatial | 0 | **KEEP** |

### 8. MULTI-LANGUAGE PORT FAMILIES

Several math libraries have been ported to multiple languages (C, TypeScript, Python, WASM):

- **griot-math:** npm + pypi + C + WASM (4 repos)
- **kintsugi-math:** npm + pypi + C + WASM (4 repos)
- **quipu-math:** npm + pypi + C + WASM (4 repos)
- **songline-math:** npm + pypi + C + WASM (4 repos)
- **adinkra-math:** npm + pypi + C (3 repos)
- **symmetry-math:** npm + pypi + C (3 repos)
- **palaver-math:** npm + pypi + C (3 repos)
- **rhythm-math:** npm + C (2 repos, also rhythm-nation-math on pypi)
- **openconstruct:** modular + catalog (2 repos)

All **KEEP** — these are published packages.

---

## Archive Recommendations

### HIGH CONFIDENCE — Archive These

| Repo | Reason |
|------|--------|
| llvm-project | Massive fork (~1GB+), no unique branches, no modifications. Extreme sync burden for zero value. |

### MODERATE CONFIDENCE — Consider Archiving

| Repo | Reason |
|------|--------|
| ab-testing | Fork, master only, no description, no unique content visible |
| bid-engine | Fork, main only, no description, no visible modifications |
| sia | Fork, main only, unclear purpose |

### LAU-* MASSIVE CONSOLIDATION OPPORTUNITY

**The 322 lau-* repos are the biggest GC opportunity.** Recommendations:

1. **IMMEDIATE:** Archive the ~226 lau-* repos with 0 stars and no published packages. These are pure sprint artifacts.

2. **SHORT-TERM:** Consolidate the remaining ~96 lau-* repos with 1 star into thematic monorepos:
   - `lau-mathematics` — all pure math crates (algebraic topology, geometry, number theory, etc.)
   - `lau-physics` — all applied physics crates (fluid dynamics, electromagnetism, etc.)
   - `lau-shell` — shell ecosystem (kernel, interface, transport, lifecycle, spawn, inter-shell)
   - `lau-agents` — agent ecosystem (shell, runtime, profile, unify)
   - `lau-infrastructure` — bytecode, CLI, bridges, runtimes
   - `lau-creative` — vibe-*, tensor-midi, visualizer, etc.

3. This would reduce 322 repos to ~6 monorepos.

---

## Consolidation Opportunities

### 1. PLATO → Monorepo (29 → 1)
Merge all 29 plato-* crates into a single `plato-kernel` monorepo with workspace crates. They form a coherent system and are all updated simultaneously.

### 2. LAU-* → Thematic Monorepos (322 → ~6)
See above. The lau-* repos are clearly sprint-generated and would benefit from consolidation.

### 3. Multi-language Math Ports → Per-Library Monorepos
Each math library (griot, kintsugi, quipu, songline, adinkra, symmetry, palaver, rhythm) has 2-4 language-specific repos. Merge each family into one repo with language subdirectories.

Example: `griot-math` repo with `/ts`, `/python`, `/c`, `/wasm` directories instead of 4 separate repos.

This would reduce ~27 repos to ~8.

### 4. Guardian/Budget Tools → Single Repo
Several repos are small budget/guardian utilities:
- codex-budget-guard
- dify-budget-watchdog
- rig-budget-guard
- uv-cache-guardian
- gem-conservation-guardian
- gem-render-guardian
- gem-storage-guardian

These could consolidate into a `guardian-toolkit` monorepo.

---

## Maintenance Burden Estimate

### Fork Sync Burden
**38 active forks** of major projects require continuous upstream syncing.

- **Per fork, per month:** ~2-3 hours (reading changelogs, resolving conflicts, testing unique branches)
- **Total monthly estimate:** 76-114 hours/month for fork maintenance alone
- **With automation (Renovate/Dependabot):** Could reduce to ~30-40 hours/month

### LAU-* Burden
322 repos with no automation = significant CI/CD cost, even if just running Dependabot scans.

---

## Summary Decision Table

| Category | Count | Action | Impact |
|----------|-------|--------|--------|
| Active Forks | 38 | KEEP (archive llvm-project) | -1 repo |
| PLATO Crates | 29 | KEEP (consider monorepo) | 0, future -28 |
| COCAPN Crates | 13 | KEEP | 0 |
| Luau Crates | 11 | KEEP | 0 |
| Multi-lang Math Ports | ~27 | KEEP (consider merging) | 0, future -19 |
| Published Packages | ~11 | KEEP (non-negotiable) | 0 |
| Other Standalone | ~40 | KEEP | 0 |
| lau-* 0-star repos | ~226 | **ARCHIVE** | -226 repos |
| lau-* 1-star repos | ~96 | KEEP (consolidate) | 0, future -90 |
| Forks to archive | 1-4 | **ARCHIVE** | -1 to -4 |

### Immediate Actions (Low Risk)
1. **Archive `llvm-project`** — no unique content, massive repo
2. **Archive ~226 lau-* repos with 0 stars** — pure sprint artifacts
3. **Set up Renovate** for the 38 forks to automate sync

### Medium-Term Actions
4. **Consolidate PLATO** into monorepo
5. **Consolidate lau-*** into thematic monorepos
6. **Merge multi-language ports** into per-library repos

### Potential Reduction
- **Immediate:** 227-230 repos archived → **270 remaining**
- **After consolidation:** ~190-200 repos → much more manageable

---

*Report generated 2026-06-02 by automated GC audit.*
