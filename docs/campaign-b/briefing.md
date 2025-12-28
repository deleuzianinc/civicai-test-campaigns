# Candidate Briefing Template

## Campaign B: Edge Cases (Gaps & Contradictions)

**Campaign Purpose:** Verify gap detection in coverage reports, contradiction identification, graceful handling of sparse content, broken link handling, and minimal document ingestion.

---

## Candidate Information

**Full Name:** John R. Miller  
**Party:** Republican  
**Office Sought:** City Council, Ward 3  
**District:** Ward 3  
**State:** Ohio (fictional city: Riverside Heights)  
**Campaign Slogan:** "Common Sense for Riverside"  
**Campaign Website:** millerforward3.com (simulated)

---

## Biography

**Personal Background:**

John Miller, 52, has lived in Riverside Heights for 25 years. Married to Karen. Two adult children. Active member of First Baptist Church. Enjoys golf and fishing.

**Professional Background:**

- Owner, Miller's Hardware Store (1998-present)
- Former President, Riverside Heights Chamber of Commerce (2015-2018)
- Rotary Club member

**Why Running:**

"City Council has been spending too much. I want to bring a businessman's perspective to local government and make sure taxpayer dollars are spent wisely."

---

## Endorsements

**Elected Officials:**
- State Representative Tom Harrison

**Organizations:**
- Riverside Heights Chamber of Commerce

**Community Leaders:**
- (None listed)

---

## Policy Positions

### Fiscal Responsibility / Taxes

**Position:** Cut wasteful spending and oppose tax increases.

**Key Points:**
- Conduct line-by-line budget audit
- Oppose any new taxes or fee increases
- Reduce city workforce through attrition

**Detailed Stance:**

"Government needs to learn to live within its means, just like families and businesses do. I'll fight any attempt to raise taxes on hardworking Riverside residents. We don't have a revenue problem—we have a spending problem."

---

### Public Safety

**Position:** Support local police and fire departments.

**Key Points:**
- Back the blue
- Increase police presence downtown
- Oppose any cuts to public safety

**Detailed Stance:**

"I support our brave men and women in uniform. We need more officers on the street, not fewer. I'll oppose any attempts to defund our police department."

---

### Economic Development

**Position:** Support local businesses and attract new investment.

**Key Points:**
- Reduce regulatory burden on small businesses
- Attract new employers to the city
- Support downtown revitalization

**Detailed Stance:**

"As a small business owner for 26 years, I know what it takes to meet a payroll. We need to cut the red tape that's strangling local businesses and make Riverside Heights a place where companies want to invest."

---

## ⚠️ INTENTIONAL GAPS

**The following common issue areas are NOT addressed:**

- ❌ **Housing/Affordable Housing** — No position
- ❌ **Education** — No position
- ❌ **Healthcare** — No position
- ❌ **Environment/Climate** — No position
- ❌ **Infrastructure/Transportation** — No position
- ❌ **Seniors** — No position
- ❌ **Immigration** — No position
- ❌ **Criminal Justice Reform** — No position (only generic "support police")

**Expected Coverage Report Output:**
- Fiscal/Taxes: covered
- Public Safety: covered (partial—only pro-police, no reform positions)
- Economic Development: covered
- Housing: GAP
- Education: GAP
- Healthcare: GAP
- Environment: GAP
- Infrastructure: GAP
- Seniors: GAP
- Immigration: GAP

---

## ⚠️ INTENTIONAL CONTRADICTION

**Contradiction to Include:**

**Statement 1 (Website - Fiscal page):**
> "I will oppose any new taxes or fee increases. Period. Riverside families are taxed enough."

**Statement 2 (PDF Document - Press Release):**
> "I support fully funding our police department, including the proposed 15% budget increase and the new public safety levy that will ask voters to approve a modest property tax increase."

**Contradiction Detection Target:**
- The system should flag: "Candidate opposes tax increases" contradicts "Candidate supports property tax increase for public safety levy"
- Category: fiscal policy / public safety funding

---

## Events

| Event Name | Date | Type | Location | Description |
|------------|------|------|----------|-------------|
| Chamber of Commerce Endorsement Event | 2024-07-20 | Endorsement | Riverside Heights Country Club | Chamber announces endorsement; 30 attendees |
| Coffee with John | 2024-08-05 | Meet & Greet | Miller's Hardware Store | Informal meet and greet; 12 attendees |

**Note:** Sparse event calendar. No upcoming events listed after August.

---

## Campaign Materials

### Press Releases:

1. **"Local Businessman John Miller Enters Ward 3 Race"** (July 1, 2024)
   - Brief announcement, mentions business background
   - Quote: "It's time for common sense in city government."
   - No policy details

2. **"Miller Pledges Support for Police, Public Safety Levy"** (August 20, 2024)
   - Announces support for public safety levy
   - **CONTAINS CONTRADICTION** with tax pledge
   - Quote: "Public safety is worth paying for. I support the modest property tax increase to fund our police department's needs."

### Speeches/Statements:

- **None available**

### Position Papers:

- **None available**

### Other Documents:

1. **Campaign Announcement PDF**
   - 2-page PDF, mostly bio, minimal policy
   - Contains the contradictory public safety levy statement
   - **Format: PDF (poorly formatted, scanned appearance)**
   - Filename: miller-announcement.pdf

---

## Website Pages

### Must Have (Minimal Implementation):

**1. Home Page**
- Basic hero with candidate photo
- Slogan: "Common Sense for Riverside"
- Brief intro paragraph (3-4 sentences)
- Donate button
- Email signup

**2. About/Bio Page**
- Short biography (3 paragraphs max)
- Professional background
- Single endorsement mention
- **No family photos**

### Issues Page (Sparse):

**3. Issues Page**
- Only three issues listed (Fiscal, Public Safety, Economic Development)
- Each issue: 2-3 sentences only
- **No detailed policy pages**
- **CONTAINS TAX OPPOSITION STATEMENT** for contradiction

### Intentionally Missing/Broken:

**4. Events Page**
- **BROKEN LINK** - clicking "Events" returns 404 error
- Or: Page exists but shows "No upcoming events" with no past events archive

**5. Contact Page**
- Email only (no phone, no address)
- No contact form

### NOT Included:

- ❌ Volunteer page
- ❌ Donate page (just a button that goes to generic ActBlue)
- ❌ News/Press page
- ❌ Endorsements page (mentioned in bio only)

---

## Document Specifications

### Required Formats for M1 Testing:

| Document | Format | Filename | Purpose |
|----------|--------|----------|---------|
| Campaign Announcement | PDF | miller-announcement.pdf | Minimal PDF, contradiction test |

**Note:** Only ONE document type to test sparse content handling.

### Content Requirements:

The PDF should be:
- 2 pages maximum
- Contain the contradictory statement about supporting tax increase
- Poor formatting (simulating a scanned flyer or basic Word export)
- Limited metadata

---

## Notes for Implementer

### Website Implementation Notes:

**Critical: This site should be minimal and flawed:**
- Maximum 3 working pages (Home, About, Issues)
- Events link returns 404 error (test broken link handling)
- No responsive design required (can break on mobile)
- Basic/dated appearance acceptable
- Minimal meta tags

### Document Implementation Notes:

**PDF Characteristics:**
- Create as a basic scan/low-quality export
- Include the contradictory statement clearly
- Minimal structure (no table of contents, headers might be inconsistent)
- 2 pages only

### Content Classification Targets:

- About page → "bio" category
- Issues page content → "policy" category
- Announcement PDF → "misc" or "bio" category (ambiguous)

### Coverage Report Expectations:

This campaign should generate a coverage report showing **significant gaps**:

- ✓ Fiscal/Taxes: covered
- ✓ Public Safety: covered
- ✓ Economic Development: covered
- ✗ Housing: **GAP DETECTED**
- ✗ Education: **GAP DETECTED**
- ✗ Healthcare: **GAP DETECTED**
- ✗ Environment: **GAP DETECTED**
- ✗ Infrastructure: **GAP DETECTED**
- ✗ Seniors: **GAP DETECTED**
- ✗ Immigration: **GAP DETECTED**

### Contradiction Detection:

**Must Detect:**
- "Opposes all tax increases" vs. "Supports property tax increase for public safety levy"
- Severity: Medium-High (core fiscal message inconsistency)
- Location: Website Issues page vs. PDF announcement

---

## Appendix: Sample Content Excerpts

### Sample: Website Issues Page (Tax Opposition)

```html
<section class="issue">
  <h2>Fiscal Responsibility</h2>
  <p>I will oppose any new taxes or fee increases. Period. Riverside families are taxed enough. Government needs to learn to live within its means.</p>
</section>
```

### Sample: PDF Announcement (Contradictory Statement)

> **John Miller Pledges Support for Police**
>
> Riverside Heights businessman John Miller today announced his strong support for local law enforcement.
>
> "Our police officers put their lives on the line every day," Miller said. "I support fully funding our police department, including the proposed 15% budget increase and the new public safety levy that will ask voters to approve a modest property tax increase. Public safety is worth paying for."
>
> Miller, owner of Miller's Hardware Store, is running for City Council in Ward 3...

### Sample: 404 Error Page for Events

```html
<!DOCTYPE html>
<html>
<head><title>Page Not Found</title></head>
<body>
  <h1>404 - Page Not Found</h1>
  <p>Sorry, the page you're looking for doesn't exist.</p>
  <a href="/">Return to Home</a>
</body>
</html>
```

---

## Testing Checklist for M1

| Test Case | Expected Result |
|-----------|-----------------|
| Scrape website | Retrieves 3 pages, logs 404 error for Events |
| Ingest PDF | Processes despite poor formatting |
| Generate coverage report | Shows 7+ gaps |
| Detect contradictions | Flags tax position inconsistency |
| Classify content | Correctly categorizes despite minimal content |
| Handle sparse data | No errors, graceful handling |

---

*End of Campaign B Briefing Document*
