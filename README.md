# hugo-cicd-example

## users

Admins and Content Creators ("Users"). Users work on copies of the site and integrate into a preview site. Admins control the release to the production site.

## goals

- save space to create and preview blog, no hassle, good CI
- automated release to prod hardened with the tools available (roles, branch proctions, static code analysis, ...)
- release and rollback capabilites for control

## plan

create example blog repo with:

- dev and main branch
- github actions that:
  - on merge to main branch (or fast-forward production to the desired commit/tag?), build and deploy to production site)
  - on push to dev branch, build and deploy to preview site
  - on dispatch rolls back main to the previous commit and builds/deploys that
  - on dispatch with parameter commit hash sets main to that commit and builds/deploys that
