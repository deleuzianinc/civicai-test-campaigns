# Campaign A: Happy Path (Full Coverage)

## Overview

Campaign A is a **simulated campaign** representing the ideal "golden path" scenario for testing CivicAI's content ingestion and analysis pipeline.

| Field | Value |
|-------|-------|
| **Candidate** | Maria Elena Santos |
| **Office** | Colorado State Representative, House District 42 |
| **Party** | Democratic |
| **Type** | Simulated (not a real campaign) |

---

## Purpose

This campaign validates that the system works correctly when provided with **complete, well-structured, internally consistent** campaign content. It establishes the baseline: if the system can't handle Campaign A perfectly, something is fundamentally broken.

### What This Tests

| Capability | Test Scenario |
|------------|---------------|
| **Document Ingestion** | All 4 formats: PDF, DOCX, TXT, MD |
| **Website Scraping** | Clean HTML with 6+ pages, all links working |
| **Content Classification** | Clear separation into bio/policy/events/misc categories |
| **Coverage Report** | 100% completeness across 9 policy areas |
| **Contradiction Detection** | Should find **zero** contradictions |

### Expected Outcomes

**Coverage Report:**
- ✓ Healthcare: covered
- ✓ Education: covered
- ✓ Housing: covered
- ✓ Economy/Jobs: covered
- ✓ Environment: covered
- ✓ Public Safety: covered
- ✓ Infrastructure: covered
- ✓ Seniors: covered
- ✓ Immigration: covered

**Contradictions:** None (all positions internally consistent)

**Errors:** None (all links work, all documents parse)

---

## Context: The Three-Campaign Framework

CivicAI's M1 milestone uses three campaigns to validate the content pipeline:

| Campaign | Type | Purpose |
|----------|------|---------|
| **A (this)** | Simulated | Happy path—verify everything works with clean input |
| **B** | Simulated | Edge cases—verify gap detection, contradiction flagging, error handling |
| **C** | Real | Real-world validation—verify system handles authentic messy content |

Campaign A must succeed before testing B or C. It's the control case.

---

## Files in This Directory

| File | Description |
|------|-------------|
| `briefing.md` | Complete candidate information, policy positions, event calendar, document specifications, website structure |
| `website-copy.md` | Full website content for all pages (Home, About, Issues, Events, etc.) |

---

## Candidate Profile Summary

**Maria Elena Santos** is a 47-year-old Democratic candidate with 20+ years in housing policy. First-generation college graduate, daughter of Mexican immigrants, married to a high school teacher with two children.

**Professional Background:**
- Executive Director, Colorado Nonprofit Housing Coalition (current)
- Deputy Director, Aurora Housing Authority
- Policy Analyst, Colorado Department of Local Affairs

**9 Policy Areas with Detailed Positions:**
1. Housing & Affordability
2. Education (K-12)
3. Healthcare Access
4. Economy & Jobs
5. Environment & Climate
6. Public Safety & Criminal Justice
7. Infrastructure & Transportation
8. Seniors & Aging
9. Immigration

**Endorsements:** State Senator Angela Williams, Mayor Mike Coffman, Colorado AFL-CIO, Sierra Club, Colorado Education Association, and 20+ others.

---

## Implementation Notes

### Website
- Build as static HTML/CSS (6+ pages)
- All internal links must work
- Include semantic HTML and meta tags
- Mobile responsive

### Documents
- `santos-housing-plan.pdf` (5+ pages, tables, headers, bullet points)
- `santos-education-platform.docx` (4+ pages, embedded images)
- `volunteer-handbook.txt` (2000+ words, plain text)
- `housing-townhall-summary.md` (500+ words, markdown formatting)

---

## Quick Reference

**Website:** https://santos4colorado--civicai-43a01.web.app  
**Slogan:** "Building Bridges, Not Barriers"  
**Key Test:** Everything works perfectly  
**Expected Gaps:** 0  
**Expected Contradictions:** 0

---

*This campaign is part of CivicAI's M1 test suite.*
