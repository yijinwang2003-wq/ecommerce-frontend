# Ecommerce Frontend

React-based frontend service.

Release version 1.0.0  
Hotfix: corrected minor typo

---

## Git Workflow and Branching Strategy

This project follows the Git Flow branching model to manage development, releases, and production fixes in a structured way.

### Branch Types

- **main**
  - Production-ready code.
  - Only stable and tested code is merged into this branch.
  - Protected to prevent direct pushes.

- **develop**
  - Integration branch for active development.
  - All feature branches are merged here before release.

- **feature/\***
  - Created from `develop`.
  - Used for implementing new features.
  - Merged back into `develop` after completion.

- **release/\***
  - Created from `develop` when preparing a production release.
  - Merged into `main` once validated.
  - After merging into `main`, changes are synced back to `develop`.

- **hotfix/\***
  - Created from `main` to fix urgent production issues.
  - Merged into `main` to resolve the issue.
  - Then merged back into `develop` to keep branches consistent.

---

## Branch Interaction Summary

Feature workflow:
feature/* → develop

Release workflow:
develop → release/* → main → develop

Hotfix workflow:
main → hotfix/* → main → develop

This structured branching strategy ensures production stability while enabling continuous development.

---

## Design Decisions and Rationale

- A microservices architecture with separate repositories allows independent development and deployment.
- Git Flow was selected because it provides a clear and controlled release lifecycle.
- Feature branches isolate development work and reduce integration risk.
- Release branches stabilize code before production deployment.
- Hotfix branches allow urgent fixes without disrupting ongoing development.
- Branch protection rules enforce code review and prevent accidental changes to production.
