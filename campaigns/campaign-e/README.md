# Campaign E: Squarespace CMS + Progressive Municipal Platform

## Overview

Campaign E tests CivicAI's handling of **Squarespace-hosted sites** and **progressive municipal campaign content**, including post-election victory messaging transitions.

| Field | Value |
|-------|-------|
| **Candidate** | Mike Siegel |
| **Office** | Austin City Council, District 7 |
| **Party** | Non-Partisan (Progressive) |
| **Type** | Real (actual 2024 municipal campaign) |
| **Website** | https://www.siegelforaustin.org |
| **Election Result** | Won (December 2024 Runoff) |

---

## Purpose

This campaign tests three distinct capabilities: Squarespace CMS scraping (third platform in suite), progressive policy language patterns, and handling of post-election site evolution where victory messaging replaces active campaign content.

### What This Tests

| Capability | Test Scenario |
|------------|---------------|
| **Squarespace HTML Parsing** | Third CMS platform (after WordPress, Wix) |
| **Progressive Policy Language** | Distinct terminology from moderate/conservative campaigns |
| **Post-Victory Content** | Site transitioned from active campaign to "thank you" state |
| **Urban Policy Coverage** | Strong positions on housing, climate, labor, transit |
| **Runoff Election Context** | Two-phase election narrative |

### Expected Outcomes

**Coverage Report (strong urban policy coverage):**
- ✓ Housing/Affordability: **COVERED** (primary focus)
- ✓ Climate/Environment: **COVERED** (dedicated page)
- ✓ Public Safety: **COVERED** (reform-oriented)
- ✓ Transportation: **COVERED** (urban mobility)
- ✗ Healthcare: **PARTIAL** (peripheral references only)
- ✗ Education: **GAP** (outside city council scope)
- ✗ Seniors: **GAP** (limited coverage)
- ✗ Immigration: **GAP** (limited coverage)

**Natural Gaps:** 3-4 (education, seniors, immigration—limited city council jurisdiction)

**Contradictions:** None expected (progressive positions are internally consistent)

---

## Context: The Campaign Test Framework

| Campaign | Type | CMS | Purpose |
|----------|------|-----|---------|
| **A** | Simulated | Static HTML | Happy path—full coverage |
| **B** | Simulated | Static HTML | Edge cases—intentional gaps, contradictions |
| **C** | Real | WordPress | Real-world validation—messy HTML |
| **D** | Real | Wix | Judicial patterns + CMS diversity |
| **E (this)** | Real | **Squarespace** | **Progressive platform + post-victory state** |
| **F** | Real | Unknown | Variable complexity—potentially sparse |

Campaign E pairs with Campaign C (Duchen) as the **second Austin City Council race**, enabling direct comparison of moderate vs progressive municipal campaigns.

---

## Files in This Directory

| File | Description |
|------|-------------|
| `README.md` | This overview document |
| `briefing.md` | Complete candidate documentation, website assessment, content inventory, expected outcomes |

---

## Why Mike Siegel?

### Technical Test Value
- **First Squarespace site** in the test suite
- **Modern responsive design** with clean DOM structure
- **ActBlue integration** for donations (external link handling)
- **Form elements** (signup) that should be identified but not extracted as content

### Content Pattern Value
- **Progressive policy language** ("pro-housing", "pro-labor", "pro-justice")
- **Opposition context** (references right-wing PAC attacks)
- **Victory messaging** mixed with platform content

### Site Evolution Value
- Site updated post-runoff victory (December 2024)
- Tests handling of campaign-to-serving transition
- "Thank you" messaging distinct from active campaign content

### Comparison Value
- **Same city, different district** as Campaign C (Duchen)
- **Different ideology** (progressive vs moderate)
- **Different CMS** (Squarespace vs WordPress)
- **Different site state** (victory vs active campaign)

---

## Quick Reference

**Website:** https://www.siegelforaustin.org  
**Platform:** Squarespace  
**Key Test:** Squarespace CMS + progressive language  
**Expected Gaps:** 3-4 (city council scope limitations)  
**Expected Contradictions:** 0  
**Special Value:** Post-victory content, progressive terminology, ActBlue integration

---

*This campaign is part of CivicAI's extended test suite (Phase 2: Post-M1).*
