# Create action-repo on GitHub

## Step 1: Create Repository
1. Go to: https://github.com/new
2. Repository name: action-repo
3. Description: Repository for testing GitHub webhooks
4. Public repository
5. Do NOT initialize with README (we already have files)
6. Click "Create repository"

## Step 2: Push Local Code
Run these commands after creating the repository:

git remote add origin https://github.com/Raj7442/action-repo.git
git branch -M main
git push -u origin main

## Step 3: Configure Webhook
1. Go to: https://github.com/Raj7442/action-repo/settings/hooks
2. Click "Add webhook"
3. Payload URL: https://your-ngrok-url.ngrok.io/webhook
4. Content type: application/json
5. Events: Push, Pull requests
6. Active: ✓
7. Click "Add webhook"