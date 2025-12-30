# Campaign D: Wix CMS + Judicial Language Patterns

## Overview

Campaign D tests CivicAI's ability to handle **judicial campaign content** on a **Wix-hosted site**—a fundamentally different content pattern and CMS from Campaigns A-C.

| Field | Value |
|-------|-------|
| **Candidate** | Judge Christine Vinh Weems |
| **Office** | Texas Supreme Court, Place 4 |
| **Party** | Democratic |
| **Type** | Real (actual 2024 statewide judicial campaign) |
| **Website** | https://www.weemsforjudge.com |
| **Election Result** | Lost to John Devine (R) |

---

## Purpose

Judicial campaigns operate fundamentally differently from legislative/executive campaigns. They're credentials-focused, endorsement-heavy, and intentionally **lack policy positions** (judges shouldn't pre-commit on cases). This tests whether CivicAI correctly identifies "missing" content as appropriate rather than as a gap.

### What This Tests

| Capability | Test Scenario |
|------------|---------------|
| **Wix HTML Parsing** | Client-side rendered, CDN-hosted images, different structure from WordPress |
| **Judicial Content Patterns** | Credentials-heavy, endorsement-focused, formal tone |
| **Natural Gap Recognition** | System should recognize that "no policy positions" is correct for judicial races |
| **Site Evolution** | Campaign repurposed from Supreme Court 2024 to District Court 2026 |
| **Losing Candidate Persistence** | Tests post-election site maintenance patterns |

### Expected Outcomes

**Coverage Report (expected judicial gaps):**
- ✗ Healthcare: **GAP** (expected - judicial campaigns don't have policy)
- ✗ Education: **GAP** (expected)
- ✗ Housing: **GAP** (expected)
- ✗ Economy: **GAP** (expected)
- ✗ Environment: **GAP** (expected)
- ✗ Public Safety: **GAP** (expected)
- ✗ Infrastructure: **GAP** (expected)
- ✗ Seniors: **GAP** (expected)
- ✗ Immigration: **GAP** (expected)

**Key Insight:** The coverage report showing 9 gaps is **correct behavior** for a judicial campaign. The system should potentially flag the race type to contextualize these gaps.

**Contradictions:** None (credentials-based content is factual, not positional)

---

## Context: The Campaign Test Framework

| Campaign | Type | CMS | Purpose |
|----------|------|-----|---------|
| **A** | Simulated | Static HTML | Happy path—full coverage |
| **B** | Simulated | Static HTML | Edge cases—intentional gaps, contradictions |
| **C** | Real | WordPress | Real-world validation—messy HTML |
| **D (this)** | Real | **Wix** | **Judicial patterns + CMS diversity** |
| **E** | Real | Squarespace | Progressive platform + post-victory state |
| **F** | Real | Unknown | Variable complexity—potentially sparse |

Campaign D establishes the **judicial campaign baseline** for comparison with Campaign F (also judicial).

---

## Files in This Directory

| File | Description |
|------|-------------|
| `README.md` | This overview document |
| `briefing.md` | Complete candidate documentation, website assessment, content inventory, expected outcomes |

---

## Why Christine Weems?

### Technical Test Value
- **First Wix site** in the test suite (different scraping patterns than WordPress)
- **Client-side rendering** may require JavaScript execution
- **Wix CDN** for images (static.wixstatic.com)

### Content Pattern Value
- **Credentials-heavy** (board certifications, bar admissions, awards)
- **Third-party validation** (endorsements from Houston Chronicle, Dallas Morning News)
- **Formal tone** contrasts with populist campaign language in A/C/E

### Site Evolution Value
- Originally built for statewide Supreme Court race (2024)
- Now repurposed for local 281st District Court re-election (2026)
- Tests how campaigns repurpose infrastructure post-election

---

## Quick Reference

**Website:** https://www.weemsforjudge.com  
**Platform:** Wix  
**Key Test:** Judicial content + Wix CMS  
**Expected Gaps:** 9 (all policy areas—correct for judicial)  
**Expected Contradictions:** 0  
**Special Value:** Credentials extraction, endorsement parsing, non-WordPress CMS

---

*This campaign is part of CivicAI's extended test suite (Phase 2: Post-M1).*
