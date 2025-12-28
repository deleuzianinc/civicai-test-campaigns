# Campaign C: Real-World Validation

## Overview

Campaign C uses a **real campaign website** to validate that CivicAI works outside "clean room" conditions with authentic, messy web content.

| Field | Value |
|-------|-------|
| **Candidate** | Marc Duchen |
| **Office** | Austin City Council, District 10 (Texas) |
| **Party** | Democratic |
| **Type** | Real (actual 2024 campaign) |
| **Website** | https://marcforaustin.com |
| **Election Result** | **Won** (November 2024) |

---

## Purpose

Campaigns A and B are simulated—their content is controlled and predictable. Campaign C proves the system works with real-world content: WordPress-generated HTML, authentic political language, natural gaps in coverage, and the general messiness of actual campaign websites.

### What This Tests

| Capability | Test Scenario |
|------------|---------------|
| **Real HTML Parsing** | WordPress + Elementor nested structure |
| **Authentic Language** | Real political phrasing, not simulated |
| **Natural Gaps** | 4-5 policy areas not addressed (vs. intentional gaps in B) |
| **Garbage Detection** | Lorem ipsum placeholder text in accordion tabs |
| **Sparse Content Handling** | Empty events calendar (post-election) |
| **Synthesized Documents** | Documents created from web content |

### Expected Outcomes

**Coverage Report (natural gaps):**
- ✓ Environment: covered
- ✓ Public Safety: covered
- ✓ Mobility/Transit: covered
- ✓ Homelessness: covered
- ✓ Spending/Fiscal: covered
- ✓ Land Use/Housing: covered
- ✓ Wildfire Prevention: covered
- ✓ Road Safety: covered
- ✗ Healthcare: **GAP** (natural)
- ✗ Education: **GAP** (natural)
- ✗ Seniors: **GAP** (natural)
- ✗ Immigration: **GAP** (natural)

**Contradictions:** None expected (or minor)

**Special Tests:**
- Lorem ipsum detected/filtered from accordion placeholders
- Empty calendar handled gracefully

---

## Context: The Three-Campaign Framework

CivicAI's M1 milestone uses three campaigns to validate the content pipeline:

| Campaign | Type | Purpose |
|----------|------|---------|
| **A** | Simulated | Happy path—verify everything works with clean input |
| **B** | Simulated | Edge cases—verify gap detection, contradiction flagging, error handling |
| **C (this)** | Real | Real-world validation—verify system handles authentic messy content |

Campaign C is the final validation. If the system handles Marc Duchen's real website correctly, it's ready for production use with actual customer campaigns.

---

## Files in This Directory

| File | Description |
|------|-------------|
| `briefing.md` | Complete candidate documentation, website assessment, content inventory, expected test outcomes |
| `framework.md` | Selection methodology used to identify this candidate (reference for future selections) |

---

## Why Marc Duchen?

### Content Quality
- **8 detailed policy areas** with 4+ bullet points each
- **Rich biography** (immigrant story, cancer survivor, Democratic political career)
- **100+ endorsements** from elected officials and organizations
- **Multiple page types** for classification testing

### Real-World Testing Value
| Challenge | Where Found | Test Value |
|-----------|-------------|------------|
| Lorem ipsum placeholder | /issues accordion tabs | Garbage detection |
| Empty calendar | /events-calendar | Sparse content handling |
| Nested Elementor HTML | All pages | Parser robustness |
| Complex endorsement lists | Homepage | Entity extraction |

### Risk Profile: Minimal
- Race completed (November 2024)
- Candidate won (now serving as Council Member)
- No controversies or scandals
- Standard local municipal governance

---

## Synthesized Documents

Marc Duchen's campaign has no downloadable documents, so we synthesize test documents from web content:

| Document | Source | Filename |
|----------|--------|----------|
| Policy Platform (PDF) | /issues page | `duchen-policy-platform.pdf` |
| Biography (DOCX) | /my-story page | `duchen-biography.docx` |
| Endorsements (TXT) | Homepage | `duchen-endorsements.txt` |

**Note:** Include the lorem ipsum placeholder text in the PDF to test garbage detection.

---

## Website Pages to Scrape

| Page | URL | Content |
|------|-----|---------|
| Home | https://marcforaustin.com | Endorsements, overview, news |
| Bio | https://marcforaustin.com/my-story | Detailed narrative |
| Issues | https://marcforaustin.com/issues | 8 policy areas |
| Events | https://marcforaustin.com/events-calendar | Empty (post-election) |
| Blog | https://marcforaustin.com/blog | 3 campaign posts |

---

## Comparison: A vs B vs C

| Dimension | Campaign A | Campaign B | Campaign C |
|-----------|:----------:|:----------:|:----------:|
| Type | Simulated | Simulated | **Real** |
| Policy areas | 9 (full) | 3 (sparse) | 8 (natural) |
| Gaps | 0 | 7+ | 4-5 |
| Contradictions | 0 | 1 (intentional) | 0 (expected) |
| HTML quality | Clean | Clean | Messy (WordPress) |
| Documents | 4 types | 1 PDF | 0 (synthesize 3) |
| Broken links | 0 | 1 (Events 404) | 0 |

---

## Quick Reference

**Website:** https://marcforaustin.com  
**Key Pages:** /issues, /my-story, /events-calendar  
**Key Test:** Real-world content parsing  
**Expected Gaps:** 4-5 (natural)  
**Expected Contradictions:** 0  
**Special Test:** Lorem ipsum garbage detection

---

*This campaign is part of CivicAI's M1 test suite.*
