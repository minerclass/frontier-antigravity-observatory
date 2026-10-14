Written on: surface-arm · antigravity · 2026-10-14

# Frontier Benchmark Atlas: Antigravity Compilation Notes (Revision 3)

## 1. Compiler Identity & Context
- **Harness:** Antigravity (Google Advanced Agentic Coding environment)
- **Host Machine:** `surface-arm` (`MSURFACE32ARM64`, verified via `hostname`)
- **Compilation Date:** 2026-10-14
- **Revision:** 3 (Citation Location & Source Integrity Audit)
- **Brief Followed:** `HARNESS.md` in `minerclass/frontier-benchmark-atlas`

## 2. Revision 2 & 3 Audits: Removals, Surviving Figures, and Cross-Check Disclosures

Revision 2 was initiated following the audit report provided by the Atlas hub owner (`surface-arm/claude-code`). Revision 3 refines all citation locations to eliminate inaccurate pseudo-quotations and misattributed tables, points Sonnet 5.5 to its authentic launch page, removes speculative architecture claims, and synchronizes all dataset counts.

### Figures Adopted from the Hub Owner Cross-Check and Compilations
In Revision 2, several figures were adopted from the hub owner's source cross-check or secondary compilations rather than found independently in the initial pass:
- **Grok 4.7 CursorBench 4.0 effort tiers (46.3% Extra High, 43.9% High, 41.6% Medium, 33.1% Low):** Adopted directly from the hub owner's check of the Cursor public leaderboard, replacing an unsourced first-pass figure of 41.2%.
- **OpenAI Secondary Compilations (GPT-6 Astra OSWorld 72.6%, GPT-6 Sol DeepSWE 68.8%, GPT-6 Luna DeepSWE 66.6%):** Adopted from analyst compilations and launch reproductions because OpenAI launch endpoints returned HTTP 403 on automated fetch.
- **Anthropic Sonnet 5.5 Launch Page Re-pointing:** In Revision 2, Sonnet 5.5's Terminal-Bench 4.0 (70.6%) and FrontierCode (52.1%) were cited to a non-existent Sonnet column on the Opus 5.5 page. Following the hub owner's source check, both figures were verified on and pointed to `https://www.anthropic.com/claude-sonnet-5-5`.
- **Meta Developer Figures (Muse Wonder DeepSWE 78.8%, SWE-Marathon 53.1%; Wonder Full DeepSWE 79.0%, SWE-Marathon 57.5%):** Originally incorporated in Revision 2 from developer compilations; directly fetched and verified in Revision 3 from Meta's blog.

### First-Pass Survival Summary
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
- Removed "discrete diffusion" from all Muse model descriptions. No source documents Muse's underlying model architecture.
- Corrected Gemini 4 Argon's context window: Google's official card states a **1M-token limit**, not 10M.
- Removed "ChatGPT 6.1 (o4)": OpenAI shipped the 6.1 generation strictly as **GPT-6.1 Sol** (29 Sep 2026) in Work, Codex, and API. No "o4" variant of 6.1 was released.

## 3. Model Names Requested vs. What Labs Released
- **"ChatGPT 6.1 various relevant models as well as Astra":** Shipped only as **GPT-6.1 Sol** (29 Sep 2026). "ChatGPT 6.1 (o4)" does not exist. Astra is **GPT-6 Astra** (3 Sep 2026); "GPT-6.1 Astra" was not released.
- **"the new Muse models":** Meta released **Muse Wonder** and **Muse Wonder Full** (12 Oct 2026, codename Watermelon). Wonder Full is restricted to the Muse Code subscription.
- **"Claude 5.5 set of models and 5.1 Fable":** **Claude Opus 5.5** (22 Sep), **Claude Sonnet 5.5** (28 Sep), **Claude Haiku 5.5** (7 Oct), and **Claude Fable 5.1** (1 Sep; URL is `/claude-fable-and-mythos-5-1`).
- **"Cursor with Grok 4.7 various models":** **Grok 4.7** (SpaceXAI / xAI), **Grok 4.6**, and Cursor's native **Composer 2.5**.
- **"Gemini 4 Argon":** Google released **Gemini 4 Argon** (13 Oct GA, 1M context limit).

## 4. Primary Sources & Exact Locations (Revision 3)
Every observation carries its exact wording, table row/column, or plain description:
- **Google DeepMind Argon Card:** `https://deepmind.google/models/model-cards/gemini-4-argon/` (`sourceRead: true`). 8 figures cited to the single Results table grouped by category (Knowledge work, Agentic coding, Science and math, Cybersecurity).
- **Cursor CursorBench 4.0 Board:** `https://cursor.com/cursorbench` (`sourceRead: true`). 8 figures cited to the public leaderboard table rows.
- **Anthropic Opus 5.5 Launch Table:** `https://www.anthropic.com/claude-opus-5-5` (`sourceRead: true`). 11 figures cited to the launch benchmark comparison table across Opus 5.5, Fable 5.1, Opus 5, GPT-6 Astra, and GPT-5.6 Sol.
- **Anthropic Sonnet 5.5 Launch Table:** `https://www.anthropic.com/claude-sonnet-5-5` (`sourceRead: true`). 2 figures cited directly to the Sonnet 5.5 launch page benchmark table.
- **OpenAI Launch Posts:** `https://openai.com/index/introducing-gpt-6-1-sol/`, `introducing-gpt-6-sol-and-luna`, `gpt-6-astra-system-card` (`sourceRead: false` due to HTTP 403 on automated fetch). 4 figures described plainly without pseudo-quotes.
- **Meta Muse Wonder Developer Blog:** `https://dev.meta.ai/resources/blog/build-with-muse-wonder` (`sourceRead: true`). 4 figures cited to the blog evaluation table.
- **Artificial Analysis Muse Wonder Article:** `https://artificialanalysis.ai/articles/muse-wonder` (`sourceRead: true`). 11 figures cited to exact article prose (Intelligence Index, Coding Agents Index, Terminal-Bench 4.0, and cost per task).

Total Revision 3 observations: **48 strictly audited figures** across **17 released model slugs** (matching `data.json`).
