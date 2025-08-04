# Workflow Token Configuration

## Issue
Pull request workflows (like `CrossRefCheckWithAnchors.yml`, `MarkdownLinksCheck.yml`, etc.) were not being triggered when pull requests were created by the `create-reports.yml` GitHub Action.

## Root Cause
GitHub Actions using the default `GITHUB_TOKEN` cannot trigger other workflows when creating pull requests. This is a security feature to prevent infinite loops and potential security issues.

## Solution
The `create-reports.yml` workflow now uses a Personal Access Token (PAT) instead of the default `GITHUB_TOKEN` when creating pull requests. This allows the created pull requests to trigger other workflows.

### Change Made
Added `token: ${{ secrets.REPO_SCOPED_TOKEN }}` parameter to the `peter-evans/create-pull-request@v7` action in the `create-reports.yml` workflow.

### Required Repository Configuration
The repository needs to have a secret named `REPO_SCOPED_TOKEN` that contains a Personal Access Token with the following permissions:
- Contents: Write
- Pull requests: Write
- Metadata: Read
- Actions: Read (if workflows need to be triggered)

## Benefits
- Pull requests created by the automated workflow will now properly trigger checking workflows
- Ensures quality gates are applied to all pull requests, whether created manually or automatically
- Maintains security while enabling proper workflow orchestration