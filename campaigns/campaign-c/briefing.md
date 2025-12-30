# Campaign C: Real-World Validation

## Marc Duchen for Austin City Council (District 10, Texas)

**Campaign Purpose:** Validate scraping and processing on real-world HTML, stress-test NLP with authentic political language patterns, and demonstrate system works outside "clean room" conditions with actual messy web content.

---

## Candidate Information

| Field | Value |
|-------|-------|
| **Full Name** | Marc Duchen |
| **Party** | Democratic |
| **Office Sought** | Austin City Council, District 10 |
| **District/Area** | District 10 (Northwest Austin) |
| **State** | Texas |
| **Election Year** | 2024 |
| **Election Date** | November 5, 2024 |
| **Election Result** | **WON** |
| **Campaign Website** | https://marcforaustin.com |
| **Current Status** | Serving (took office January 2025) |

---

## Why This Candidate

Marc Duchen's campaign site provides exceptional testing value:

### Content Quality
- **8 detailed policy areas** with 4+ bullet points each
- **Rich biography** (1000+ words) - immigrant story, cancer survivor narrative, career in Democratic politics
- **100+ endorsements** from elected officials, organizations, neighborhood leaders
- **Blog posts** with campaign updates

### Real-World Messiness (Critical for Testing)
- **WordPress Elementor HTML** - complex, nested structure
- **Lorem ipsum placeholder text** in accordion tabs = garbage/noise detection test
- **Empty events calendar** = sparse content handling test
- **Mixed content types** on single pages = classification stress test

### Natural Gaps (for Coverage Report Comparison)
- ❌ NO Healthcare policy
- ❌ NO Education policy
- ❌ NO Immigration policy
- ❌ NO Seniors policy

These natural gaps allow direct comparison with Campaign A's 9-area coverage framework.

### Risk Profile: MINIMAL
- Race completed (November 2024)
- Candidate won (now serving as Council Member)
- No controversies or scandals
- Standard local municipal governance

---

## Website Assessment

**Date Assessed:** December 28, 2024  
**Site Status:** ✅ Accessible  
**SSL:** ✅ Valid HTTPS  
**Robots.txt Restrictions:** None (standard WordPress)

### Available Pages

| Page | URL | Status | Content Quality |
|------|-----|--------|-----------------|
| Home | https://marcforaustin.com | ✅ 200 | High - endorsements, intro, news |
| About/Bio | https://marcforaustin.com/my-story | ✅ 200 | High - detailed narrative |
| Issues/Platform | https://marcforaustin.com/issues | ✅ 200 | High - 8 policy areas |
| Events | https://marcforaustin.com/events-calendar | ✅ 200 | Low - empty calendar (post-election) |
| Blog | https://marcforaustin.com/blog | ✅ 200 | Medium - 3 posts |
| Get Involved | https://marcforaustin.com/get-involved | ✅ 200 | Medium |
| Testimonials | https://marcforaustin.com/testimonials | ✅ 200 | Medium |
| Donate | https://marcforaustin.com/donate | ✅ 200 | External link |

### Downloadable Documents

**None found** - Policy content is web-based only.

For testing, synthesize documents from web content (see Synthesized Documents section below).

---

## Content Inventory

### Biography Content

**Source URL:** https://marcforaustin.com/my-story

**Key Elements:**
- Born in Johannesburg, South Africa; immigrated to Houston at age 4
- UT Austin graduate (BA Government, MBA Entrepreneurship)
- Career in Democratic politics: ran campaigns across Texas, Research Director for Texas Democratic Party
- Founded technology engagement company focused on civic data
- Cancer survivor - diagnosed 2018
- District 10 resident for 24 years
- HOA board service managing ~$750,000 budget
- Austin Neighborhood Council executive committee

### Policy Positions Found

| Issue Area | Present | Source Page | Summary |
|------------|:-------:|-------------|---------|
| Environment | ✅ | /issues | Water conservation, parkland bonds, air quality, tree canopy |
| Public Safety | ✅ | /issues | Police/fire staffing, EMS, mental health response, gun safety |
| Mobility & Transit | ✅ | /issues | Project Connect evaluation, BRT, on-demand transit |
| Homelessness | ✅ | /issues | Shelter beds, permanent supportive housing, accountability |
| Spending/Fiscal | ✅ | /issues | Financial audits, sunset commission, bond oversight |
| Land Use/Housing | ✅ | /issues | Permitting reform, zoning near transit, neighborhood input |
| Wildfire Prevention | ✅ | /issues | AFD Wildfire Division, FireWise, WUI code |
| Road Safety | ✅ | /issues | Potholes, road calming, congestion pricing |
| Healthcare | ❌ | — | NOT ADDRESSED |
| Education | ❌ | — | NOT ADDRESSED |
| Immigration | ❌ | — | NOT ADDRESSED |
| Seniors | ❌ | — | NOT ADDRESSED |

### Events
**Past events documented:** Yes (blog posts reference Meet & Greet, Campaign Kick-Off)  
**Current calendar:** Empty ("No events to display")  
**Event content type:** WordPress calendar plugin

### Press/News
**Press releases available:** No dedicated press page  
**News coverage links:** Referenced on homepage (endorsements from Austin American-Statesman)

### Endorsements
**Organizational endorsements:**
- Austin American-Statesman
- Sierra Club
- Austin Firefighters Association
- Austin Police Association (Retired)
- Austin EcoDistrict
- Community Action Democrats
- BATPAC

**Individual endorsements:** 100+ names including:
- Hon. Alison Alter (current D10 Council Member)
- Hon. Brigid Shea (Travis County Commissioner)
- Adm. Bill McRaven (former UT System Chancellor)
- Multiple Travis County Democratic Precinct Chairs

---

## Expected Test Outcomes

### Coverage Report

Based on content inventory, the system should produce:

| Issue Area | Expected Result | Notes |
|------------|-----------------|-------|
| Healthcare | **GAP** | No content |
| Education | **GAP** | No content |
| Housing | **COVERED** | Via Land Use section |
| Economy/Jobs | **PARTIAL** | Mentioned in Land Use context only |
| Environment | **COVERED** | Detailed 4-point plan |
| Public Safety | **COVERED** | Detailed 4-point plan |
| Infrastructure | **COVERED** | Via Mobility, Road Safety |
| Seniors | **GAP** | No content |
| Immigration | **GAP** | No content (bio mentions being immigrant but no policy) |

**Expected gap count:** 4-5 gaps (Healthcare, Education, Seniors, Immigration, possibly Economy)

### Potential Contradictions

**Likelihood:** Low  
**Areas to watch:**
- Fiscal/spending positions vs. bond support (may need reconciliation)
- "Neighborhood preservation" vs. density support near transit

**Note:** Unlike Campaign B's intentional contradiction, any detected contradictions here would be authentic.

### Real-World Messiness Challenges

| Challenge | Where Found | Test Value |
|-----------|-------------|------------|
| Lorem ipsum placeholder | /issues accordion tabs | Garbage detection |
| Empty calendar | /events-calendar | Sparse content handling |
| Nested Elementor HTML | All pages | Parser robustness |
| Mixed endorsement formats | Homepage | Entity extraction |
| External donation link | /donate | Link following behavior |

---

## Synthesized Documents

Since Marc Duchen's campaign has no downloadable documents, synthesize test documents from web content:

### Document 1: Policy Platform Summary
**Format:** PDF  
**Source material:** /issues page content  
**Filename:** `duchen-policy-platform.pdf`

**Content to include:**
- All 8 policy sections from /issues
- Preserve bullet point structure
- Add header with candidate name, office, district
- Note: Include the lorem ipsum placeholder text to test garbage detection

### Document 2: Candidate Biography
**Format:** DOCX  
**Source material:** /my-story page content  
**Filename:** `duchen-biography.docx`

**Content to include:**
- Full narrative from bio page
- Professional history timeline
- Personal background sections

### Document 3: Endorsement Compilation
**Format:** TXT  
**Source material:** Homepage endorsements section  
**Filename:** `duchen-endorsements.txt`

**Content to include:**
- Organizational endorsements with quotes
- Individual endorsers by category
- Full endorsement quotes where available

---

## Implementation Notes

### Scraping Considerations

```bash
# Quick accessibility verification
curl -I https://marcforaustin.com
# Expected: HTTP/2 200

# Check robots.txt
curl https://marcforaustin.com/robots.txt
# Expected: Standard WordPress, no blocking
```

**Recommended scrape targets:**
1. https://marcforaustin.com (home - endorsements, overview)
2. https://marcforaustin.com/my-story (biography)
3. https://marcforaustin.com/issues (policy positions)
4. https://marcforaustin.com/events-calendar (empty calendar test)
5. https://marcforaustin.com/blog (campaign updates)

**Rate limiting:** Add 1-2 second delays between requests (good citizen behavior)

### Technical Notes

- **HTML Structure:** WordPress 6.9 + Elementor 3.34.0
- **JavaScript:** Minimal JS-rendered content; static HTML works
- **Images:** Standard JPG/PNG, no special handling needed
- **Forms:** Contact forms use reCAPTCHA (skip form scraping)

### Legal/Ethical Considerations

- ✅ All content is publicly available
- ✅ No password-protected content
- ✅ Campaign website intended for public consumption
- ✅ Candidate is now a public official
- ⚠️ Mark synthesized documents as compilations
- ⚠️ Attribute content to original source

---

## Testing Checklist for M1

| Test Case | Expected Result | Notes |
|-----------|-----------------|-------|
| Scrape real website | ✅ Handles WordPress/Elementor HTML | Complex nested structure |
| Process real language | ✅ NLP handles authentic political phrasing | Southwest Texas political vernacular |
| Generate coverage report | ✅ Shows 4-5 natural gaps | Compare to Campaign A's 9-area framework |
| Detect contradictions | ✅ Reports none (or minor) | No intentional contradictions |
| Handle sparse content | ✅ Events calendar returns empty | Graceful handling of "No events" |
| Handle garbage text | ✅ Lorem ipsum filtered or flagged | Accordion placeholder text |
| Performance | ✅ Scraping completes <30 seconds | 5-6 page site |

---

## Comparison with Other Campaigns

| Dimension | Campaign A (Santos) | Campaign B (Miller) | Campaign C (Duchen) |
|-----------|:-------------------:|:-------------------:|:-------------------:|
| Type | Simulated | Simulated | **REAL** |
| Policy areas | 9 (full) | 3 (sparse) | 8 (natural) |
| Gaps | 0 | 7+ | 4-5 |
| Contradictions | 0 | 1 (intentional) | 0-1 (natural) |
| Broken links | 0 | 1 (Events 404) | 0 |
| Documents | 4 types | 1 PDF | 0 (synthesize 3) |
| HTML quality | Clean | Clean | Messy (WordPress) |
| Test purpose | Happy path | Edge cases | Real-world validation |

---

## Quick Reference

**Candidate:** Marc Duchen  
**Website:** https://marcforaustin.com  
**Office:** Austin City Council District 10  
**Election:** November 2024 (WON)  
**Key Pages:** /issues, /my-story, /events-calendar  
**Expected Gaps:** Healthcare, Education, Seniors, Immigration  
**Expected Contradictions:** None (or minor)  
**Special Test Value:** Lorem ipsum placeholders, empty calendar, complex HTML

---

*End of Campaign C Briefing Document*
