# Hugo CI/CD Example

Minimal Hugo site demonstrating CI/CD workflows with artifact-based deployment to a remote host.

## Overview

- **dev** branch → builds and deploys to preview environment
- **main** branch → builds and deploys to production environment
- **workflow_dispatch** → admin actions: rollback or pin to specific commit


## Admin Actions

Via GitHub Actions > "Run workflow":

- **rollback**: Deploy previous commit to production
- **pin**: Deploy a specific commit hash to production (requires `commit_hash` input)
