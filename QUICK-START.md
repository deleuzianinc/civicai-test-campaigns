# Quick Start Guide

For developers who need to get the test campaigns running immediately.

---

## Prerequisites

- Python 3.7+ (for local web server)
- Web browser
- Git (for version control)

---

## Serve Sites Locally

### Campaign A (Santos)
```bash
cd sites/santos4colorado
python3 -m http.server 8001
```
Open: http://localhost:8001

**Test:**
- ✅ All 13 pages load
- ✅ All issue pages under /issues/ work
- ✅ All internal links work

---

### Campaign B (Miller)
```bash
cd sites/millerforward3
python3 -m http.server 8002
```
Open: http://localhost:8002

**Test:**
- ✅ Home, About, Issues, Contact pages load
- ✅ Events link returns 404 (this is intentional!)

---

### Campaign C (Duchen)
Already live: https://marcforaustin.com

**Test:**
- ✅ Site is accessible
- ✅ /issues page has 8 policy sections
- ✅ /my-story has full bio

---

## Point Your Scraper At

| Campaign | URL (local) | URL (deployed - TBD) |
|----------|-------------|----------------------|
| A | http://localhost:8001 | TBD: santos4colorado.web.app |
| B | http://localhost:8002 | TBD: millerforward3.web.app |
| C | https://marcforaustin.com | https://marcforaustin.com |

---

## Test Documents

Located in `documents/campaign-*/`

### Campaign A (5 documents)
- ✅ `housing-townhall-summary.md` — Event summary
- ✅ `volunteer-handbook.txt` — Plain text guide
- ✅ `santos-housing-plan.md` — Housing policy (convert to PDF)
- ✅ `santos-education-platform.md` — Education policy (convert to DOCX)
- ✅ `santos-fact-sheet.md` — Candidate summary (convert to PDF)

### Campaign B (1 document)
- ✅ `miller-announcement.md` — Campaign announcement (convert to PDF)
  - **Contains contradiction** for detection testing

### Campaign C (pipeline synthesizes)
- Documents are **not** manually created
- The scraping pipeline will synthesize documents from https://marcforaustin.com
- See `docs/campaign-c/briefing.md` for expected content

---

## Expected Test Results

### Campaign A (Santos)
```
Coverage Report: 9/9 policy areas covered
Contradictions: None
Broken Links: None
Classification: Bio, Policy, Events, Misc (clear)
```

### Campaign B (Miller)
```
Coverage Report: 3/9 policy areas covered (6 GAPS)
Contradictions: 1 detected (tax policy)
Broken Links: 1 (Events page 404)
Classification: Bio, Policy (sparse content handling)
```

### Campaign C (Duchen)
```
Coverage Report: 8/9 policy areas covered (4-5 natural gaps)
Contradictions: None expected
Broken Links: None
Special: Lorem ipsum filtered, empty calendar handled
```

---

## Understanding the Structure

```
civicai-test-campaigns/
├── docs/           ← Read this to understand what to test
├── sites/          ← Point your scraper here
└── documents/      ← Point your document ingestion here
```

**Workflow:**
1. Read `docs/campaign-a/README.md` → understand Campaign A
2. Serve `sites/santos4colorado/` → scrape the website
3. Ingest `documents/campaign-a/*` → process documents
4. Verify coverage report matches expectations in README

---

## Document Format Conversion

Markdown documents need conversion to PDF/DOCX for format testing:

```bash
# Install pandoc (Arch Linux)
sudo pacman -S pandoc texlive-core

# Convert Campaign A
cd documents/campaign-a/
pandoc santos-housing-plan.md -o santos-housing-plan.pdf
pandoc santos-education-platform.md -o santos-education-platform.docx
pandoc santos-fact-sheet.md -o santos-fact-sheet.pdf

# Convert Campaign B
cd documents/campaign-b/
pandoc miller-announcement.md -o miller-announcement.pdf
```

---

## Troubleshooting

**"Port already in use"**
```bash
# Kill process on port 8001
lsof -ti:8001 | xargs kill -9

# Or use a different port
python3 -m http.server 8003
```

**"Can't find sites directory"**
```bash
# Make sure you're in the project root
cd /home/trinity/Templates/civicai-test-campaigns
pwd  # Should show: /home/trinity/Templates/civicai-test-campaigns
```

**"Need PDF/DOCX versions"**
- Install pandoc and run conversion commands above
- Markdown files contain full content, just different format

---

## For More Detail

- **Overview:** [README.md](README.md)
- **Status:** [PROJECT-STATUS.md](PROJECT-STATUS.md)
- **Campaign A context:** [docs/campaign-a/README.md](docs/campaign-a/README.md)
- **Campaign B context:** [docs/campaign-b/README.md](docs/campaign-b/README.md)
- **Campaign C context:** [docs/campaign-c/README.md](docs/campaign-c/README.md)
