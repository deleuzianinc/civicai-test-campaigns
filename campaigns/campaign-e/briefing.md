# Campaign E: Squarespace CMS + Progressive Municipal Platform

## Mike Siegel for Austin City Council (District 7)

**Campaign Purpose:** Test scraping of Squarespace-hosted sites, validate handling of progressive municipal campaign content, and examine post-election site transitions from active campaign to victory state.

---

## Candidate Information

| Field | Value |
|-------|-------|
| **Full Name** | Mike Siegel |
| **Party** | Non-Partisan (Progressive) |
| **Office Sought** | Austin City Council, District 7 |
| **District/Area** | District 7 (Central/North Austin) |
| **State** | Texas |
| **Election Year** | 2024 |
| **Election Dates** | November 5, 2024 (General); December 14, 2024 (Runoff) |
| **Opponent** | Gary Bledsoe |
| **Election Result** | Won (Runoff) |
| **Campaign Website** | https://www.siegelforaustin.org |
| **Current Status** | Serving as Council Member (took office January 2025) |

---

## Why This Candidate

### Technical Value: Squarespace CMS

This is the **first Squarespace-hosted site** in the test suite, testing:
- Squarespace-specific HTML/CSS structure
- Modern responsive design patterns
- Client-side rendering considerations
- Clean, template-based DOM (contrast with messy WordPress in Campaign C)

### Content Value: Progressive Municipal Platform

Mike Siegel represents **progressive municipal politics**, distinct from:
- Campaign A (Santos): Moderate Democratic state legislative
- Campaign C (Duchen): Moderate Democratic city council
- Campaign D/F: Non-ideological judicial campaigns

**Progressive Language Patterns:**
- "Pro-housing" (vs "affordable housing")
- "Pro-labor" (explicit workers' rights framing)
- "Pro-justice" (civil rights background)
- "Pro-climate" (environmental urgency)

**Opposition Context:**
Campaign materials reference "unrelenting negative and defamatory attacks by several right-wing PACs"—tests extraction of competitive dynamics beyond candidate's own positions.

### Site Evolution Value: Post-Victory Transition

The Siegel campaign site demonstrates **victory state content**:
- Homepage updated with election victory announcement
- "Thank you" messaging replaces calls-to-action
- Platform pages preserved alongside victory content
- Tests distinguishing campaign platform from post-election messaging

### Comparison Value: Austin City Council Pair

Campaigns C and E both represent **Austin City Council races** (2024):

| Dimension | Campaign C (Duchen, D10) | Campaign E (Siegel, D7) |
|-----------|--------------------------|-------------------------|
| Ideology | Moderate | Progressive |
| CMS | WordPress/Elementor | Squarespace |
| Site state | Active (post-win) | Victory (post-runoff) |
| Endorsements | 100+ listed | Less emphasis on quantity |
| Policy depth | 8 areas | 4-5 detailed areas |

This enables direct comparison of:
- Different CMS scraping patterns
- Different ideological language patterns
- Different approaches to municipal governance

---

## Website Assessment

**Date Assessed:** December 2024  
**Site Status:** ✅ Active (post-victory, now serving)  
**Platform:** Squarespace  
**Robots.txt Restrictions:** Standard Squarespace configuration

### Available Pages

| Page | URL | Status | Content |
|------|-----|--------|---------|
| Home | https://www.siegelforaustin.org | ✅ | Victory announcement, navigation |
| Issues - Affordability | /issues/affordability | ✅ | Housing/affordability platform |
| Issues - Climate | /issues/climate | ✅ | Environmental policy |
| Issues - Housing | /issues/housing | ✅ | Pro-housing agenda |
| Issues - Public Safety | /issues/public-safety | ✅ | Reform-oriented safety |
| Issues - Transportation | /issues/transportation | ✅ | Urban mobility |
| Get Involved | /get-involved | ✅ | Volunteer signup |
| Donate | /donate | ✅ | ActBlue integration |

### Technical Characteristics

```
Platform: Squarespace
Rendering: Client-side (JavaScript)
Design: Modern responsive
External Integration: ActBlue (donations)
SSL: Valid HTTPS
Mobile: Fully responsive
```

---

## Content Inventory

### Platform Pillars

**Source:** Issues pages

| Pillar | Focus | Key Positions |
|--------|-------|---------------|
| **Pro-Housing** | Affordability crisis | Zoning reform, density near transit, tenant protections |
| **Pro-Climate** | Environmental sustainability | Clean energy, green infrastructure, climate resilience |
| **Pro-Labor** | Workers' rights | Living wage, union support, worker protections |
| **Pro-Justice** | Civil rights | Police accountability, criminal justice reform, equity |

### Campaign Narrative

**Professional Background:**
- Civil rights attorney
- Previous campaigns for U.S. Congress (TX-10)
- Community organizer

**Campaign Themes:**
- "People power" grassroots approach
- Progressive alternative to establishment candidates
- Withstood well-funded PAC opposition
- District 7 represents diverse Austin neighborhoods

### Victory Messaging (Post-Runoff)

The homepage was updated after the December 2024 runoff victory to include:
- Election result announcement
- Thank you to supporters and volunteers
- Transition messaging (campaign to office)

**Test Value:** System should distinguish between:
- **Platform content** (issues pages) → policy classification
- **Victory messaging** (homepage) → bio/narrative classification

---

## Expected Test Outcomes

### Coverage Report

| Issue Area | Expected Result | Notes |
|------------|-----------------|-------|
| Affordability/Housing | **COVERED** | Primary campaign focus |
| Climate/Environment | **COVERED** | Dedicated page |
| Public Safety | **COVERED** | Reform-oriented approach |
| Transportation | **COVERED** | Urban mobility focus |
| Economy/Jobs | **PARTIAL** | Via pro-labor framing |
| Healthcare | **PARTIAL** | Peripheral references only |
| Education | **GAP** | Outside city council scope |
| Seniors | **GAP** | Limited coverage |
| Immigration | **GAP** | Limited coverage |

**Expected Gap Count:** 3-4 (education, seniors, immigration—city council scope)

**Natural Gap Explanation:** City councils have limited jurisdiction over education (AISD), senior services (county/state), and immigration (federal). These gaps reflect **appropriate scope** for municipal races.

### Content Classification

| Content Type | Expected Extraction |
|--------------|---------------------|
| Policy/Issues | ✅ Clear issue pages with substantial text |
| Biography | ✅ Professional background, campaign narrative |
| Victory messaging | ✅ Post-election homepage content |
| Calls-to-action | ⚠️ Volunteer signup, donate—identify but don't extract as substantive content |

### Contradiction Detection

**Likelihood:** None  
**Rationale:** Progressive positions are internally consistent. "Pro-housing" and "pro-justice" don't create contradiction opportunities like Campaign B's intentional tax contradiction.

### Technical Outcomes

| Test | Expected Result |
|------|-----------------|
| Squarespace HTML parsing | ✅ Clean DOM structure handled |
| JavaScript rendering | ⚠️ May need JS execution for full content |
| ActBlue link handling | ✅ External link identified, not followed |
| Form detection | ✅ Signup forms identified (not extracted as content) |
| Responsive design | ✅ Content consistent across viewports |

---

## Synthesized Documents

Create from website content:

### Document 1: Policy Platform Summary
**Format:** PDF  
**Source:** All issues pages  
**Filename:** `siegel-policy-platform.pdf`

**Content:**
- Affordability/Housing positions
- Climate/Environment positions
- Public Safety positions
- Transportation positions
- Pro-labor positions

### Document 2: Candidate Biography
**Format:** DOCX  
**Source:** About/bio content, campaign narrative  
**Filename:** `siegel-biography.docx`

**Content:**
- Professional background (civil rights attorney)
- Previous campaigns (TX-10)
- Community organizing experience
- Campaign narrative

### Document 3: Victory Statement
**Format:** TXT  
**Source:** Post-runoff homepage content  
**Filename:** `siegel-victory-statement.txt`

**Content:**
- Election result announcement
- Thank you messaging
- Transition to office statement

---

## Implementation Notes

### Scraping Considerations

```bash
# Verify site accessibility
curl -I https://www.siegelforaustin.org

# Check robots.txt
curl https://www.siegelforaustin.org/robots.txt
```

**Squarespace-Specific Notes:**
- Generally cleaner HTML than WordPress
- May use lazy loading for images
- Forms may have Squarespace-specific attributes
- ActBlue donation link is external (don't follow)

### Content Extraction Focus

1. **Issues pages** - Primary policy content (5 pages)
2. **Homepage** - Victory messaging, overview
3. **About/Bio** - Professional background
4. **Get Involved** - Campaign structure (metadata only)

### Classification Challenges

| Challenge | Approach |
|-----------|----------|
| Victory vs platform | Temporal context—victory is recent addition, platform is persistent |
| Progressive terminology | Map progressive language to standard policy categories |
| Opposition references | Extract as political context, not candidate position |
| Form elements | Identify as interactive, don't extract as content |

---

## Comparison to Other Campaigns

### Municipal Campaign Comparison (C vs E)

| Aspect | Campaign C (Duchen) | Campaign E (Siegel) |
|--------|:-------------------:|:-------------------:|
| District | Austin D10 | Austin D7 |
| Ideology | Moderate | Progressive |
| CMS | WordPress/Elementor | Squarespace |
| Policy depth | 8 areas | 4-5 areas |
| Endorsements | 100+ listed | Less emphasis |
| Site status | Active (serving) | Victory (just won) |
| HTML quality | Messy (Elementor) | Clean (template) |

### Full Test Suite Position

| Dimension | A | B | C | D | E | F |
|-----------|---|---|---|---|---|---|
| Type | Sim | Sim | Real | Real | **Real** | Real |
| CMS | Static | Static | WordPress | Wix | **Squarespace** | Unknown |
| Policy | Full | Sparse | Natural | None | **Strong** | Unknown |
| Gaps | 0 | 7+ | 4-5 | 9 | **3-4** | Variable |

---

## Testing Checklist for M1

| Test Case | Expected Result | Priority |
|-----------|-----------------|----------|
| Squarespace HTML scraping | ✅ Content extracted from clean DOM | High |
| Progressive language handling | ✅ Pro-X terminology mapped to policy categories | High |
| Victory messaging extraction | ✅ Post-election content captured | Medium |
| Issues page scraping | ✅ All 5 policy areas extracted | High |
| Coverage report | ✅ Shows 3-4 gaps (city council scope) | High |
| Contradiction detection | ✅ None found | Medium |
| ActBlue link handling | ✅ External link identified, not followed | Low |

---

## Quick Reference

**Candidate:** Mike Siegel  
**Website:** https://www.siegelforaustin.org  
**Office:** Austin City Council, District 7  
**Election:** November/December 2024 (Won Runoff)  
**Platform:** Squarespace  
**Key Pages:** /issues/* (5 pages)  
**Expected Gaps:** 3-4 (city council scope)  
**Expected Contradictions:** 0  
**Special Test Value:** Squarespace CMS, progressive terminology, victory messaging

---

*End of Campaign E Briefing Document*
