# Campaign B - John Miller Campaign Website

Minimal campaign website for testing purposes.

## Structure

- **index.html** - Home page with hero, donate button, email signup
- **about.html** - Biography and endorsements
- **issues.html** - Three policy positions (Fiscal, Public Safety, Economic Development)
- **contact.html** - Email address only
- **events.html** - 404 error page (intentional broken link)
- **style.css** - Basic dated styling

## Serving the Site

### Option 1: Python HTTP Server
```bash
cd site
python3 -m http.server 8000
```
Visit: http://localhost:8000

### Option 2: Node.js http-server
```bash
cd site
npx http-server -p 8000
```

### Option 3: PHP Built-in Server
```bash
cd site
php -S localhost:8000
```

## Testing Requirements

### Expected Behavior:
- ✅ Home, About, Issues, Contact pages functional
- ✅ Events link in navigation goes to 404 page
- ✅ Donate button links to external URL
- ✅ Email signup form (non-functional, HTML only)
- ✅ Contact page shows email only (no form)

### Content Preservation:
- Issues page contains exact anti-tax statement: "I will oppose any new taxes or fee increases. Period. Riverside families are taxed enough."
- This statement intentionally contradicts a separate PDF document (not included in website) for testing contradiction detection

### Gap Detection Targets:
The site deliberately omits common policy areas:
- Housing/Affordable Housing
- Education
- Healthcare
- Environment/Climate
- Infrastructure/Transportation
- Seniors
- Immigration
- Criminal Justice Reform

## Campaign Details

**Candidate:** John R. Miller  
**Office:** City Council, Ward 3  
**Location:** Riverside Heights, Ohio (fictional)  
**Party:** Republican  
**Slogan:** "Common Sense for Riverside"  
**Website:** millerforward3.com (simulated)

## Edge Case Testing Purpose

This site simulates a sparse, poorly-maintained campaign presence to stress-test scraping and analysis pipelines:
- Minimal content coverage
- Broken navigation links
- Missing standard pages (volunteer, press, endorsements)
- Intentional policy gaps
- Contradiction with external document
