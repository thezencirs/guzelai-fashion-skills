---
name: guzelai-human-algorithm-warmup
description: Pre-Publish Human Browsing, GhostCursor Cubic Bézier Biometrics & Niche Algorithm Warm-Up Engine for GüzelAI Holding (@guzelaicom). Ported from Xetera/ghost-cursor and riflosnake/HumanCursor for single-trusted Chrome CDP (port 9230). Browses organically before publishing, selectively watches fashion/Old Money Reels (9-21s), skips off-niche content (2-4s), performs micro-dose engagement (max 1-2 likes, max 1 save, zero comments/follows), and trains Instagram's interest graph with 0% bot violation risk.
---

# GüzelAI Pre-Publish Human Browsing & Algorithm Warm-Up Skill (`guzelai-human-algorithm-warmup`)

## 1. Purpose & Core Philosophy
Instagram's behavioral telemetry (`Falco` / biometric event streams) evaluates whether an account behaves like a **real human creator in its niche** or an **isolated upload-only bot**.
At the same time, aggressive engagement bots get banned because they perform puluhan/hundreds of likes, comments, or rapid URL jumps.

This skill implements the **Golden Middle — Ultra-Safe Human Creator Warm-Up**:
- **Single Trusted Browser Only:** Runs exclusively inside `C:\Users\zenci\.gemini\antigravity\scratch\ig_chrome_trusted` (Port `9230`) on the user's residential IP.
- **Open-Source Biometric Physics (GitHub R&D):**
  - `Xetera/ghost-cursor` (1.6k+ ⭐) & `reaz1995/ghost-cursor-playwright`: Cubic Bézier mouse trajectories with Fitts's Law velocity profiling, slight human overshoot, and micro-tremor noise.
  - `riflosnake/HumanCursor` (540+ ⭐): Gaussian-randomized target points inside the inner 60% of DOM bounding boxes (never clicking exact mathematical center `(w/2, h/2)`) and multi-step inertia mouse-wheel scrolling.

---

## 2. The 7 Zero-Violation Guardrails ("İhlal Olmasın" Standard)

1. **24-Hour Post-Login Curing Lock (`session_warmup_until_iso`):**
   - Never performs any automated browsing, liking, saving, or posting during the first 24 hours after a manual password login.
2. **Micro-Dose Engagement Caps (Hard-Coded Maximums per Warm-Up Session):**
   - **Watched Reels:** `4 to 6` Reels per pre-publish session.
   - **Likes (`❤️`):** Maximum `1 to 2` likes per session (only on verified fashion/style/kombin content).
   - **Saves (`🔖`):** Maximum `1` save per session (highest-signal algorithm training action).
   - **Comments / Follows / Unfollows / DMs:** **STRICTLY `0` (Permanently Prohibited).**
3. **Selective Niche Discrimination (Algorithmic Interest Graph Training):**
   - Inspects visible caption/hashtags in read-only mode against `FASHION_NICHE_KEYWORDS` (`kombin`, `old money`, `quiet luxury`, `stil`, `moda`, `outfit`, `kaban`, `triko`, `palazzo`, `ootd`, `menswear`, `womenswear`).
   - **On-Niche High-Quality Reel:** Watches for `9.5s – 21.0s` (often letting the Reel loop once), moves cursor organically, and probabilistically likes (`~35%`) or saves (`~25%`, capped at 1).
   - **Off-Niche Reel:** Scrolls past within `2.2s – 4.1s` with zero interaction, training Instagram's algorithm that `@guzelaicom` is 100% dedicated to fashion/styling.
4. **Zero Direct Hashtag URL Loops:**
   - Never rapid-loads `/explore/tags/...` URLs. Uses the native Reels tab (`/reels/`) or home feed (`/`) with natural wheel scroll inertia.
5. **Creator Transition Pause:**
   - Waits `12s – 22s` after finishing the warm-up walk before clicking the `+` (Oluştur) button to upload the new Reel.
6. **6-Hour Minimum Cooldown Between Sessions:**
   - Warm-up + publish runs at most once every 6 hours (`IG_MIN_INTERVAL_SEC = 21600`).
7. **Trend Inspiration Ledger (`output/instagram_algorithm_warmup_ledger.json`):**
   - Logs captions and metrics of saved/liked niche Reels so the **Style Curation Council (`STYLE_CURATION_COUNCIL_AGENCY`)** can incorporate viral hook patterns.

---

## 3. Reference Implementation
- Engine: `C:\Users\zenci\.gemini\antigravity\scratch\instagram-kombin-bot\src\instagram_human_warmup.py`
- Integrated Publisher: `C:\Users\zenci\.gemini\antigravity\scratch\instagram-kombin-bot\src\instagram_safe_publisher.py`
