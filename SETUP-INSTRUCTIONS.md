# Setup Instructions for GitHub Actions

## Firebase CI Token Setup

To enable automatic deployment via GitHub Actions, you need to add a Firebase CI token to your repository secrets.

### Step 1: Generate Firebase CI Token

Run this command in a terminal:

```bash
firebase login:ci
```

This will:
1. Open your browser for Firebase authentication
2. After successful login, output a token in the terminal
3. Copy this token (starts with `1//...`)

### Step 2: Add Token to GitHub Secrets

#### Option A: Using GitHub CLI (Recommended)

```bash
# Set the token as an environment variable first
export FIREBASE_TOKEN="your-token-here"

# Add it to GitHub secrets
cd /home/trinity/Templates/civicai-test-campaigns
gh secret set FIREBASE_TOKEN --body "$FIREBASE_TOKEN"
```

#### Option B: Using GitHub Web Interface

1. Go to: https://github.com/tr1n1tycat/civicai-test-campaigns/settings/secrets/actions
2. Click "New repository secret"
3. Name: `FIREBASE_TOKEN`
4. Value: Paste your token from Step 1
5. Click "Add secret"

### Step 3: Verify Deployment

Once the secret is added:

1. Make any change to the repository
2. Commit and push to `main` branch
3. Go to Actions tab: https://github.com/tr1n1tycat/civicai-test-campaigns/actions
4. Watch the "Deploy to Firebase Hosting" workflow run
5. Verify both sites are updated:
   - https://santos4colorado.web.app
   - https://millerforward3.web.app

### Manual Workflow Trigger

You can also manually trigger deployment without pushing:

1. Go to: https://github.com/tr1n1tycat/civicai-test-campaigns/actions/workflows/deploy.yml
2. Click "Run workflow" dropdown
3. Select branch: `main`
4. Click "Run workflow" button

---

## Current Status

✅ Repository created: https://github.com/tr1n1tycat/civicai-test-campaigns
✅ Initial commit pushed
✅ GitHub Actions workflow configured
⏳ **PENDING:** Add `FIREBASE_TOKEN` secret (follow steps above)

Once the token is added, the CI/CD pipeline will be fully operational.
