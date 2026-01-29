# Action Repository

This repository is used to test GitHub webhooks.

## Purpose
Triggers webhooks on:
- Push events
- Pull request events
- Merge events

## Setup Webhook

1. Go to Settings → Webhooks
2. Add webhook with your endpoint URL
3. Select events: Push, Pull requests
4. Save

## Test Actions

### Test Push
```bash
echo "test" >> test.txt
git add .
git commit -m "Test push event"
git push
```

### Test Pull Request
1. Create a new branch
2. Make changes
3. Push branch
4. Create PR on GitHub

### Test Merge
1. Approve and merge the PR
2. Webhook will trigger with merge event

## Webhook Endpoint
Configure in Settings → Webhooks:
- URL: `https://your-webhook-url/webhook`
- Content type: `application/json`
- Events: Push, Pull requests
