# CivicAI Test Campaigns

Test campaign data for validating CivicAI's M1 content ingestion and analysis pipeline.

**Repository:** https://github.com/tr1n1tycat/civicai-test-campaigns

---

## Quick Links

| Campaign | Live URL | Docs | Documents | Status |
|----------|----------|------|-----------|--------|
| **A (Santos)** | [santos4colorado.web.app](https://santos4colorado.web.app) | [docs/campaign-a/](docs/campaign-a/) | [documents/campaign-a/](documents/campaign-a/) | ✅ Live |
| **B (Miller)** | [millerforward3.web.app](https://millerforward3.web.app) | [docs/campaign-b/](docs/campaign-b/) | [documents/campaign-b/](documents/campaign-b/) | ✅ Live |
| **C (Duchen)** | [marcforaustin.com](https://marcforaustin.com) | [docs/campaign-c/](docs/campaign-c/) | Pipeline synthesizes | ✅ Live |

---

## Directory Structure

```
civicai-test-campaigns/
├── README.md                    ← You are here
├── PROJECT-STATUS.md            ← Current status and next actions
├── QUICK-START.md               ← Developer quick reference
├── docs/                        ← Campaign briefings and context
│   ├── campaign-a/
│   │   ├── README.md           ← Happy path overview
│   │   ├── briefing.md         ← Full candidate/policy details
│   │   └── website-copy.md     ← Website content source
│   ├── campaign-b/
│   │   ├── README.md           ← Edge cases overview
│   │   ├── briefing.md         ← Sparse candidate details
│   │   └── website-copy.md     ← Minimal website content
│   └── campaign-c/
│       ├── README.md           ← Real-world validation overview
│       ├── briefing.md         ← Marc Duchen documentation
│       └── framework.md        ← Selection methodology (reference)
├── sites/                       ← Static HTML campaign websites
│   ├── santos4colorado/        ← Campaign A: Full site (13 pages)
│   │   ├── index.html
│   │   ├── about.html
│   │   ├── issues/
│   │   │   ├── index.html
│   │   │   ├── housing.html
│   │   │   ├── education.html
│   │   │   └── ... (9 policy areas)
│   │   ├── events.html
│   │   ├── volunteer.html
│   │   ├── donate.html
│   │   ├── news.html
│   │   ├── endorsements.html
│   │   ├── contact.html
│   │   └── css/styles.css
│   └── millerforward3/         ← Campaign B: Sparse site (4 pages + 404)
│       ├── index.html
│       ├── about.html
│       ├── issues.html
│       ├── contact.html
│       ├── events.html         ← Returns 404 (intentional)
│       └── style.css
└── documents/                   ← Test documents for ingestion
    ├── campaign-a/
    │   ├── housing-townhall-summary.md      ✅
    │   ├── volunteer-handbook.txt           ✅
    │   ├── santos-housing-plan.md           ✅ (convert to PDF)
    │   ├── santos-education-platform.md     ✅ (convert to DOCX)
    │   └── santos-fact-sheet.md             ✅ (convert to PDF)
    ├── campaign-b/
    │   └── miller-announcement.md           ✅ (convert to PDF, has contradiction)
    └── campaign-c/
        └── (empty - pipeline synthesizes from web)
```

---

## Testing Matrix

| Test Case | Campaign A | Campaign B | Campaign C |
|-----------|:----------:|:----------:|:----------:|
| **Type** | Simulated | Simulated | Real |
| **Policy Coverage** | 9/9 areas | 3/9 areas | 8/9 areas |
| **Expected Gaps** | 0 | 7+ | 4-5 (natural) |
| **Contradictions** | 0 | 1 (intentional) | 0 |
| **Broken Links** | 0 | 1 (Events 404) | 0 |
| **HTML Quality** | Clean | Basic | Messy (WordPress) |
| **Documents** | 5 (4 formats) | 1 PDF | Pipeline synthesizes |
| **Special Tests** | Happy path | Gap/contradiction detection | Real-world parsing, garbage detection |

---

## Campaign Summaries

### Campaign A: Maria Santos (Happy Path)

**Purpose:** Verify everything works with complete, well-structured content.

**Candidate:** Maria Elena Santos, Democratic candidate for Colorado State Representative (HD-42)

**Content:**
- ✅ Complete website (13 pages, all links working)
- ✅ 9 policy areas with detailed positions
- ✅ Rich biography (immigrant story, 20+ years housing policy)
- ✅ 100+ endorsements
- ✅ 5 test documents (markdown, ready for format conversion)

**Expected Results:**
- Coverage report: 100% complete
- Contradictions: None
- Errors: None

---

### Campaign B: John Miller (Edge Cases)

**Purpose:** Verify gap detection, contradiction flagging, error handling.

**Candidate:** John R. Miller, Republican candidate for City Council Ward 3 (Riverside Heights, OH - fictional)

**Content:**
- ✅ Sparse website (4 pages, minimal content)
- ✅ Events page returns 404 (intentional)
- ✅ Only 3 policy areas (Fiscal, Public Safety, Economic Development)
- ✅ 1 document with contradiction (markdown, ready for PDF conversion)

**Intentional Contradiction:**
- Website: "I will oppose any new taxes or fee increases. Period."
- Document: "I support... the property tax increase for the police levy."

**Expected Results:**
- Coverage report: 7+ gaps detected
- Contradictions: 1 detected (tax policy)
- Errors: 1 (404 on Events page)

---

### Campaign C: Marc Duchen (Real-World)

**Purpose:** Verify system handles authentic messy web content.

**Candidate:** Marc Duchen, Austin City Council District 10 (Texas) - **Real 2024 campaign, won election**

**Content:**
- ✅ Real website at https://marcforaustin.com
- ✅ 8 policy areas with authentic political language
- ✅ WordPress/Elementor HTML (complex nested structure)
- ✅ Lorem ipsum placeholder text (garbage detection test)
- ✅ Empty events calendar (post-election)
- ⏳ Documents synthesized by pipeline from web content

**Expected Results:**
- Coverage report: 4-5 natural gaps (Healthcare, Education, Seniors, Immigration)
- Contradictions: None expected
- Special: Lorem ipsum detected/filtered, empty calendar handled gracefully

---

## Live Deployments

All campaigns are live on Firebase:

- **Campaign A:** https://santos4colorado.web.app
- **Campaign B:** https://millerforward3.web.app
- **Campaign C:** https://marcforaustin.com

### Serve Locally (Development)

```bash
# Campaign A
cd sites/santos4colorado && python3 -m http.server 8001

# Campaign B
cd sites/millerforward3 && python3 -m http.server 8002
```

---

## Deployment

### Firebase Multi-Site Hosting

Both test campaigns are deployed via Firebase:

```bash
# Deploy all sites
firebase deploy --only hosting

# Deploy individually
firebase deploy --only hosting:santos   # Santos campaign
firebase deploy --only hosting:miller   # Miller campaign
```

**Auto-deployment:** GitHub Actions workflow deploys on push to `main` branch.

### Firebase Configuration

- **Project:** `civicai-43a01` (CivicAI Development)
- **Sites:**
  - `santos4colorado` → https://santos4colorado.web.app
  - `millerforward3` → https://millerforward3.web.app
- **Configuration:** See `firebase.json` and `.firebaserc`

---

## Next Steps

1. **Convert Documents** (when pandoc available)
   - Campaign A: 3 markdown → PDF/DOCX
   - Campaign B: 1 markdown → PDF

2. **Document Hosting**
   - Upload to Firebase Storage or GCS
   - Provide download links for pipeline testing

---

## Document Format Conversion

Once pandoc is installed:

```bash
# Install (Arch Linux)
sudo pacman -S pandoc texlive-core

# Campaign A
cd documents/campaign-a/
pandoc santos-housing-plan.md -o santos-housing-plan.pdf
pandoc santos-education-platform.md -o santos-education-platform.docx
pandoc santos-fact-sheet.md -o santos-fact-sheet.pdf

# Campaign B
cd documents/campaign-b/
pandoc miller-announcement.md -o miller-announcement.pdf
```

---

## Questions?

Review the README.md in each campaign's docs directory for detailed context on what each campaign tests and why.
