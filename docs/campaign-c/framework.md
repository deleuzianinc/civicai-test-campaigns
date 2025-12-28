# Candidate Briefing Template

## Campaign C: Real-World Validation

**Campaign Purpose:** Validate scraping and processing on real-world HTML, stress-test NLP with authentic political language patterns, and demonstrate system works outside "clean room" conditions with actual messy web content.

---

## Selection Framework

Unlike Campaigns A and B (simulated), Campaign C requires selecting a real past campaign at implementation time. This document provides the selection criteria, research methodology, and documentation template.

### Why a Framework Instead of Specific Candidate

1. **Campaign websites change or go offline** — A candidate selected today may have no accessible website tomorrow
2. **Content availability varies** — Need to verify sufficient content exists at implementation time
3. **Political sensitivity** — Want to avoid any campaign that becomes controversial
4. **Implementer judgment** — Person doing the scraping can best assess site structure and content quality

---

## Selection Criteria

### Must Have:
- [ ] **Completed race (2023 or 2024)** — Campaign is over, reducing political sensitivity
- [ ] **Local office** — City council, state representative, county commissioner, school board, mayor of small/medium city
- [ ] **NOT federal office** — Avoid U.S. House, Senate, President
- [ ] **Website still accessible** — Can load and scrape pages successfully
- [ ] **Has documented positions** — At least 3 issue areas with stated positions
- [ ] **English language** — Primary content in English

### Nice to Have:
- [ ] **Multiple page types** — About, Issues, Events, News sections
- [ ] **Mix of static and dynamic content** — Tests scraper robustness
- [ ] **Downloadable documents** — PDFs of position papers, press releases
- [ ] **Messy HTML** — Real-world complexity (not a clean template)
- [ ] **Some gaps** — Natural incomplete coverage for comparison with Coverage Report

### Avoid:
- ❌ **Highly partisan/divisive figures** — Could create bias perception in testing
- ❌ **Currently serving federal officials** — Too much external scrutiny
- ❌ **Campaigns with legal issues** — Lawsuits, investigations, scandals
- ❌ **Very recent losers** — May be planning another run (still active)
- ❌ **Sites behind paywalls or login walls**

---

## Research Methodology

### Step 1: Identify Candidate Pool

Use these sources to find completed local races:

1. **Ballotpedia** — ballotpedia.org/State_legislative_elections,_2024
   - Filter by state legislative or municipal
   - Look at both winners and losers
   
2. **Vote Smart** — votesmart.org
   - Search by state and office type
   - Check candidate profiles for website links

3. **Local news archives**
   - Search "[city name] city council election 2024"
   - Often link to candidate websites in coverage

4. **State Secretary of State websites**
   - Official candidate filings include campaign website URLs

### Step 2: Website Accessibility Check

For each candidate, verify:

```bash
# Quick accessibility check
curl -I https://[candidate-website].com

# Check for robots.txt restrictions
curl https://[candidate-website].com/robots.txt
```

Confirm:
- Site loads (200 status)
- No robots.txt blocks on key pages
- Pages have substantive content (not just redirects)

### Step 3: Content Assessment

Visit the site and document:

| Page | Exists | Content Quality | Notes |
|------|--------|-----------------|-------|
| Home | Y/N | High/Med/Low | |
| About/Bio | Y/N | High/Med/Low | |
| Issues | Y/N | High/Med/Low | |
| Events | Y/N | High/Med/Low | |
| News/Press | Y/N | High/Med/Low | |
| Contact | Y/N | High/Med/Low | |
| Downloads/PDFs | Y/N | High/Med/Low | |

**Minimum viable content:**
- At least 3 issue positions with 2+ sentences each
- Bio with professional background
- 1+ downloadable document OR substantial page content

### Step 4: Final Selection

Choose the candidate that best meets criteria. Document selection rationale.

---

## Documentation Template

Once a candidate is selected, complete this template:

---

## Candidate Information

**Full Name:** [Selected candidate name]  
**Party:** [Party affiliation]  
**Office Sought:** [Specific office]  
**District/Area:** [Geographic area]  
**State:** [State]  
**Election Year:** [2023 or 2024]  
**Election Result:** [Won/Lost]  
**Campaign Website:** [URL]

---

## Website Assessment

**Date Assessed:** [Date]  
**Site Status:** [Accessible/Partially Accessible/Issues]  
**Robots.txt Restrictions:** [None/Partial/Significant]

**Available Pages:**
- [ ] Home — URL: 
- [ ] About/Bio — URL:
- [ ] Issues/Platform — URL:
- [ ] Events — URL:
- [ ] News/Press — URL:
- [ ] Contact — URL:
- [ ] Other: _____ — URL:

**Downloadable Documents:**
- [ ] Document 1: [Name, format, URL]
- [ ] Document 2: [Name, format, URL]

---

## Content Inventory

### Biography Content
**Source URL(s):** 
**Content Summary:**
[Brief summary of available bio information]

### Policy Positions Found

| Issue Area | Present | Source Page | Summary |
|------------|---------|-------------|---------|
| Healthcare | Y/N | | |
| Education | Y/N | | |
| Housing | Y/N | | |
| Economy/Jobs | Y/N | | |
| Environment | Y/N | | |
| Public Safety | Y/N | | |
| Infrastructure | Y/N | | |
| Taxes/Fiscal | Y/N | | |
| Other: _____ | Y/N | | |

### Events
**Past events documented:** [Yes/No, count]
**Event content type:** [Calendar/List/News articles]

### Press/News
**Press releases available:** [Yes/No, count]
**News coverage links:** [Yes/No, count]

---

## Expected Test Outcomes

Based on content inventory, predict:

### Coverage Report
| Issue Area | Expected Result |
|------------|-----------------|
| Healthcare | Covered/Gap |
| Education | Covered/Gap |
| Housing | Covered/Gap |
| Economy | Covered/Gap |
| Environment | Covered/Gap |
| Public Safety | Covered/Gap |
| Infrastructure | Covered/Gap |
| Seniors | Covered/Gap |
| Immigration | Covered/Gap |

### Potential Contradictions
**Likelihood:** [Low/Medium/High]
**Areas to watch:** [List any areas where contradictions might exist]

### Scraping Challenges
**Anticipated issues:**
- [ ] JavaScript-rendered content
- [ ] Inconsistent HTML structure
- [ ] Missing meta tags
- [ ] Broken internal links
- [ ] Large media files
- [ ] Rate limiting
- [ ] Other: _____

---

## Synthesized Documents

Since real campaigns may not have all document types needed for testing, synthesize documents from available content:

### Document 1: Position Summary
**Format:** PDF  
**Source material:** Issues pages, speeches, interviews  
**Content:** Consolidated policy positions  
**Filename:** [candidate-lastname]-positions.pdf

### Document 2: Campaign Overview
**Format:** DOCX or MD  
**Source material:** Bio, endorsements, news coverage  
**Content:** Candidate background and campaign narrative  
**Filename:** [candidate-lastname]-overview.docx

### Document 3: Public Statements Compilation
**Format:** TXT  
**Source material:** Quotes from website, news articles, social media  
**Content:** Direct quotes organized by topic  
**Filename:** [candidate-lastname]-statements.txt

**Note:** Synthesized documents should be clearly marked as compilations of public statements and should cite sources. Do not fabricate positions the candidate did not actually take.

---

## Implementation Notes

### Scraping Considerations
- Respect rate limits (add delays between requests)
- Check robots.txt before scraping
- Store raw HTML for debugging
- Log any failed page loads

### Legal/Ethical Considerations
- Only use publicly available information
- Do not scrape password-protected content
- Attribute content to original sources
- Mark synthesized documents clearly

### Testing Verification
After ingestion, verify:
- [ ] Website pages scraped successfully
- [ ] Content classified correctly
- [ ] Coverage report reflects actual content
- [ ] Gaps match missing content
- [ ] Any contradictions detected match actual contradictions (if present)

---

## Suggested Candidates (Starting Points)

The following are starting points for research. **Verify all criteria at implementation time.**

### Option Pool 1: State Legislative (2024)
Research completed state house/senate races in these states known for good campaign website culture:
- California (large candidate pool)
- Colorado (transparent election system)
- Washington (strong digital campaigning)
- Minnesota (civic engagement culture)
- Virginia (competitive races with detailed platforms)

### Option Pool 2: City Council (2023-2024)
Medium-sized cities often have substantive local races:
- Austin, TX city council
- Portland, OR city council
- Denver, CO city council
- Minneapolis, MN city council
- Seattle, WA city council
- San Jose, CA city council

### Option Pool 3: County/School Board (2023-2024)
Often overlooked but can have detailed platforms:
- School board races in suburban districts
- County commissioner races
- Mayor races in cities 50K-200K population

---

## Quick Selection Checklist

Before finalizing Campaign C candidate:

- [ ] Website loads today
- [ ] Has at least 3 issue positions with real content
- [ ] Has bio/about page with professional history
- [ ] Race is completed (not upcoming)
- [ ] No major controversies in news search
- [ ] Content can be legally scraped (robots.txt check)
- [ ] Sufficient content for meaningful test
- [ ] HTML structure allows scraping (not entirely JavaScript-rendered)

**If all boxes checked → Proceed with documentation template above**

---

## Testing Checklist for M1

| Test Case | Expected Result |
|-----------|-----------------|
| Scrape real website | Handles messy HTML, extracts content |
| Process real language | NLP handles authentic political phrasing |
| Generate coverage report | Reflects actual gaps in real campaign |
| Detect contradictions | Finds any real contradictions (or correctly reports none) |
| Handle errors | Graceful failure on broken links, missing pages |
| Performance | Scraping completes in reasonable time |

---

*End of Campaign C Framework Document*
