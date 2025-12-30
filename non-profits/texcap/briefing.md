# Non-Profit Briefing: TexCap Policy Institute

## TexCap Policy Institute: First Non-Campaign Test Case

**Purpose:** Validate content ingestion pipeline for non-campaign civic organizations, test WordPress CMS scraping, embedded PDF extraction, and research content classification patterns.

---

## Organization Information

| Field | Value |
|-------|-------|
| **Full Name** | TexCap Policy Institute (TXCPI) |
| **Organization Type** | 501(c)(3) Non-Profit, Non-Partisan Think Tank |
| **Founded** | June 2025 |
| **Location** | Austin, Texas |
| **Website** | https://texcap.org |
| **CMS Platform** | WordPress |
| **Traffic** | ~300-400 unique visitors/month |
| **Status** | Active (first CivicAI pilot customer) |

---

## Why This Organization

### Strategic Value: First Non-Campaign Pilot

TexCap Policy Institute represents CivicAI's first expansion beyond political campaigns into the broader civic technology space:

- **Personal Connection:** Founder Gavin Nicholson is a known contact
- **Board Connection:** Omar Zaki (Board Chair) provides direct relationship
- **Pilot Customer:** First organization testing CivicAI for non-campaign use
- **Content Diversity:** Fundamentally different content patterns from campaigns

### Technical Value: WordPress CMS

This is the **first WordPress-hosted site** in the test suite, testing:
- WordPress-specific HTML/DOM structure
- WordPress media library URL patterns
- Plugin-generated content (events, forms)
- Blog post pagination and archives
- Category/tag taxonomy pages

### Content Value: Think Tank Patterns

Non-profit think tanks differ fundamentally from political campaigns:

| Dimension | Political Campaign | Think Tank (TexCap) |
|-----------|-------------------|---------------------|
| **Primary Content** | Policy positions (9 areas) | Research publications & analysis |
| **Content Lifecycle** | Election-cycle driven | Ongoing publication schedule |
| **Tone** | Persuasive, populist | Academic, authoritative |
| **Target Audience** | Voters, donors, volunteers | Policymakers, researchers, media |
| **Success Metrics** | Votes, donations | Policy impact, citations |
| **Events** | Rallies, town halls | Conferences, workshops, socials |
| **Endorsements** | Political figures | Academic citations, partnerships |

**Key Insight:** The content structure requires different classification logic than campaigns. Policy research is not the same as campaign policy positions.

---

## Leadership & Governance

### Board of Directors

| Name | Role | Background |
|------|------|------------|
| **Gavin Nicholson** | Founder & CEO, Board Treasurer | Nonpartisan policy expert |
| **Omar Zaki** | Board Chair | CivicAI relationship contact |
| **Ashley Myers** | Board Secretary | Executive Director, Texas Association of Water Companies; Director at Whitmire & Munoz LLC |
| **Joshua Lapidus** | Board Member | CEO and Founder, Azos Labs |
| **Zhelun Chen** | Board Member | Government Affairs Professional |

---

## Mission & Focus Areas

### Mission Statement

> To design and advocate for **private-sector guided**, **public-interest policies** that channel private capital into building long-term prosperity for all Texans through **infrastructure**, **equitable tax structures**, and **responsible governance** rooted in transparency, innovation, and impact.

### Vision

> To ground innovation in **ethical stewardship** and **prosperity** through public policy at the State and Local level, increasing quality of life without partisan division.

### Policy Focus Areas

#### 1. Equitable Taxes
Fairer tax systems that prioritize responsible stewardship of taxpayer dollars and balance Texas' growing needs.

#### 2. Infrastructure Investment
Increasing access to rural and urban broadband and expanding smarter multi-modal transportation systems.

#### 3. Climate & Resource Stewardship
Market-driven approaches to environmental sustainability including:
- Grid resiliency
- Diverse energy production (Nuclear, Geothermal, Hydro)
- Sustainable water policies

#### 4. Government Innovation
Increasing transparency, efficiency, civic tech, and local-first solutions including:
- Blockchain systems for government
- AI regulation and policy

### Guiding Methodologies

TexCap evaluates policy proposals against five key criteria:

| Methodology | Description |
|-------------|-------------|
| **Net Benefit to Texas Households** | Changes in disposable income, cost of living, and consumer purchasing power |
| **Fiscal Sustainability** | Long-run effects on state and local budgets, debt, and revenue stability |
| **Regional Competitiveness** | Ability to attract and retain jobs, investment, and talent across rural, suburban, and urban areas |
| **Return on Investment** | Economic impact, weighed by the net gains and losses experienced across all stakeholders |
| **Innovation & Productivity** | Degree to which policy spurs R&D, accelerates technology adoption, and boosts workforce efficiency |

---

## Website Assessment

**Date Assessed:** December 2024  
**Site Status:** ✅ Active  
**Platform:** WordPress  
**SSL:** Valid HTTPS

### Available Pages

| Page | URL | Content Type |
|------|-----|--------------|
| Home | https://texcap.org | Mission overview, focus areas, navigation |
| About | https://texcap.org/about | Vision, mission, methodologies, supporters |
| Team | https://texcap.org/team | Board members with bios and photos |
| Reports/Publications | Various blog posts | Policy papers, legislative reports |
| Donate | https://texcap.org/donate | Donation options, tax-deductible giving |
| Contact | https://texcap.org/contact | Contact form, campaign contact info |

### Technical Characteristics

```
Platform: WordPress
Rendering: Server-side (PHP) with some JavaScript enhancement
Image CDN: WordPress media library (wp-content/uploads)
SSL: Valid HTTPS
Mobile: Responsive
Blog Structure: WordPress post/page architecture
```

---

## Content Inventory

### Publications

#### 1. 89th Legislative Session Report (Flagship Publication)
**Format:** PDF (embedded/linked from website)  
**Location:** `documents/TexCap-Policy-Institute-89th-Legislative-Session-Report.pdf`

**Content:**
- Comprehensive analysis of Texas Legislature's impact
- Coverage areas: Taxes, Infrastructure, Water & Natural Resources, Technology
- Non-partisan evaluation of legislation
- First "proof-of-concept" publication demonstrating TXCPI's analytical approach

#### 2. Civil Rights Policy Position
**Format:** HTML  
**Location:** `documents/Civil Rights Policy - Comprehensive Position.html`

**Content:**
- Comprehensive civil rights position paper
- Topics: Racial Justice, Voting Rights, LGBTQ+ Rights, Women's Rights, Disability Rights, Religious Freedom, Immigration, Criminal Justice Reform, Hate Crimes
- Detailed policy recommendations for each area

#### 3. Environmental Risk to Baseload Energy (Referenced)
**Format:** PDF (embedded on website)  
**Content:** Report on retrofitting inactive wells into closed-loop geothermal systems

#### 4. AI Policy Primer (Referenced)
**Format:** PDF (embedded on website)  
**Content:** Overview of AI policy considerations for Texas

### Events

| Event | Date | Type | Description |
|-------|------|------|-------------|
| Launch Event | October 3, 2025 | Conference | Panel discussions on energy, technology, and AI |
| Winter Social | December 11, 2025 | Networking | Donor appreciation event at Higbie's in Austin |

---

## Expected Test Outcomes

### Coverage Report

Non-profits don't map directly to campaign policy areas. Expected classification:

| Content Category | Expected Result | Notes |
|-----------------|-----------------|-------|
| Organizational Info | ✅ Covered | Mission, vision, about pages |
| Leadership/Team | ✅ Covered | Board bios, staff information |
| Policy Research | ✅ Covered | Publications, reports, analysis |
| Events | ✅ Covered | Launch event, socials |
| Donation/Support | ✅ Covered | Donate page, membership info |
| Focus Areas | ✅ Covered | Four policy focus areas |

**Key Test:** System should recognize this as non-campaign content and apply appropriate classification logic.

### Content Classification Challenges

| Challenge | Approach |
|-----------|----------|
| Research vs Campaign Policy | Policy papers are analysis, not campaign promises |
| Academic Tone | Handle formal language appropriately |
| Embedded PDFs | Must extract PDFs linked within pages |
| Blog Post Format | WordPress posts vs static pages |
| Event Announcements | Different from campaign rallies |

### Contradiction Detection

**Likelihood:** Low  
**Rationale:** Research-based content is factual and analytical. Unlike campaign statements, policy analysis doesn't typically contain internal contradictions.

### Technical Outcomes

| Test | Expected Result |
|------|-----------------|
| WordPress HTML parsing | ✅ Handles WordPress DOM structure |
| Embedded PDF detection | ✅ Identifies PDFs in page content |
| PDF content extraction | ✅ Extracts text from linked PDFs |
| Blog post scraping | ✅ Captures post content and metadata |
| Image extraction | ✅ Handles WordPress media library URLs |
| Form detection | ✅ Contact/donation forms identified |
| Mobile responsiveness | ✅ Responsive design handled |

---

## Pipeline Requirements

### ⚠️ CRITICAL: Embedded PDF Extraction

**TexCap's website contains multiple policy paper PDFs embedded within pages.** These are NOT manually uploaded by the organization—they must be automatically extracted by the scraping/ingestion pipeline.

**Requirements:**
1. Detect `<a>` tags linking to PDF files
2. Detect `<embed>` and `<iframe>` elements containing PDFs
3. Follow WordPress media library URLs (`/wp-content/uploads/...`)
4. Extract full PDF text content
5. Associate PDF content with parent page context
6. Handle PDFs served via CDN or external hosting

**Test Cases:**
- 89th Legislative Session Report (direct link)
- Environmental Risk report (embedded)
- AI Policy Primer (embedded)

### ⚠️ WordPress-Specific Handling

**Page Structure:**
- Posts vs Pages distinction
- Category archives (`/category/...`)
- Tag archives (`/tag/...`)
- Author archives

**Content Areas:**
- Main content area (`article`, `.entry-content`)
- Sidebar widgets
- Footer content
- Navigation menus

**Dynamic Elements:**
- WordPress block editor content
- Plugin-generated content (events, forms)
- Widget areas

### ⚠️ Donation/Pricing Information

**Extract:**
- Donation tier options
- Tax-deductible status information
- Membership benefits
- Support levels and giving options

**Location:** `/donate` page and potentially sidebar widgets

---

## Comparison to Campaign Test Cases

| Aspect | Campaign A (Santos) | Campaign D (Weems) | TexCap (Non-Profit) |
|--------|:-------------------:|:------------------:|:------------------:|
| **Type** | State House candidate | Supreme Court judge | Think tank |
| **Content Style** | Policy positions | Credentials | Research & analysis |
| **Tone** | Populist | Professional | Academic |
| **Policy Areas** | 9 defined areas | None (judicial) | 4 focus areas |
| **CMS** | Static (simulated) | Wix | **WordPress** |
| **PDF Content** | Linked documents | Limited | **Embedded in pages** |
| **Event Types** | Rallies, town halls | Limited | Conferences, socials |
| **Real/Simulated** | Simulated | Real (lost) | **Real (active)** |

---

## Implementation Notes

### Scraping Considerations

```bash
# WordPress sites typically allow scraping
# Check robots.txt for restrictions
curl https://texcap.org/robots.txt

# Verify site accessibility
curl -I https://texcap.org
```

**WordPress-Specific Challenges:**
- Pagination on blog archives
- Lazy-loaded images
- Plugin-generated markup
- Sidebar content vs main content distinction

### Content Extraction Focus

1. **Homepage** - Mission, focus areas overview
2. **About Page** - Full mission, vision, methodologies
3. **Team Page** - Board member bios and roles
4. **Blog/Publications** - All policy papers and reports
5. **Donate Page** - Support options and membership
6. **Embedded PDFs** - All linked policy documents

### Classification Guidance

| Content Type | Classification |
|--------------|----------------|
| Mission/About | `organizational` |
| Team/Board Bios | `leadership` |
| Policy Papers | `research` |
| Legislative Reports | `research` |
| Event Announcements | `events` |
| Donation/Support | `support` |
| Blog Posts | `news` or `research` based on content |

---

## Document Specifications

### Existing Documents (in `documents/`)

| Document | Format | Filename | Purpose |
|----------|--------|----------|---------|
| 89th Legislative Session Report | PDF | `TexCap-Policy-Institute-89th-Legislative-Session-Report.pdf` | PDF ingestion test, research content |
| Civil Rights Policy | HTML | `Civil Rights Policy - Comprehensive Position.html` | HTML document ingestion test |

### Documents to Extract from Website

| Document | Format | Source | Notes |
|----------|--------|--------|-------|
| Environmental Risk Report | PDF | Embedded on site | Must auto-detect and extract |
| AI Policy Primer | PDF | Embedded on site | Must auto-detect and extract |
| Additional policy papers | PDF | Blog posts | Ongoing publications |

---

## Testing Checklist for M1

| Test Case | Expected Result | Priority |
|-----------|-----------------|----------|
| WordPress HTML scraping | ✅ Content extracted correctly | High |
| Embedded PDF detection | ✅ All PDFs identified | **Critical** |
| PDF content extraction | ✅ Full text extracted from PDFs | **Critical** |
| Non-campaign classification | ✅ Recognized as non-campaign org | High |
| Research content handling | ✅ Policy papers classified correctly | High |
| Team/leadership extraction | ✅ Board info captured | Medium |
| Event extraction | ✅ Event details captured | Medium |
| Donation page extraction | ✅ Support options captured | Medium |
| Blog pagination | ✅ All posts captured | Medium |
| WordPress media URLs | ✅ Images/PDFs from wp-content handled | Medium |

---

## Quick Reference

**Organization:** TexCap Policy Institute  
**Website:** https://texcap.org  
**Type:** 501(c)(3) Non-Profit Think Tank  
**Platform:** WordPress  
**Founded:** June 2025  
**Key Contact:** Gavin Nicholson (Founder), Omar Zaki (Board Chair)  
**Focus Areas:** Taxes, Infrastructure, Climate/Resources, Government Innovation  
**Key Publications:** 89th Legislative Session Report, Civil Rights Policy  
**Expected Challenges:** Embedded PDF extraction, non-campaign content classification  
**Expected Contradictions:** 0 (research-based content)  
**Special Test Value:** WordPress CMS, embedded PDFs, non-campaign content patterns, first pilot customer

---

*End of Non-Profit Briefing Document*
