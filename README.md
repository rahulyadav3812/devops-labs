# devops-labs

This repository includes a starter **n8n GitHub automation workflow** that:

1. Listens for newly opened pull requests.
2. Posts a standard onboarding comment on the PR.

## Files

- `/n8n/workflows/github-pr-onboarding.json` – importable n8n workflow definition.

## How to use

1. Open n8n and choose **Import from File**.
2. Import `/n8n/workflows/github-pr-onboarding.json`.
3. In n8n, create/select a **GitHub API credential** and attach it to:
   - `GitHub Trigger` node
   - `Post PR onboarding comment` node
4. Set your repository owner and name in the workflow variables:
   - `owner`: GitHub org/user
   - `repository`: repository name
5. Activate the workflow.

## What it automates

When a pull request is opened, n8n automatically posts a welcome comment asking for:
- a summary of changes
- test evidence
- linked issue(s)
