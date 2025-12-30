# Campaign B: Edge Cases (Gaps & Contradictions)

## Overview

Campaign B is a **simulated campaign** designed to stress-test CivicAI's ability to detect problems: missing policy positions, contradictory statements, broken links, and sparse content.

| Field | Value |
|-------|-------|
| **Candidate** | John R. Miller |
| **Office** | City Council, Ward 3 (Riverside Heights, Ohio) |
| **Party** | Republican |
| **Type** | Simulated (fictional candidate in fictional city) |

---

## Purpose

This campaign validates that the system correctly identifies issues that a campaign manager or comms director would need to address. If Campaign A tests "does it work?", Campaign B tests "does it catch problems?"

### What This Tests

| Capability | Test Scenario |
|------------|---------------|
| **Gap Detection** | Only 3 of 10 standard policy areas addressed |
| **Contradiction Detection** | "Oppose all taxes" vs. "Support property tax increase for police levy" |
| **Broken Link Handling** | Events page returns 404 error |
| **Sparse Content** | Minimal bio, no detailed position papers |
| **Single Document Format** | Only PDF (poorly formatted) |

### Expected Outcomes

**Coverage Report:**
- ✓ Fiscal/Taxes: covered
- ✓ Public Safety: covered
- ✓ Economic Development: covered
- ✗ Housing: **GAP**
- ✗ Education: **GAP**
- ✗ Healthcare: **GAP**
- ✗ Environment: **GAP**
- ✗ Infrastructure: **GAP**
- ✗ Seniors: **GAP**
- ✗ Immigration: **GAP**

**Contradictions:** 1 detected (tax policy)
> "I will oppose any new taxes or fee increases. Period."  
> vs.  
> "I support... the new public safety levy that will ask voters to approve a modest property tax increase."

**Errors:** 1 (Events page 404)

---

## Context: The Three-Campaign Framework

CivicAI's M1 milestone uses three campaigns to validate the content pipeline:

| Campaign | Type | Purpose |
|----------|------|---------|
| **A** | Simulated | Happy path—verify everything works with clean input |
| **B (this)** | Simulated | Edge cases—verify gap detection, contradiction flagging, error handling |
| **C** | Real | Real-world validation—verify system handles authentic messy content |

Campaign B intentionally includes flaws. A "passing" test means the system **detects** these flaws, not that it processes without errors.

---

## Files in This Directory

| File | Description |
|------|-------------|
| `briefing.md` | Candidate information with intentional gaps, contradiction specifications, minimal content |
| `website-copy.md` | Sparse website content (3 pages only), includes contradictory tax statement |

---

## Candidate Profile Summary

**John R. Miller** is a 52-year-old Republican small business owner running for city council in a fictional Ohio city.

**Background:**
- Owner, Miller's Hardware Store (26 years)
- Former Chamber of Commerce President
- Rotary Club member

**Only 3 Policy Areas:**
1. Fiscal Responsibility (anti-tax)
2. Public Safety (pro-police)
3. Economic Development (pro-business)

**Missing Policy Areas (7+ gaps):**
- Housing, Education, Healthcare, Environment, Infrastructure, Seniors, Immigration, Criminal Justice Reform

**Endorsements:** Only 2 (State Rep, Chamber of Commerce)

---

## The Intentional Contradiction

This is the core test for contradiction detection:

### Statement 1 (Website - Issues Page)
> "I will oppose any new taxes or fee increases. Period. Riverside families are taxed enough."

### Statement 2 (PDF - Campaign Announcement)
> "I support fully funding our police department, including the proposed 15% budget increase and the new public safety levy that will ask voters to approve a modest property tax increase."

**Detection Target:** The system should flag that opposing "any new taxes" contradicts supporting a "property tax increase" for the police levy.

---

## Implementation Notes

### Website
- **Minimal:** Only 3 working pages (Home, About, Issues)
- **Broken:** Events link returns 404
- **Basic:** No responsive design required, dated appearance acceptable
- **Sparse:** Minimal meta tags

### Documents
- `miller-announcement.pdf` only (2 pages, poorly formatted)
- Contains the contradictory statement about supporting the tax increase
- Simulates a scanned flyer or basic Word export

---

## Testing Checklist

| Test Case | Expected Result |
|-----------|-----------------|
| Scrape website | Retrieves 3 pages, logs 404 error for Events |
| Ingest PDF | Processes despite poor formatting |
| Generate coverage report | Shows 7+ gaps |
| Detect contradictions | Flags tax position inconsistency |
| Classify content | Correctly categorizes despite minimal content |
| Handle sparse data | No crashes, graceful degradation |

---

## Quick Reference

**Website:** https://millerforward3--civicai-43a01.web.app  
**Slogan:** "Common Sense for Riverside"  
**Key Test:** Detects gaps and contradictions  
**Expected Gaps:** 7+  
**Expected Contradictions:** 1 (tax policy)  
**Expected Errors:** 1 (404 on Events)

---

*This campaign is part of CivicAI's M1 test suite.*
