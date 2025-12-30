# Non-Profit Test Case: TexCap Policy Institute

## Overview

TexCap Policy Institute is a **real non-profit organization** representing the first non-campaign use case for CivicAI's content ingestion pipeline. This tests fundamentally different content patterns from political campaigns.

| Field | Value |
|-------|-------|
| **Organization** | TexCap Policy Institute (TXCPI) |
| **Type** | 501(c)(3) Non-Partisan Think Tank |
| **Founded** | June 2025 |
| **Location** | Austin, Texas |
| **Website** | https://texcap.org |
| **CMS Platform** | WordPress |
| **Status** | Real organization (first pilot customer) |

---

## Purpose

This non-profit case validates that CivicAI's pipeline can handle **non-campaign civic organizations** with fundamentally different content structures than political campaigns.

### What This Tests

| Capability | Test Scenario |
|------------|---------------|
| **WordPress CMS Scraping** | Different DOM structure than Wix/Squarespace campaigns |
| **Embedded PDF Extraction** | Policy papers embedded within website pages |
| **Research Content Classification** | Think-tank analysis vs campaign policy positions |
| **Pricing/Membership Pages** | Donation tiers, membership information |
| **Dynamic Blog Content** | Blog posts, news updates, event announcements |
| **Organizational Structure** | Board members, staff, partnerships |

### Key Non-Profit vs Campaign Differences

| Dimension | Political Campaign | Non-Profit Think Tank |
|-----------|-------------------|----------------------|
| **Content Focus** | Candidate-centric policy positions | Issue-centric research & analysis |
| **Tone** | Populist/persuasive | Academic/authoritative |
| **Events** | Rallies, town halls, canvassing | Conferences, workshops, networking |
| **Call-to-Action** | Vote, volunteer, donate to candidate | Support research, attend events, policy advocacy |
| **Endorsements** | Political figures, organizations | Academic citations, partner organizations |
| **Content Updates** | Campaign-cycle driven | Ongoing research publications |

### Expected Outcomes

**Coverage Report:**
Since non-profits don't map to campaign policy areas, coverage should reflect:
- ✓ Organizational Mission: covered
- ✓ Policy Research Areas: covered (Taxes, Infrastructure, Climate, Government Innovation)
- ✓ Leadership/Team: covered
- ✓ Publications: covered
- ✓ Events: covered
- ✓ Donation/Support: covered

**Contradictions:** Minimal expected (research positions are internally consistent)

**Errors:** None expected if WordPress scraping and PDF extraction work correctly

---

## Organization Profile Summary

**TexCap Policy Institute** is a non-partisan think tank focused on state and local policy in Texas. Founded by Gavin Nicholson, TXCPI designs private-sector guided, public-interest policies.

**Leadership:**
- **Gavin Nicholson** - Founder & CEO, Board Treasurer
- **Omar Zaki** - Board Chair
- **Ashley Myers** - Board Secretary (Exec Dir, Texas Association of Water Companies)
- **Joshua Lapidus** - Board Member (CEO, Azos Labs)
- **Zhelun Chen** - Board Member (Government Affairs)

**Focus Areas:**
1. Equitable Taxes
2. Infrastructure Investment
3. Climate & Resource Stewardship
4. Government Innovation

**Key Publications:**
- 89th Legislative Session Report
- Environmental Risk to Baseload Energy
- AI Policy Primer for Texas

---

## Files in This Directory

| File | Description |
|------|-------------|
| `briefing.md` | Complete organizational information, content inventory, pipeline requirements, technical considerations |
| `README.md` | This overview document |

## Related Documents (in `documents/`)

| File | Description |
|------|-------------|
| `TexCap-Policy-Institute-89th-Legislative-Session-Report.pdf` | Comprehensive legislative session analysis |
| `Civil Rights Policy - Comprehensive Position.html` | Detailed policy position paper (HTML format) |

---

## Critical Pipeline Requirements

### ⚠️ Embedded PDF Extraction

**TexCap's website contains multiple embedded policy paper PDFs** that are not manually uploaded but rather linked/embedded within pages. The scraping/ingestion pipeline must:

1. **Detect embedded PDF links** within WordPress pages
2. **Follow and extract PDF content** from embedded documents
3. **Associate PDFs with their parent page context**
4. **Handle WordPress media library URLs** (different from direct file paths)

### ⚠️ Dynamic Content Handling

WordPress sites have:
- Blog post pagination
- Category/tag archives
- Sidebar widgets with dynamic content
- Event calendar plugins

### ⚠️ Pricing/Donation Information

TexCap has donation tiers and membership information that should be extracted:
- Tax-deductible contribution options
- Membership benefits
- Support levels

---

## Quick Reference

**Website:** https://texcap.org  
**Platform:** WordPress  
**Key Test:** Non-campaign content patterns, embedded PDF extraction  
**Expected Issues:** Different coverage model than campaigns  
**Strategic Value:** First non-campaign pilot customer

---

*This non-profit case is part of CivicAI's expanded test suite beyond political campaigns.*
