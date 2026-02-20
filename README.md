# Ecommerce Frontend

React-based frontend service.

Release version 1.0.0
Hotfix: corrected minor typo

## Git Flow Branch Interaction

This project follows the Git Flow model.

Branch structure:

- main: production-ready code
- develop: integration branch for development
- feature/*: branched from develop and merged back into develop
- release/*: branched from develop and merged into main
- hotfix/*: branched from main and merged into both main and develop

Workflow summary:

feature/* → develop → release/* → main → develop  
hotfix/* → main → develop

## Design Decisions and Rationale

- Microservices architecture with separate repositories enables independent deployment and scalability.
- Git Flow was chosen because it provides structured release management.
- Feature branches allow isolated development.
- Release branches ensure production stability.
- Hotfix branches allow urgent fixes without disrupting ongoing development.
- Branch protection rules prevent direct pushes to main, improving code quality and safety.

