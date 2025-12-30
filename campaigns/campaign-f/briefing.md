# Campaign F: Variable Complexity + Veteran Narrative

## DaSean Jones for Texas Supreme Court (Place 2)

**Campaign Purpose:** Test graceful handling of potentially sparse or inactive campaign content, validate veteran credential extraction, and confirm judicial campaign handling consistency with Campaign D.

---

## Candidate Information

| Field | Value |
|-------|-------|
| **Full Name** | Judge DaSean Jones |
| **Party** | Democratic |
| **Office Sought** | Texas Supreme Court, Place 2 |
| **District/Area** | Statewide (Texas) |
| **State** | Texas |
| **Election Year** | 2024 |
| **Election Date** | November 5, 2024 |
| **Election Result** | Lost to incumbent Jimmy Blacklock (R) |
| **Campaign Website** | https://www.daseanjones.com (⚠️ STATUS UNCERTAIN) |
| **Current Status** | Serving as 180th District Court Judge (Harris County) |

---

## Why This Candidate

### Test Value: Variable Complexity

Campaign F is the **edge case within real campaigns**. Unlike Campaign B (simulated edge cases), this tests **authentic uncertainty**:

| Scenario | Test Value |
|----------|------------|
| Site fully active | Normal judicial scraping (validates Campaign D approach) |
| Site sparse | Tests minimal content extraction |
| Site inactive/down | Tests graceful failure, third-party fallback |
| Site redirected | Tests handling of changed URLs |

**The uncertainty is the point.** This campaign teaches us how the system handles real-world variability that we can't control.

### Content Value: Veteran Narrative

DaSean Jones is the **only military veteran** in the entire test suite:

| Credential Type | Source |
|-----------------|--------|
| Military Service | U.S. Army combat veteran |
| Legal Career | Currently serving as 180th District Court Judge (Harris County) |
| Education | JD, Texas Southern University (Thurgood Marshall School of Law) |

**Unique Test:** Can the system:
- Extract military credentials alongside legal credentials?
- Recognize veteran narrative as distinct credential category?
- Handle diverse professional backgrounds in judicial candidates?

### Comparison Value: Judicial Pair Validation

Campaign F pairs with Campaign D (Weems) to validate **judicial campaign handling is consistent**:

| If Both Handled Correctly | Validation |
|---------------------------|------------|
| Same gap patterns (9 policy gaps) | Judicial gap detection works |
| Same content classification | Credentials vs bio vs endorsements |
| Same contradiction outcome (none) | Factual content handling |
| Different specific content | System generalizes beyond single candidate |

---

## Website Assessment

**⚠️ IMPORTANT: Verify status before implementation**

**Expected URL:** https://www.daseanjones.com  
**Status:** NEEDS VERIFICATION  
**Last Known State:** Active during 2024 campaign; post-election status unknown

### Verification Steps

```bash
# Step 1: Check if site loads
curl -I https://www.daseanjones.com

# Expected outcomes:
# - 200: Site active → proceed with scraping
# - 301/302: Redirect → document new URL
# - 404/503: Site down → use third-party sources
# - Connection refused: Site removed → use third-party sources

# Step 2: If site loads, check content
curl https://www.daseanjones.com | grep -i "dasean\|jones\|judge\|court"
```

### Possible Site States

| State | Likelihood | Response |
|-------|------------|----------|
| **Fully Active** | Medium | Scrape normally; document content |
| **Minimal/Sparse** | Medium | Document sparse state; supplement with third-party |
| **Inactive/Parked** | Medium | Document as edge case; use third-party entirely |
| **Repurposed** | Low | Document evolution (like Campaign D) |
| **Completely Down** | Low | Use third-party sources exclusively |

---

## Content Inventory (If Site Active)

### Expected Content

Based on 2024 campaign materials and third-party sources:

**Professional Background:**
- U.S. Army combat veteran
- Currently serves as Texas 180th District Court Judge (Harris County)
- Age: 45-46 (as of 2024)

**Education:**
- JD, Texas Southern University (Thurgood Marshall School of Law)

**Campaign Focus (expected):**
- Judicial reform
- Court transparency
- Veteran perspective on justice system

### Content Classification Targets

| Content Type | Expected Presence | Notes |
|--------------|-------------------|-------|
| Biography | ✅ Expected | Professional history, military service |
| Credentials | ✅ Expected | Legal certifications, bar admissions |
| Endorsements | ⚠️ Variable | May or may not be emphasized |
| Policy positions | ❌ Not expected | Judicial campaign norm |
| Events | ❌ Unlikely | Post-election, campaign concluded |

---

## Third-Party Fallback Sources

If primary website is sparse or unavailable, use these sources for document synthesis:

### Primary Sources

| Source | URL | Content Type |
|--------|-----|--------------|
| **Ballotpedia** | https://ballotpedia.org/DaSean_Jones | Comprehensive candidate profile |
| **Texas State Bar** | State Bar website | License verification |
| **Harris County Courts** | County judiciary site | Current judicial position |

### Secondary Sources (News/Coverage)

| Source | Content |
|--------|---------|
| San Antonio Report | Candidate profile, race coverage |
| Texas Civil Justice League | Judicial comparison ratings |
| Kendall County Democrats | Candidate spotlight |
| Texas Tribune | Election coverage |

### Synthesis Guidelines

When using third-party sources:
1. **Attribute clearly** — Note source for each piece of information
2. **Prioritize official sources** — Ballotpedia, state bar, court system
3. **Cross-reference** — Verify facts across multiple sources
4. **Document gaps** — Note what information is unavailable

---

## Expected Test Outcomes

### If Site Fully Active

| Test | Expected Result |
|------|-----------------|
| Website scraping | ✅ Content extracted (CMS unknown) |
| Veteran narrative | ✅ Military service captured |
| Credentials extraction | ✅ Legal and military credentials |
| Coverage report | ✅ 9 gaps (all policy—judicial norm) |
| Contradiction detection | ✅ None (factual content) |

### If Site Sparse/Inactive

| Test | Expected Result |
|------|-----------------|
| Error handling | ✅ Graceful failure, no crash |
| Fallback synthesis | ✅ Third-party sources used |
| Documentation | ✅ Edge case documented |
| Coverage report | ✅ Limited data acknowledged |

### Judicial Campaign Consistency (vs Campaign D)

| Dimension | Campaign D (Weems) | Campaign F (Jones) | Consistent? |
|-----------|-------------------|-------------------|-------------|
| Policy gaps | 9 (all) | 9 (all) | ✅ |
| Content type | Credentials-focused | Credentials-focused | ✅ |
| Contradictions | None | None | ✅ |
| Tone | Professional/formal | Professional/formal | ✅ |

---

## Synthesized Documents

### If Site Active

Create from website content:

**Document 1: Judicial Profile**
- Format: PDF
- Filename: `jones-judicial-profile.pdf`
- Content: Background, qualifications, judicial experience

**Document 2: Veteran Story**
- Format: TXT
- Filename: `jones-veteran-story.txt`
- Content: Military service narrative, veteran perspective

**Document 3: Endorsements (if available)**
- Format: DOCX
- Filename: `jones-endorsements.docx`
- Content: Campaign endorsements

### If Site Sparse/Inactive

Synthesize from third-party sources:

**Document 1: Candidate Profile (Compiled)**
- Format: PDF
- Filename: `jones-profile-compiled.pdf`
- Source: Ballotpedia, news articles, court records
- Note: Clearly marked as compiled from public sources

**Document 2: Career Timeline**
- Format: TXT
- Filename: `jones-career-timeline.txt`
- Source: State bar, court records
- Content: Military service → law school → legal career → judgeship → Supreme Court campaign

---

## Implementation Notes

### Decision Tree for Implementation

```
Step 1: Verify https://www.daseanjones.com
         |
         ├─── Site loads (200) ──→ Assess content depth
         |                         |
         |                         ├─── Full content ──→ Scrape normally
         |                         └─── Sparse content ──→ Scrape + supplement
         |
         └─── Site fails (4xx/5xx/connection refused)
                   |
                   └─── Use third-party sources exclusively
                        Document as edge case
```

### Scraping Considerations

**If site is active:**
- Unknown CMS—adapt scraping approach based on site structure
- Look for military service mentions specifically
- Extract judicial experience from current role
- Capture any endorsements present

**Rate limiting:** Standard delays (1-2 seconds between requests)

### Classification Challenges

| Challenge | Approach |
|-----------|----------|
| Military vs legal credentials | Both are valid credential categories; extract separately |
| Sparse content | Accept limited extraction; document coverage |
| Third-party synthesis | Attribute sources clearly; distinguish from primary |
| Unknown CMS | Adaptive scraping; test multiple approaches |

---

## Comparison to Other Campaigns

### Judicial Campaign Pair (D vs F)

| Aspect | Campaign D (Weems) | Campaign F (Jones) |
|--------|:------------------:|:------------------:|
| Court | Supreme Court Pl 4 | Supreme Court Pl 2 |
| Background | Civil litigator | Veteran + sitting judge |
| Site status | Active (repurposed) | **Unknown** |
| CMS | Wix | Unknown |
| Endorsements | Heavy emphasis | Unknown |
| Post-election | 2026 lower court run | Unknown |

### Full Test Suite Position

| Dimension | A | B | C | D | E | F |
|-----------|---|---|---|---|---|---|
| Type | Sim | Sim | Real | Real | Real | **Real** |
| CMS | Static | Static | WordPress | Wix | Squarespace | **Unknown** |
| Policy | Full | Sparse | Natural | None | Strong | **None** |
| Gaps | 0 | 7+ | 4-5 | 9 | 3-4 | **9** |
| Certainty | High | High | High | High | High | **Variable** |

**Campaign F is the only campaign with variable certainty**—this is the test value.

---

## Testing Checklist for M1

### Pre-Implementation

| Task | Status | Notes |
|------|--------|-------|
| Verify website status | ⬜ Pending | First step before any scraping |
| Assess content depth | ⬜ Pending | Full/sparse/inactive |
| Determine fallback needs | ⬜ Pending | Third-party source selection |

### If Site Active

| Test Case | Expected Result | Priority |
|-----------|-----------------|----------|
| CMS identification | ✅ Platform detected | High |
| Veteran narrative extraction | ✅ Military service captured | High |
| Credentials extraction | ✅ Legal + military credentials | High |
| Coverage report | ✅ Shows 9 gaps (judicial norm) | High |
| Consistency with Campaign D | ✅ Same patterns | Medium |

### If Site Sparse/Inactive

| Test Case | Expected Result | Priority |
|-----------|-----------------|----------|
| Graceful failure | ✅ No crash, informative error | High |
| Third-party synthesis | ✅ Sources used correctly | High |
| Edge case documentation | ✅ Behavior logged | Medium |
| Limited coverage acknowledged | ✅ Report reflects data availability | High |

---

## Quick Reference

**Candidate:** Judge DaSean Jones  
**Website:** https://www.daseanjones.com (⚠️ verify)  
**Office:** Texas Supreme Court, Place 2  
**Election:** November 2024 (Lost)  
**Platform:** Unknown  
**Status:** VARIABLE—requires verification  
**Expected Gaps:** 9 (all policy—judicial norm)  
**Expected Contradictions:** 0  
**Special Test Value:** Variable complexity, veteran narrative, graceful degradation

---

## ⚠️ First Step for Implementers

**Before any document synthesis or scraping:**

1. Visit https://www.daseanjones.com
2. Document site status (active/sparse/down)
3. If active: proceed with standard scraping
4. If sparse: scrape available + plan third-party supplement
5. If down: proceed directly to third-party synthesis

**This verification step is required.** Campaign F's value is testing variable conditions.

---

*End of Campaign F Briefing Document*
