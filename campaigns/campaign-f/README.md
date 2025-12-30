# Campaign F: Variable Complexity + Veteran Narrative

## Overview

Campaign F is the **variable complexity test case**—a real judicial campaign whose website status is uncertain post-election. It tests graceful handling of potentially sparse or inactive content while validating veteran credential extraction.

| Field | Value |
|-------|-------|
| **Candidate** | Judge DaSean Jones |
| **Office** | Texas Supreme Court, Place 2 |
| **Party** | Democratic |
| **Type** | Real (actual 2024 statewide judicial campaign) |
| **Website** | https://www.daseanjones.com (⚠️ NEEDS VERIFICATION) |
| **Election Result** | Lost to Jimmy Blacklock (R) |

---

## Purpose

Campaign F serves as the **edge case within real campaigns**. While Campaign B provides simulated edge cases (intentional contradictions, broken links), Campaign F tests **real-world edge case behavior**: a losing campaign's post-election site that may be sparse, inactive, or taken down entirely.

### What This Tests

| Capability | Test Scenario |
|------------|---------------|
| **Variable Site Status** | May be active, sparse, or down—tests graceful degradation |
| **Veteran Narrative Extraction** | Military service as distinguishing credential (unique in suite) |
| **Post-Election Losing Campaign** | How losing candidates handle site maintenance |
| **Fallback to Third-Party Sources** | If primary site sparse, synthesize from Ballotpedia, news |
| **Judicial Campaign Consistency** | Validates Campaign D judicial handling is generalizable |

### Expected Outcomes

**If Site Active:**
- Coverage report shows judicial gaps (same as Campaign D)
- Veteran narrative successfully extracted
- Credentials and judicial experience captured

**If Site Sparse/Inactive:**
- Graceful handling of missing content
- Fallback synthesis from third-party sources
- Documents edge case behavior for sparse judicial sites

**Contradictions:** None (credentials-based content)

---

## Context: The Campaign Test Framework

| Campaign | Type | CMS | Purpose |
|----------|------|-----|---------|
| **A** | Simulated | Static HTML | Happy path—full coverage |
| **B** | Simulated | Static HTML | Edge cases—intentional gaps, contradictions |
| **C** | Real | WordPress | Real-world validation—messy HTML |
| **D** | Real | Wix | Judicial patterns + CMS diversity |
| **E** | Real | Squarespace | Progressive platform + post-victory state |
| **F (this)** | Real | **Unknown** | **Variable complexity—potentially sparse** |

Campaign F pairs with Campaign D (Weems) to **validate judicial campaign handling consistency**. If the system handles both correctly, it can generalize to any judicial campaign.

---

## Files in This Directory

| File | Description |
|------|-------------|
| `README.md` | This overview document |
| `briefing.md` | Complete candidate documentation, website assessment, content inventory, expected outcomes |

---

## Why DaSean Jones?

### Unique Test Value: Variable Complexity

**This is the "what if" campaign:**
- What if the site is down?
- What if the site is minimal?
- What if we need third-party sources?

Unlike simulated Campaign B (where we control the broken link), Campaign F is **real-world variable**. The outcome depends on actual site status at implementation time.

### Content Value: Veteran Narrative

DaSean Jones is the **only military veteran** in the test suite:
- U.S. Army combat veteran
- Military service as judicial qualification
- Different from typical legal-only judicial candidates

**Test Value:** Can the system extract and categorize military credentials alongside legal credentials?

### Comparison Value: Judicial Campaign Pair

| Dimension | Campaign D (Weems) | Campaign F (Jones) |
|-----------|-------------------|-------------------|
| Supreme Court Place | Place 4 | Place 2 |
| Background | Civil litigator | Combat veteran + sitting judge |
| Site status | Active (repurposed) | Unknown |
| CMS | Wix | Unknown |
| Post-election | Running for lower court 2026 | Unknown future |

If both campaigns are handled consistently (same gap patterns, same content classification), the system generalizes to judicial campaigns.

---

## Quick Reference

**Website:** https://www.daseanjones.com (⚠️ verify status)  
**Platform:** Unknown  
**Key Test:** Variable complexity + veteran narrative  
**Expected Gaps:** 9 (all policy—judicial campaign)  
**Expected Contradictions:** 0  
**Special Value:** Graceful degradation, fallback sources, military credentials

---

## Implementation Note

**FIRST STEP:** Verify website status before document synthesis.

| Site Status | Action |
|-------------|--------|
| Active | Scrape and document normally |
| Sparse | Document sparse state as test case; use third-party fallback |
| Down/Redirected | Document as edge case; synthesize entirely from third-party |

This variable outcome is **intentional**—it tests real-world uncertainty handling.

---

*This campaign is part of CivicAI's extended test suite (Phase 2: Post-M1).*
