---
name: guzelai-oldmoney-gender-guardrail
description: Zero-Tolerance Gender Compliance Firewall (strictly blocks women's bags/items in men's outfits; enforces masculine chronograph watches/accessories in men's slot 5), Named Iconic Style Movements Engine (Old Money Heritage, Quiet Luxury, Italian Sprezzatura, Dark Academia, Alpine Après-Ski), and Multi-Agent Fashion Design Council Communication Protocol for GüzelAI Holding. Trigger whenever generating, auditing, or publishing outfits across kadin, erkek, kiz_cocuk, or erkek_cocuk.
---

# GüzelAI Zero-Tolerance Gender Guardrail, Old Money Style Curation & Multi-Agent Design Council Skill

## 1. Zero-Tolerance Gender & Accessory Compliance Rule (`KADİR` & `HALUK` Firewall)
1. **NO Women's Bags or Feminine Items in Men's (`erkek` / `erkek_cocuk`) Outfits — Ever:**
   - A men's (`erkek`) or boys' (`erkek_cocuk`) outfit MUST NEVER include a women's handbag, purse, tote, clutch, woven top-handle portföy (`el çantası`, `portföy`, `omuz çantası`, `mini çanta`), or any women-only store/brand (`Bagmori`, `İpekyol`, `Twist`, `Quzu`, `Machka`).
   - **Men's (`erkek`) 5th Slot Standard (`05_bag` slot key):** Instead of ambiguous handbags, Men's Old Money / Sartorial / Quiet Luxury creations use a **100% Masculine Luxury Mechanical/Chronograph Wristwatch (`Erkek Lüks Kronograf / Otomatik Deri veya Çelik Kol Saati`)**, **Masculine Leather Belt & Cashmere Scarf Set (`Erkek Hakiki Deri Kemer & Kaşmir Atkı`)**, or an unmistakably masculine laptop/backpack.
   - **Strict Cross-Gender Asset Isolation:** When resolving `cutout_assets` or `model_frames` (including cloud fallbacks in `autonomous_creation_factory.py`), an `erkek` outfit may ONLY match files explicitly prefixed with `erkek_` (and `erkek_cocuk` only `kid_boy_` / `erkek_cocuk_`). Cross-gender fallback is a hard runtime error (`GenderComplianceViolationError`).

## 2. Named Iconic Style Movements Only (Zero Random Seasonal Combinations)
Seasonal appropriateness (winter coats, cashmere, wool flannel, shearling) is mandatory, **but outfits must NEVER be random assortments of clothes**. Every creation must explicitly embody one of the **6 Iconic Named Style Movements**:
1. **Old Money Heritage (`OLD MONEY MİRAS STİLİ` — Loro Piana / Ralph Lauren Aesthetic):**
   - *Palette:* Warm Camel, Ivory/Ecru, Espresso Brown, Charcoal Flannel, Deep Navy, Forest Green (`60-30-10` ratio).
   - *Key Pieces:* Double-breasted camel wool/cashmere coat, cable-knit (`saç örgü`) cashmere/merino turtleneck, pleated wool flannel trousers, brown leather chronograph watch (men) or equestrian gold-buckle saddle bag (women), suede Chelsea boots or equestrian leather boots.
2. **Quiet Luxury / Stealth Wealth (`SESSİZ LÜKS` — The Row / Brunello Cucinelli Aesthetic):**
   - Zero visible logos, tonal cashmere-on-wool layering, matte suede and brushed merino textures.
3. **Italian Sprezzatura Sartorial (`İTALYAN SPREZZATURA & MILANO SARTORIAL`):**
   - Sharp peak-lapel overcoats, fine gauge merino rollnecks, double-pleated flannel trousers, Italian suede boots, mechanical dress watch.
4. **Dark Academia & Ivy League (`DARK ACADEMIA & OXFORD PREPPY`):**
   - Herringbone tweed overcoat, oxblood/emerald/ecru cable-knit sweater, tailored wool/corduroy trousers, leather brogues/boots.
5. **Alpine Après-Ski Luxury (`ST. MORITZ & COURCHEVEL ALPINE LUXURY`):**
   - Shearling-collar suede jacket or quilted down jacket, heavy ribbed merino turtleneck, winter wool trousers, winter boots.
6. **Parisian Left-Bank Editorial (`PARİZYEN RIVE GAUCHE ŞIKLIĞI`):**
   - Deep oxblood or jet-black maxi wool/leather coat, silk-cashmere mock-neck, wide-leg wool trousers, pointed ankle boots.

## 3. Multi-Agent Fashion Design Council Communication Protocol (`MODA TASARIM KONSEYİ`)
Before any outfit is rendered into a 2K Reel or dispatched to Telegram (`@guzelaibot`), 6 specialized agents execute a synchronous council review (`run_fashion_design_council_session()`):
1. **Style Curator (`FERİDE` / `TARIK`):** Selects the named style movement (*Old Money Heritage*, *Italian Sprezzatura*, etc.) and defines the `60-30-10` color palette.
2. **Lead Atelier Designer (`DEFNE` for Women, `KEREM` + `HALUK` for Men, `LEYLA` / `MERT` for Kids):** Crafts the 6 pieces with 1:1 visual and textural harmony.
3. **Gender & Compliance Inspector (`KADİR`):** Verifies 100% gender-locked items, URLs, brands, and PNG cutouts (zero women's bags in men's outfits).
4. **Texture & Color Harmonist (`ZEYNEP`):** Validates fabric weight contrast (cashmere vs. wool flannel vs. suede/leather).
5. **AI Supermodel Casting & Pose Director (`DERİN` & `KUZEY`):** Enforces 100% photorealistic human AI supermodels (`is_3d_avatar = False`) and natural masculine/feminine posture (no handbag in male model's hands).
6. **Remotion 2K Cinema Director (`KORAY` & `ATLAS`):** Locks spring physics, lighting, and camera parallax to match the style movement's mood.
