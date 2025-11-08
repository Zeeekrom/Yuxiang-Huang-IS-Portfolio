# 💼 Internships — From Creative Work to Information Systems

This section documents real workflow experiences from three internships:  
**Tencent IEG (Honor of Kings)**, **Lilith Games (AIGC Pipeline)**, and **Perfect World (AI Environment Art)**.  
All information is depersonalized; only the **systems**, **documentation structure**, and **information-management practices** are retained.

---

## 🧩 Tencent IEG (Honor of Kings) — Complex Information Flow

### 🔹 Systems and Documents Accessed Daily

**1️⃣ Data & Telemetry (supporting win/pick/telemetry analysis)**  
- **Internal BI Dashboards:** segmented win rates, pick-ban data, match duration, KDA, damage share, usage heat (P0/P1…King tier; 7/14/30-day windows).  
- **Data Warehouse / SQL:** key tables such as `hero_metrics_daily`, `match_skill_events`, `economy_timeline`, and `ab_result_summary`.  
  These cover skill-event frames, economy curves, and A/B experiment aggregates.  
- **Logs & Replays:** combat logs (`killfeed`, `damage_tick`, `ability_cast`) and replay tools for verifying mechanic triggers.

**2️⃣ Experiment & Parameter Configuration (for balance iteration)**  
- **Experiment / Gray-release platform:** create and monitor skill parameter tests (damage, cooldown, mana cost, hitbox size, thresholds) while tracking sample size, significance, and stop rules.  
- **Configuration Center:** manage hero growth curves, frame data, equipment/rune/buff coefficients, hotfix switches, and rollback conditions.

**3️⃣ Design & Version Management**  
- **Design Doc Library:** hero design intent, frame/collision data, and meeting notes.  
- **Iteration Boards (TAPD / Jira):** numerical-change tasks, validation lists, defect reports, milestones, and changelogs.

**4️⃣ QA & Quality Monitoring**  
- **Test-case Library:** edge-case combos, frame validation, abnormal state overlaps (silence, knock-up, vulnerability).  
- **Performance Dashboards:** crash rate, frame drop, latency alerts, and regression results.

**5️⃣ Operations & External Feedback**  
- **Tournament / High-rank Reports:** comparing pro vs ladder samples.  
- **Community Reports:** tagging frequent complaints to distinguish “experience” vs “numerical” issues.

**6️⃣ Daily Stakeholders to Sync With**  
Numerical & gameplay designers, client/server engineers, analysts, QA testers, operations and esports teams.

---

### 🔹 Typical Multi-System Scenarios

#### (1) Gray-Release for Hero Parameter Tuning
- **Data viewed:** segmented win/pick rates, match duration, economy curves, A/B significance.  
- **Tools:** BI dashboards, SQL, experiment platform, configuration center.  
- **Alignment:** design, engineering, analytics, QA, operations.  
- **Outputs:** modification notes, gray-release plan (scope, thresholds, stop rules), rollback config, changelog.

#### (2) Skill-Mechanic Anomaly Investigation
- **Data viewed:** event timestamps, abnormal logs, outlier KDA/damage peaks.  
- **Tools:** combat logs, replay tools, TAPD/Jira tickets, frame tables, collision docs.  
- **Outputs:** reproduction videos, frame-table fixes, prioritized defect lists, regression checklists.

#### (3) Community or Esports “Overpowered” Review
- **Data viewed:** pro vs public win-rate gaps, lane-time and economy curves, counter matrix.  
- **Tools:** sentiment reports, BI comparison boards, layered SQL queries, A/B platform.  
- **Outputs:** categorized conclusions (experience / perception / numeric), communication briefs, micro-adjustment plans.

#### (4) Pre-Release “Regression + Rollback” Audit
- **Data viewed:** gray-release curves, crash/freeze rate, KPI thresholds.  
- **Tools:** monitoring dashboards, rollback scripts, coverage reports.  
- **Outputs:** rollout plan, alert thresholds, rollback ownership, release checklist.

---

## 🧩 Lilith Games — AIGC Content-Pipeline Optimization

### 🔹 Common Pain Points and Solutions

| **Problem**                                    | **Manifestation**                                            | **My Handling**                                              | **Further Optimization**                     |
| :--------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- | :------------------------------------------- |
| Too many asset/model versions; unclear lineage | Multiple LoRA / Prompt / ControlNet versions per style; final package untraceable. | Created “Model/Prompt Cards” recording base model, weight, sampler, CFG, ControlNet type, and metadata (who/when/model/prompt). | Add model registry & hash validation.        |
| Style inconsistency; heavy manual curation     | Lighting & angle drift; different prompt habits.             | Built “Golden Reference Board” (10–20 key images) + preset templates (ComfyUI/SD params + negative list); dual-channel review. | Add style classifier / embedding alignment.  |
| Incomplete requests; repeated clarification    | Missing usage/resolution/license info.                       | Enforced request template (use case, refs, must/optional elements, license window); “no ticket → no schedule.” | Integrate mandatory form into system.        |
| Format mismatch before Unity/UE import         | Different export size/color space/bit depth.                 | Co-wrote batch preprocessing script (rename, unify size/color space/LOD) with TA. | CI hook for auto-validation.                 |
| Unclear license boundaries                     | Ambiguous rights & expiry.                                   | Added license tags & expiry fields; built registry (source, agreement, limitations). | Connect to legal contract database.          |
| Invisible efficiency                           | Team tracked quantity but not conversion.                    | Built dashboard showing generation → usable → packaged; annotated rejection causes. | Auto-link dashboard to asset DB.             |
| GPU contention                                 | LoRA training and batch inference overlapped.                | Created resource booking & priority pools; added low-VRAM presets for previews. | Implement job-queue manager & budget alerts. |

---

## 🧩 Perfect World — Discoverability & Collaboration Systems

### 🔹 Naming & Tagging Convention

[Project_AssetType_Style_Res_Version_Date_Author]

Example tags:  
`style:filmic | lora:v3.2 | cn:openpose | res:2048x1024 | color:sRGB | lic:comm-ok`  
→ Immediate clarity on usage, style, version, license; supports fuzzy search and batch operations.

### 🔹 Asset Metadata Cards
Fields: `base_model, lora_id, alpha, ckpt_hash, sampler, steps, cfg, controlnet(type,strength), seed_range, author, date`.  
→ One card per model/prompt version; stored with asset for rollback and traceability.

### 🔹 Request Templates
Mandatory fields: purpose, resolution/ratio, style reference, mutable/fixed elements, release window, license limits.  
→ No template, no scheduling; missing fields resolved in weekly sync.

### 🔹 Directory & Index Convention

/Project/AssetType(Character/Env/FX)/StylePack/Version/BatchID/

`asset_index.csv` → (asset_id, path, tags, lic, version, source, status).  
→ Enables quick cross-user search and clear in-package status tracking.

### 🔹 Pre-Import Batch Scripts
Auto-unify naming, size, color space, bit depth; generate thumbnails & LOD presets.  
→ Must pass local self-check before commit; CI verifies again before merge.

### 🔹 Version & Lineage Table

final_asset_id ← batch_id ← model_version ← prompt_version ← controlnet_cfg

→ One-page lineage map enabling rollback and reproduction.

### 🔹 “Golden Style” Baseline Boards
10–20 benchmark images per character/theme with evaluation criteria (composition, lighting ratio, material, tone).  
→ Used for both training reference and review scoring.

### 🔹 Reusable Preset Library
Common ComfyUI/SD setups for resolution, lighting, material, camera, and negative prompts.  
→ Ensures immediate productivity and visual consistency.

### 🔹 Lightweight Efficiency Dashboard
Metrics: generation → usable → packaged; rejection reasons (style, res, license, import fail); average processing time.  
→ Weekly reports visualize bottlenecks and guide improvement.

### 🔹 Mini Glossary of Terms
Examples:  
`style:filmic` = “realistic-film look”  
`lic:comm-ok` = “commercial use allowed”  
`lock:hair_color` = “non-modifiable element”  
→ Ensures shared vocabulary across art, TA, design, and legal teams.

### 🔹 Document Templates & Definition of Done (DoD)
Standard bundle: style guide, parameter log, import checklist, review notes, rollback plan.  
→ Must pass all checks before asset submission.

### 🔹 Permission Zones
Asset library divided into **production / review / release** zones; release zone set to **read-only** to prevent overwrites.

---

## 🌐 Takeaway

Across all internships, I learned that **content creation is a form of information management**.  
Large studios rely on structured data governance — from BI dashboards and telemetry pipelines to LoRA registries and metadata cards — to maintain clarity and traceability.

Each workflow answered a common question:

> **How can information stay clear, trustworthy, and reusable?**

“What began as gameplay or art production became a study of data governance —  
every table, tag, and template is a small act of keeping chaos in check.”