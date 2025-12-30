# CivicAI Test Campaigns & Organizations

Test data repository for CivicAI's content ingestion pipeline, covering political campaigns and non-profit organizations.

## Repository Structure

```
campaigns/              Political campaign test cases
├── campaign-a/        
│   ├── README.md             Quick reference for dev team
│   ├── briefing.md           Comprehensive test case documentation
│   ├── documents/            Source documents to be ingested
│   └── santos4colorado/      Deployed website (Firebase)
├── campaign-b/
│   ├── README.md
│   ├── briefing.md
│   ├── documents/
│   └── millerforward3/       Deployed website (Firebase)
├── campaign-c/        Real-world WordPress test
├── campaign-d/        Wix CMS + Judicial race
├── campaign-e/        (future)
└── campaign-f/        (future)

non-profits/            Non-campaign civic organizations
└── texcap/
    ├── README.md
    ├── briefing.md
    └── documents/      Policy papers, reports
```

**Design Principle:** Everything related to a test case lives under one directory—documentation, source materials, and deployed sites together.

---

## Campaign Test Cases

### Campaign A: Santos for State Rep (Happy Path)
- **Site:** https://santos4colorado.web.app
- **Tests:** Complete content pipeline—9 policy areas, multiple document formats, clean HTML
- **Status:** Simulated (ideal baseline)

### Campaign B: Miller for City Council (Edge Cases)
- **Site:** https://millerforward3.web.app
- **Tests:** Sparse content, 404 errors, **intentional policy contradiction**
- **Status:** Simulated (error handling)
- **Contradiction:** Website opposes taxes; document supports property tax increase

### Campaign C: Duchen for City Council (Real World)
- **Site:** https://marcforaustin.com
- **Tests:** Real WordPress site, messy HTML, lorem ipsum placeholders
- **Status:** Real candidate (won election)

### Campaign D: Weems for TX Supreme Court (Judicial + Wix)
- **Site:** https://www.weemsforjudge.com
- **Tests:** Wix CMS scraping, judicial content patterns (no policy positions)
- **Status:** Real candidate (lost election, site repurposed)

### Campaign E: TBD
### Campaign F: TBD

---

## Non-Profit Test Cases

### TexCap Policy Institute
- **Site:** https://texcap.org
- **Tests:** WordPress CMS, **embedded PDF extraction**, think-tank content patterns
- **Status:** Real organization (first pilot customer)
- **Critical:** Website contains embedded policy papers that must be auto-extracted

---

## Documents Structure

Each test case contains a `documents/` subdirectory with source materials:

**Campaign A (Santos):**
- Housing plan (PDF)
- Education platform (DOCX)
- Fact sheet (PDF)
- Town hall summary (MD)
- Volunteer handbook (TXT)

**Campaign B (Miller):**
- Announcement with contradiction (PDF)

**Campaign C (Duchen):**
- None—pipeline synthesizes from website only

**TexCap:**
- 89th Legislative Session Report (PDF)
- Civil Rights Policy Position (HTML)

---

## For Developers

Each test case directory contains:
- **`README.md`** - Quick reference (what it tests, expected outcomes)
- **`briefing.md`** - Comprehensive documentation (content inventory, technical requirements, implementation notes)
- **`documents/`** - Source files for ingestion testing
- **`[site-name]/`** - Deployed website (campaigns A & B only)

**Start here:** Read the README for overview, then briefing for details.

---

## Deployment

**Auto-deploy:** Pushes to `main` trigger GitHub Actions deployment to Firebase.

**Manual deploy:**
```bash
firebase deploy --only hosting
```

**Setup CI token:**
```bash
firebase login:ci
gh secret set FIREBASE_TOKEN  # paste token when prompted
```

---

**Repository:** https://github.com/deleuzianinc/civicai-test-campaigns  
**Firebase Project:** civicai-43a01  
**Maintained by:** CivicAI Development Team
