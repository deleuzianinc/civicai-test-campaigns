# CivicAI Test Campaigns

Test data for M1 content ingestion pipeline validation.

## Scrape Targets

| Campaign | URL | Tests |
|----------|-----|-------|
| **A (Santos)** | https://santos4colorado.web.app | Happy path—complete content, 9 policy areas, clean HTML |
| **B (Miller)** | https://millerforward3.web.app | Edge cases—sparse content, 404 on Events, **intentional tax contradiction** |
| **C (Duchen)** | https://marcforaustin.com | Real-world—messy WordPress HTML, lorem ipsum garbage, empty calendar |

## The Contradiction (Campaign B)

**Website says:** "I will oppose any new taxes or fee increases. Period."

**Document says:** "I support... the property tax increase for the police levy."

Pipeline should flag this inconsistency.

## Documents

All in `documents/` directory:

- **Campaign A:** 5 docs (housing plan, education platform, fact sheet, town hall summary, volunteer handbook)
- **Campaign B:** 1 doc with contradiction (miller-announcement.pdf)
- **Campaign C:** None—pipeline synthesizes from web

## Deployment

Auto-deploys on push to `main` via GitHub Actions.

Manual: `firebase deploy --only hosting`

**Setup CI token:**
```bash
firebase login:ci
gh secret set FIREBASE_TOKEN  # paste token when prompted
```

---

**Repo:** https://github.com/deleuzianinc/civicai-test-campaigns  
**Firebase Project:** civicai-43a01
