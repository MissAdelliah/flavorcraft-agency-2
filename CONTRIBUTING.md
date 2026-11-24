
# Contributing to FlavorCraft Labs

## 1. Purpose

This document establishes the technical contribution guidelines for Team Alpha throughout the FlavorCraft Labs Agency 2 project.

The guidelines are based on:

- Agency 2 Course Assignment
- FlavorCraft Labs Client Brief
- Module 1 – Onboarding onto an Existing Codebase
- Module 2 – Git Workflow & Advanced GitHub Functions
- Module 3 – GitFlow, Branching, Staging & Deployment

The objective is to maintain a consistent, organised and traceable development workflow that supports collaboration, maintainability, quality assurance and individual contributions.

## 2. Documentation Index

- [Getting Started & Technical Setup](README.md)
- [Client Brief](CLIENT_BRIEF.md)
- [Workflow, Framework & Conduct](WORKFLOW_FRAMEWORK_CONDUCT.md)
- [AI Usage & Contribution Log](AI_LOG.md)

## 3. General Contribution Guidelines

All contributors are expected to:

- Work within the shared team repository.
- Follow the agreed technology stack and project architecture.
- Work on assigned and approved GitHub issues.
- Follow the established branching and commit conventions.
- Write maintainable, well-structured code.
- Review and test changes before submitting a pull request.
- Document relevant technical decisions and dependencies.
- Communicate technical blockers and challenges.
- Maintain evidence of individual contributions.
- Follow the established peer review and QA process.

## 4. Development Environment

Follow the installation and configuration instructions provided in the README.md before contributing.

All team members should use the agreed:

- Framework and programming language.
- Node.js version.
- Package manager.
- Dependencies.
- Folder structure.
- Linting and formatting configurations.
- Testing tools.
- Development environment configuration.

Technical decisions affecting the shared development environment must be discussed with the relevant team members.

## 5. Dependency Management

Dependencies must be managed consistently throughout the project.

- Use the agreed package manager.
- Review existing dependencies before introducing new ones.
- Discuss additional dependencies with the team.
- Ensure compatibility with the existing technology stack.
- Commit changes to package.json and the associated lock file.
- Do not commit node_modules.
- Do not remove or update shared dependencies without agreement.
- Document dependencies that require additional configuration.

For projects using npm, use:

```bash
npm install
```

For a clean installation using the committed package-lock.json:

```bash
npm ci
```

Do not delete or regenerate the shared lock file as a routine troubleshooting measure.

## 6. Git Workflow

The proposed workflow follows the GitFlow branching strategy introduced in Module 3.

### Branch Structure

| Branch | Purpose |
| --- | --- |
| main | Stable, production-ready application |
| develop | Integration and ongoing development |
| feature/* | New features and functionality |
| bugfix/* | Non-production bug fixes |
| release/* | Release preparation and final testing |
| hotfix/* | Urgent production fixes |
| docs/* | Documentation changes |
| chore/* | Configuration and maintenance |
| test/* | Testing-related contributions |

### Protected Branches

The main and develop branches should be protected.

- Do not push changes directly to protected branches.
- All changes must follow the pull request workflow.
- Force-pushing to protected branches is prohibited.
- At least one peer approval is required before merging.
- QA sign-off is required before merging into main.
- Applicable automated checks must pass before merging.

## 7. Starting a New Task

Before starting development:

1. Review the assigned GitHub issue.
2. Confirm the acceptance criteria.
3. Identify relevant dependencies.
4. Move the issue to In Progress.
5. Ensure your local development branch is up to date.
6. Create a branch for the assigned task.

Update your local development branch:

```bash
git switch develop
git pull --ff-only origin develop
```

Create a new working branch:

```bash
git switch -c feature/12-recipe-search
```

Replace the example branch name with the relevant issue number and task description.

## 8. Branch Naming Conventions

Branch names should be descriptive, lowercase and use hyphens between words.

### Format

```text
type/issue-number-short-description
```

### Examples

```text
feature/12-recipe-search
feature/15-recipe-details
feature/18-saved-recipes
bugfix/24-mobile-navigation
docs/26-update-readme
chore/30-configure-eslint
test/35-recipe-filtering
release/v1.0.0
hotfix/42-api-error
```

Each working branch should focus on one issue or clearly defined task.

## 9. Semantic Commit Conventions

The client requires semantic commit messages.
The team follows a Conventional Commits-style format.

### Format

```text
type(scope): description
```

The scope is optional.

| Type | Purpose |
| --- | --- |
| feat | New feature or functionality |
| fix | Bug fix |
| docs | Documentation changes |
| style | Code formatting without functional changes |
| refactor | Code restructuring without changing functionality |
| test | Adding or updating tests |
| chore | Maintenance and configuration |
| build | Build tools and dependency changes |
| ci | Continuous integration changes |
| perf | Performance improvements |
| revert | Reverting previous changes |

### Examples

```text
feat(search): implement recipe filtering
feat(favorites): add localStorage persistence
fix(api): handle failed recipe requests
fix(ui): resolve mobile navigation overflow
docs: update README installation instructions
docs: document AI assistance
refactor(components): simplify recipe card
test: add recipe search tests
chore: configure prettier
ci: add automated build checks
perf: optimise recipe images
```

### Commit Guidelines

- Keep commits small and focused.
- Use clear and descriptive commit messages.
- Use the imperative form.
- Avoid combining unrelated changes.
- Review staged changes before committing.
- Avoid unclear messages such as "update", "changes" or "final fix".

## 10. Submitting Changes

Review your changes:

```bash
git status
git diff
```

Stage the relevant files:

```bash
git add path/to/changed-file
```

Review staged changes:

```bash
git diff --staged
```

Commit your changes:

```bash
git commit -m "feat(search): implement recipe filtering"
```

Push your working branch:

```bash
git push -u origin feature/12-recipe-search
```

Create a pull request targeting develop and request a peer review.

## 11. Synchronising Branches

Regularly synchronise your working branch with develop to minimise merge conflicts.

From your working branch:

```bash
git fetch origin
git merge origin/develop
```

If merge conflicts occur:

- Review the affected files.
- Communicate with the relevant contributors.
- Resolve conflicts without removing other contributors' work unintentionally.
- Test the application after resolving conflicts.
- Commit and push the resolved changes.

Advanced Git commands such as interactive rebase, stash, reflog and cherry-pick may be used where appropriate.

Do not rewrite shared branch history without agreement.

## 12. Pull Requests

All contributions must follow the agreed pull request workflow.

### Pull Request Requirements

Each pull request should include:

- A clear and descriptive title.
- A summary of the changes.
- A reference to the relevant GitHub issue.
- Applicable acceptance criteria.
- Testing instructions and results.
- Screenshots for visual changes.
- Relevant documentation updates.
- Known limitations or outstanding issues.
- AI usage documentation where applicable.

### Target Branches

| Working Branch | Target Branch |
| --- | --- |
| feature/* | develop |
| bugfix/* | develop |
| docs/* | develop |
| chore/* | develop |
| test/* | develop |
| release/* | main, followed by synchronisation with develop |
| hotfix/* | main, followed by synchronisation with develop |

### Issue References

Reference the relevant issue in the pull request:

```text
Related to #12
```

Where appropriate, use closing keywords:

```text
Closes #12
```

GitHub automatically closes linked issues when the relevant pull request is merged into the default branch.

For pull requests targeting develop, update the issue and project board manually where necessary.

## 13. Peer Review

Peer reviews support collaboration, knowledge sharing and maintainability.

Reviewers should consider:

- Functionality and acceptance criteria.
- Code readability and maintainability.
- Application architecture.
- Project naming conventions.
- Potential bugs and edge cases.
- Accessibility and responsive behaviour.
- Performance.
- Unnecessary dependencies.
- Code duplication.
- Security and privacy considerations.

Review feedback should be constructive, specific and relevant to the contribution.

Contributors are responsible for addressing requested changes before merging.

## 14. Quality Assurance

The QA Lead establishes the testing strategy in collaboration with the developers and relevant team members.

Testing should cover applicable:

- Feature functionality.
- Acceptance criteria.
- Responsive layouts.
- Cross-browser compatibility.
- Accessibility.
- API loading and error states.
- Empty and no-results states.
- Search and filtering.
- Recipe details.
- Saved recipe persistence.
- Visual consistency.
- Performance and SEO.

Testing results and identified defects should be documented in the relevant GitHub issue or pull request.

QA sign-off is required before merging changes into main.

The client requires Lighthouse scores of 90 or higher across:

- Performance
- Accessibility
- SEO

## 15. Code Standards

All contributions should follow the agreed project architecture and framework conventions.

### General Standards

- Write clean, readable and maintainable code.
- Use descriptive names.
- Separate responsibilities appropriately.
- Create reusable components where appropriate.
- Avoid unnecessary complexity and duplicated code.
- Remove unused imports and unnecessary console logs.
- Follow the agreed linting and formatting configuration.
- Document complex logic where necessary.

### Front-end Standards

- Use semantic HTML.
- Follow responsive design principles.
- Consider accessibility throughout development.
- Follow the established design system.
- Maintain consistent component behaviour.
- Handle loading, error and empty states.
- Ensure interactive elements are usable across relevant devices.

### File & Folder Naming

The final naming conventions must align with the selected framework.

Proposed React conventions:

| Item | Convention | Example |
| --- | --- | --- |
| Components | PascalCase | RecipeCard.tsx |
| Custom Hooks | camelCase with use prefix | useRecipes.ts |
| Functions | camelCase | filterRecipes |
| Variables | camelCase | savedRecipes |
| Types and Interfaces | PascalCase | Recipe |
| Constants | UPPER_SNAKE_CASE | API_BASE_URL |
| CSS Modules | ComponentName.module.css | RecipeCard.module.css |
| Documentation | Descriptive naming | CONTRIBUTING.md |

## 16. SEO & Analytics

Contributions must support the client's technical requirements where applicable.

These include:

- Dynamic page titles.
- Dynamic meta descriptions.
- Open Graph metadata.
- Schema.org Recipe structured data (JSON-LD).
- Search engine indexing.
- Analytics and heatmapping.
- Performance and accessibility optimisation.

Implementation decisions should be coordinated with the SEO & Analytics Lead.

Analytics integrations must consider privacy, consent and responsible handling of user data.

## 17. Security & Configuration

Never commit:

- Passwords.
- API keys.
- Authentication tokens.
- Sensitive environment variables.
- Personal or confidential information.
- Installed dependencies.
- Unnecessary generated build files.

Where environment variables are required, provide an .env.example file containing variable names and non-sensitive example values.

Sensitive configuration files must be excluded through .gitignore.

## 18. AI-Assisted Contributions

AI tools are encouraged as part of the development and learning process.
All contributors remain responsible for understanding, reviewing, adapting and validating AI-assisted work.
Significant AI assistance should be documented in the
[AI Log](AI_LOG.md).
AI-assisted contributions follow the same peer review, testing and QA requirements as other contributions.

## 19. Documentation

All team members are responsible for maintaining documentation relevant to their contributions.
Update the README.md when changes affect:

- Technology stack.
- Dependencies.
- Application architecture.
- Folder structure.
- Installation instructions.
- Environment configuration.
- Development scripts.
- Testing procedures.
- API integrations.
- Deployment.

Documentation should accurately reflect the implemented project setup.
Changes related to an active task should be included in the existing working branch and pull request.
Standalone documentation changes should use a separate docs/* branch.

## 20. Release & Deployment

Release and deployment practices follow the GitFlow principles introduced in Module 3.

### Release Preparation

- Create a release branch from develop when required.
- Complete final testing and quality checks.
- Resolve outstanding defects.
- Update relevant documentation.
- Obtain peer approval and QA sign-off.
- Merge the approved release into main.
- Synchronise release changes with develop.

### Versioning

Release versions may follow semantic versioning:

```text
MAJOR.MINOR.PATCH
```

Example:

```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
git push origin v1.0.0
```

The agreed hosting platform, staging environment and CI/CD workflow must be documented in README.md.

## 21. Definition of Done

A contribution is considered ready for completion when all applicable criteria have been satisfied.

- [ ] Assigned requirements are implemented.
- [ ] Acceptance criteria are met.
- [ ] Code follows the agreed project conventions.
- [ ] Functionality has been tested.
- [ ] Responsive behaviour has been verified.
- [ ] Accessibility has been considered.
- [ ] Relevant error and empty states are handled.
- [ ] Applicable linting, build and test checks pass.
- [ ] Relevant documentation is updated.
- [ ] Significant AI assistance is documented.
- [ ] Pull request has received peer approval.
- [ ] QA verification has been completed where applicable.
- [ ] Required QA sign-off has been obtained before merging into main.
- [ ] Changes have been merged into the appropriate branch.
- [ ] GitHub issue and project board are updated.
- [ ] Product Owner acceptance has been obtained where required.

