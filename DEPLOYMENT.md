# Deployment Guide

## Firebase Hosting

Both campaign sites are deployed to Firebase using multi-site hosting.

### Live URLs

- **Campaign A (Santos):** https://santos4colorado.web.app
- **Campaign B (Miller):** https://millerforward3.web.app
- **Campaign C (Duchen):** https://marcforaustin.com (external)

---

## Manual Deployment

### Prerequisites

1. Firebase CLI installed: `npm install -g firebase-tools`
2. Authenticated: `firebase login`
3. Project configured: See `.firebaserc`

### Deploy Commands

```bash
# Deploy all hosting sites
firebase deploy --only hosting

# Deploy specific site
firebase deploy --only hosting:santos
firebase deploy --only hosting:miller
```

---

## GitHub Actions Auto-Deployment

### Setup

The repository includes a GitHub Actions workflow (`.github/workflows/deploy.yml`) that automatically deploys to Firebase when you push to the `main` branch.

#### Required Secret

You need to add a `FIREBASE_TOKEN` secret to your GitHub repository:

1. **Generate Firebase CI token:**
   ```bash
   firebase login:ci
   ```
   This will open a browser for authentication and output a token.

2. **Add secret to GitHub:**
   - Go to your repository → Settings → Secrets and variables → Actions
   - Click "New repository secret"
   - Name: `FIREBASE_TOKEN`
   - Value: Paste the token from step 1
   - Click "Add secret"

### Workflow Details

- **Trigger:** Push to `main` branch or manual dispatch
- **Actions:**
  1. Checkout code
  2. Install Node.js and Firebase CLI
  3. Deploy both sites to Firebase using the CI token

### Manual Workflow Trigger

You can manually trigger deployment from GitHub:
- Go to Actions tab → "Deploy to Firebase Hosting" → "Run workflow"

---

## Firebase Configuration

### Project Structure

```
Firebase Project: civicai-43a01 (CivicAI Development)
│
├── Hosting Site: santos4colorado
│   URL: https://santos4colorado.web.app
│   Source: sites/santos4colorado/
│   Target: santos
│
└── Hosting Site: millerforward3
    URL: https://millerforward3.web.app
    Source: sites/millerforward3/
    Target: miller
```

### Configuration Files

- **firebase.json** — Defines hosting targets and public directories
- **.firebaserc** — Maps targets to Firebase site IDs

### Multi-Site Hosting Targets

```json
{
  "santos": ["santos4colorado"],
  "miller": ["millerforward3"]
}
```

Each target maps a logical name to a Firebase hosting site ID, allowing independent deployment of each campaign site.

---

## Troubleshooting

### Permission Denied

If deployment fails with permission errors:
1. Verify you're authenticated: `firebase login`
2. Check project access: `firebase projects:list`
3. Verify project ID in `.firebaserc` matches your Firebase project

### Site Not Found

If a hosting site doesn't exist:
```bash
firebase hosting:sites:create santos4colorado
firebase hosting:sites:create millerforward3
```

### Target Not Applied

If targets aren't configured:
```bash
firebase target:apply hosting santos santos4colorado
firebase target:apply hosting miller millerforward3
```

### GitHub Actions Token Invalid

If CI deployment fails:
1. Regenerate token: `firebase login:ci`
2. Update `FIREBASE_TOKEN` secret in GitHub
3. Re-run the workflow

---

## Rollback

To rollback to a previous deployment:

```bash
# List previous releases
firebase hosting:channel:list

# Deploy specific version
firebase hosting:rollback
```

Or use the Firebase Console:
- Go to Hosting → View release history → Rollback

---

## Cost & Limits

Firebase Hosting free tier includes:
- 10 GB storage
- 360 MB/day bandwidth
- Custom domain support

These test campaigns are well within free tier limits.

---

## Additional Resources

- [Firebase Hosting Documentation](https://firebase.google.com/docs/hosting)
- [Multi-Site Hosting Guide](https://firebase.google.com/docs/hosting/multisites)
- [GitHub Actions for Firebase](https://github.com/marketplace/actions/deploy-to-firebase-hosting)
