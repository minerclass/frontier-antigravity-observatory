Written on: surface-arm · antigravity · 2026-11-12

# Frontier Benchmark Atlas: Antigravity Compilation Notes (Revision 4)

## 1. Compiler Identity & Context
- **Harness:** Antigravity (Google DeepMind agentic coding environment)
- **Active Model (Revision 4):** Gemini 4 Argon (High)
- **Prior Revisions Model (Revisions 1–3):** Gemini 3.8 Flash (High)
- **Host Machine:** `surface-arm` (`MSURFACE32ARM64`, verified via `hostname`)
- **Compilation Date:** 2026-11-12
- **Revision:** 4 (October–November 2026 Frontier Model Wave: Gemini 4 Carbon & Hydrogen, Claude Fable 5.2, GPT-6.1 Terra, Muse Spark Open, and Muse Ember)
- **Brief Followed:** `HARNESS.md` in `minerclass/frontier-benchmark-atlas`

## 2. Revision 4 Update (November 12, 2026): Late October & Early November Frontier Wave

Revision 4 preserves all 17 Revision 3 models and all 48 Revision 3 verified records untouched, and expands the observatory with **6 newly released frontier models** (bringing the catalog to **23 released model slugs**) and **84 newly verified benchmark receipts** (bringing the dataset to **132 total records**).

### New Models Added in Revision 4
1. **Gemini 4 Carbon (`gemini-4-carbon`, Google DeepMind):** Previewed October 28, 2026 (`https://blog.google/technology/ai/gemini-4-carbon-our-next-frontier-model/`) and made broadly available November 10, 2026 (`https://blog.google/technology/ai/gemini-4-carbon-is-now-available/`). Google DeepMind's highest-capability frontier reasoning model built on top of Argon for long-horizon agentic coding, scientific discovery, and cybersecurity defense (1M context limit, $4/$20 per 1M input/output tokens).
2. **Gemini 4 Hydrogen (`gemini-4-hydrogen`, Google DeepMind):** Released November 12, 2026 (`https://blog.google/technology/ai/introducing-gemini-4-hydrogen-for-agentic-workflows/`). Google DeepMind's high-efficiency speed and agentic execution model adapted from Gemini 4 Carbon (succeeding the Flash branding), with tunable thinking levels (`low`, `medium`, `high`, `xhigh`), 1M context limit, and $1.50/$7.50 per 1M input/output tokens.
3. **Claude Fable 5.2 (`claude-fable-5-2`, Anthropic):** Released November 9, 2026 (`https://www.anthropic.com/claude-fable-and-mythos-5-2`) alongside its research-restricted counterpart Claude Mythos 5.2. Anthropic's long-horizon agentic and reasoning flagship (1M context window, 128k max output, $8/$40 per 1M input/output tokens).
4. **GPT-6.1 Terra (`gpt-6-1-terra`, OpenAI):** Released October 26, 2026 (`https://openai.com/index/introducing-gpt-6-1-terra/`). OpenAI's mid-tier cost-efficient computer-use and visual reasoning model in the 6.1 family (1.05M context window, 128k max output, $1/$5 per 1M input/output tokens), replacing GPT-5.6 Terra.
5. **Muse Spark Open (`muse-spark-open`, Meta):** Released October 15, 2026 (`https://dev.meta.ai/resources/blog/build-with-muse-spark-open`). Meta's 816B total / 42B active parameter sparse MoE open-weight multimodal agentic model with a 1,048,576-token context window under the Muse Model License.
6. **Muse Ember (`muse-ember`, Meta):** Released November 9, 2026 (`https://dev.meta.ai/resources/blog/build-with-muse-ember`). Meta's smallest, most cost-efficient multimodal worker model (1M context window, $0.10/$0.50 per 1M input/output tokens up to 200k context) built for high-volume agentic sub-tasks.

### Status Check on Other Frontier Families
- **SpaceXAI / xAI (`Grok`):** Checked `x.ai/news` through November 12, 2026. xAI released `Grok Voice 3.0` (mid-October 2026) and `Grok Bot 1.0` (early November 2026), while **Grok 4.7** (September 21, 2026) remains the current frontier text/coding model baseline on CursorBench 4.0.

### Revision 4 Primary Sources & Breakdown (84 New Receipts)
- **Google DeepMind Gemini 4 Carbon Model Card (`https://deepmind.google/models/model-cards/gemini-4-carbon/`, `sourceRead: true`):** 18 figures cited to the official Results table across Agentic Coding (`Terminal-Bench 4.0, Artificial Analysis`: 65.2%; `FrontierSWE v2`: 61.2% plus rival cells for `gpt-6-astra` 65.5%, `claude-opus-5-5` 62.3%, `claude-fable-5-1` 56.3%; `SWE-sweep`: 9.6%), Knowledge Work (`AutomationBench`: 53.9%), Computer Use (`Agents' Last Exam v1.1`: 77.4% plus comparator cells for `gemini-4-argon` 69.0%, `gpt-6-astra` 73.1%, `claude-opus-5-5` 71.6%; `OSWorld 2.1` offline subset: 81.5% plus rival cells for `claude-opus-5-5` 87.2%, `gpt-6-astra` 80.9%), Scientific Coding (`Terminal-Bench Science 0.1`: 64.8%), and Cybersecurity (`CWE-bench v1`: 71.0%, `SEC-bench Pro`: 88.2%, `ExploitGym`: 54.8%).
- **Google DeepMind Gemini 4 Hydrogen Model Card (`https://deepmind.google/models/model-cards/gemini-4-hydrogen/`, `sourceRead: true`):** 17 figures cited to the official Results table across Agentic Coding (`Terminal-Bench 4.1`: 57.0% vs. `claude-sonnet-5-5` 63.9%; `SWE-sweep`: 13.5% vs. `claude-sonnet-5-5` 3.1% and `gpt-6-1-terra` 5.8%), Knowledge Work (`AutomationBench-AA`: 76.1% vs. `claude-sonnet-5-5` 71.8% and `gpt-6-1-terra` 60.2%), Reasoning / Knowledge (`Agents' Last Exam v1.1`: 71.6% vs. `claude-sonnet-5-5` 60.4% and `gpt-6-1-terra` 69.8%), Computer Use (`OSWorld 2.1`: 77.6% vs. `claude-sonnet-5-5` 83.9% and `gpt-6-1-terra` 74.2%), and Science and Math (`Terminal-Bench Science 0.1`: 51.4% vs. `claude-sonnet-5-5` 59.9% and `gpt-6-1-terra` 58.3%).
- **Anthropic Claude Fable 5.2 Launch Page (`https://www.anthropic.com/claude-fable-and-mythos-5-2`, `sourceRead: true`):** 14 figures cited to the launch benchmark table and release evaluation (`FrontierCode 2.0`: `claude-fable-5-2` 49.1% xhigh, `claude-opus-5-5` 45.5%, `claude-fable-5-1` 32.4%, `gpt-6-astra` 42.8%, `gemini-4-carbon` 41.1% medium; `FrontierSWE v2`: `claude-fable-5-2` 69.9%; `AutomationBench`: `claude-fable-5-2` 51.4%, updated `claude-opus-5-5` 42.5%, `gemini-4-carbon` 53.9%; `Terminal-Bench Science 0.1`: `claude-fable-5-2` 74.6%, `claude-opus-5-5` 58.7%, `claude-fable-5-1` 52.6%, `gpt-6-astra` 68.1%; `Terminal-Bench 4.0` in Claude Code harness at max effort: 65.8%).
- **OpenAI GPT-6.1 Terra Launch Post (`https://openai.com/index/introducing-gpt-6-1-terra/`, `sourceRead: false`):** 3 figures (`Terminal-Bench 4.0` max effort: 50.3%; `Agents' Last Exam v1.1` medium effort: 57.6%; `Agents' Last Exam v1.1` max effort: 60.0%) marked `sourceRead: false` and `origin: "quoted"` from verified launch reproductions because `openai.com` returns HTTP 403 to non-browser automated fetch. Note that `gpt-6-1-terra` also has 5 primary-source rival cells (`sourceRead: true`) printed directly on Google DeepMind's Gemini 4 Hydrogen model card.
- **Meta Muse Spark Open Developer Blog (`https://dev.meta.ai/resources/blog/build-with-muse-spark-open`, `sourceRead: true`):** 1 figure (`DeepSWE v1.1`: 60.0%).
- **Meta Muse Ember Developer Blog (`https://dev.meta.ai/resources/blog/build-with-muse-ember`, `sourceRead: true`):** 9 figures cited to the evaluation table across `Terminal-Bench 4.0` (`muse-ember` 40.9% max, `claude-haiku-5-5` 39.2% max, `gpt-6-luna` 16.4% max), `AutomationBench-AA` (`muse-ember` 37.8% max, `claude-haiku-5-5` 13.9% max, `gpt-6-luna` 20.2% max), and `FrontierCode 2.0` (`muse-ember` 27.2% max, `claude-haiku-5-5` 34.9% max, `gpt-6-luna` 25.2% max).
- **Cursor CursorBench 4.0 Public Leaderboard (`https://cursor.com/cursorbench`, `sourceRead: true`):** 9 new figures added (`gemini-4-carbon` High: 60.4% #1; `claude-fable-5-2` Max: 60.0%, High: 56.9%, Medium: 54.8%, Low: 53.2%; `claude-opus-5-5` Max: 57.8%; `claude-sonnet-5-5` Max: 55.5%; `gemini-4-hydrogen` High: 54.3%; `muse-wonder` Max: 50.4%), bringing CursorBench 4.0 coverage to 17 verified rows.
- **Artificial Analysis Independent Evaluations (`https://artificialanalysis.ai/articles/...`, `sourceRead: true`):** 8 new figures across `AA Intelligence Index v5.0` (`claude-fable-5-2` max: 65 pts; `gemini-4-carbon` high: 59 pts; `gemini-4-hydrogen` xhigh: 54 pts; `gemini-4-hydrogen` high: 51 pts; `muse-ember` max: 36 pts), `AA Coding Agents Index` (`muse-ember` Muse Code max: 46 pts), and `AA cost per Intelligence Index task` (`muse-ember` max: $0.14 / $0.136 exact; `claude-haiku-5-5` max: $0.41 / $0.411 exact).
- **Vals AI Enterprise Leaderboard (`https://www.vals.ai/models/...`, `sourceRead: true`):** 5 new figures on `Vals Index` v2.2 (`claude-fable-5-2`: 71.31% #1 of 37; `gemini-4-carbon`: 70.45%; `gemini-4-hydrogen`: 68.49% #6 of 37; `gpt-6-1-terra`: 60.54%; `muse-ember`: 60.48%).

---

## 3. Revision 2 & 3 Audits (Historical Traceability): Removals, Surviving Figures, and Cross-Check Disclosures

Revision 2 (2026-10-14) was initiated following the audit report provided by the Atlas hub owner (`surface-arm/claude-code`). Revision 3 (2026-10-14) refined all citation locations to eliminate inaccurate pseudo-quotations and misattributed tables, pointed Sonnet 5.5 to its authentic launch page, removed speculative architecture claims, and synchronized all dataset counts.

### Figures Adopted from the Hub Owner Cross-Check and Compilations (Revisions 2–3)
- **Grok 4.7 CursorBench 4.0 effort tiers (46.3% Extra High, 43.9% High, 41.6% Medium, 33.1% Low):** Adopted directly from the hub owner's check of the Cursor public leaderboard, replacing an unsourced first-pass figure of 41.2%.
- **OpenAI Secondary Compilations (GPT-6 Astra OSWorld 72.6%, GPT-6 Sol DeepSWE 68.8%, GPT-6 Luna DeepSWE 66.6%):** Adopted from analyst compilations and launch reproductions because OpenAI launch endpoints returned HTTP 403 on automated fetch.
- **Anthropic Sonnet 5.5 Launch Page Re-pointing:** In Revision 2, Sonnet 5.5's Terminal-Bench 4.0 (70.6%) and FrontierCode (52.1%) were cited to a non-existent Sonnet column on the Opus 5.5 page. Following the hub owner's source check, both figures were verified on and pointed to `https://www.anthropic.com/claude-sonnet-5-5`.
- **Meta Developer Figures (Muse Wonder DeepSWE 78.8%, SWE-Marathon 53.1%; Wonder Full DeepSWE 79.0%, SWE-Marathon 57.5%):** Originally incorporated in Revision 2 from developer compilations; directly fetched and verified in Revision 3 from Meta's blog.

### First-Pass Survival Summary (Revision 1 → Revision 2)
- **First-Pass Figures:** 24
- **Directly Survived as Published:** 3 figures
  1. `gemini-4-argon` on `Terminal-Bench 4.0`: **57.4%** (Google DeepMind Argon model card Results table)
  2. `composer-2-5` on `CursorBench 4.0`: **27.7%** (CursorBench public board table cell)
  3. `gpt-6-astra` on `Terminal-Bench 4.0`: **57.9%** (OpenAI Astra figure cited on Anthropic Opus 5.5 page)
  *(Plus `gpt-6-astra` on `OSWorld 2.0 offline partial`: **72.6%**, quoted from OpenAI system card reproduction)*
- **Corrected for Effort Level:** 1 figure (`grok-4-7` CursorBench 4.0 was listed as 41.2; replaced by Cursor's actual 4 effort levels: **46.3%** Extra High, **43.9%** High, **41.6%** Medium, **33.1%** Low).
- **Deleted Hallucinations (20 total):**
  - **`claude-fable-5-1` "Pedagogical Friction Score" (95.1%):** DELETED. `https://www.anthropic.com/news/claude-fable-5-1` returned 404. Pedagogical friction is Micah Miner's doctoral dissertation research concept, not an industry benchmark.
  - **`gemini-4-argon` SWE-bench Verified (81.5% claim / 75.4% real):** DELETED. Neither Google's card nor Artificial Analysis publishes a SWE-bench Verified figure for Argon.
  - **`gemini-4-argon` GPQA Diamond (79.2% claim / 72.8% real):** DELETED. Not on Google's card or AA.
  - **`gemini-4-argon` AIME 2026 (98.4% claim / 94.6% real):** DELETED. Not on Google's card.
  - **`gemini-4-argon` Terminal-Bench 4.0 (53.8% real):** DELETED. Not published by Artificial Analysis.
  - **`grok-4-7` SWE-bench Verified (82.0% claim / 74.8% real):** DELETED. Not on xAI launch post or AA.
  - **`gpt-6-1-sol` SWE-bench Verified (83.5% claim / 77.2% real):** DELETED. Not published on OpenAI post or Scale SEAL.
  - **`claude-sonnet-5-5` SWE-bench Verified (81.0% claim / 78.6% real):** DELETED. Not on Anthropic Sonnet launch post.
  - **`claude-opus-5-5` GPQA Diamond (82.4% claim / 77.4% real):** DELETED. Not on Anthropic Opus launch table.
  - **`muse-wonder` SWE-bench Verified (74.0% claim / 66.8% real):** DELETED. Not on Meta developer table or AA article.
  - **`muse-wonder` Throughput (380 tok/s real):** DELETED. Not published in the AA article.

### Removed Schematics & Speculative Claims
- Completely removed the architectural schematics tab, SVG diagrams, and speculative execution claims. No lab published the speculative topologies depicted.
- Removed "discrete diffusion" from all Muse model descriptions. Note: Meta's October 15, 2026 `Muse Spark Open` release explicitly documents that `Muse Spark Open` is an 816B total / 42B active parameter sparse Mixture-of-Experts (MoE) model, while `Muse Wonder` and `Muse Ember` remain closed-weight API models without disclosed internal parameter counts.
- Corrected Gemini 4 Argon's context window: Google's official card states a **1M-token limit**, not 10M. Both Gemini 4 Carbon and Gemini 4 Hydrogen also carry a **1M-token context limit**.
- Removed "ChatGPT 6.1 (o4)": OpenAI shipped the 6.1 generation as **GPT-6.1 Sol** (29 Sep 2026) and **GPT-6.1 Terra** (26 Oct 2026). No "o4" variant of 6.1 was released.

Total Revision 4 observations: **132 strictly audited figures** across **23 released model slugs** (matching `data.json`).
