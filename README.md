# flavorcraft-agency-2 Team Alpha
Description:
A recipe discovery web application developed for FlavorCraft Labs as part of Noroff's Agency 2 course. The application aims to reduce food waste and simplify recipe discovery through intuitive search, filtering and a distraction-free cooking experience.

Product Owner: Monde Sineke
Team: Alpha
Project Links
- Noroff API documentation
- Recipe Book API
- Figma: <!-- Add link -->
- GitHub Projects: <!-- Add link -->
- Live application: <!-- Add link -->

# Team Members
| Name | Role | GitHub |
| Silje Reppe | Scrum | MissAdelliah |
| Julie Thronæs | QA | |
| Anthony Apicella | Designer | |
| Priscilla Neeraas | Developer | |
| Nicklas Øen | Developer | |
| Tomine Rønningen Haug | Developer, SEO & Analytics | |

# Features
- Recipe feed, text search and category filtering
- Individual recipe pages with ingredients and instructions
- Saved recipes using localStorage
- Responsive and accessible design
- Dynamic metadata, Open Graph and Recipe JSON-LD
- Analytics and heatmapping

| Tool | Technology |
| --- | --- |
| Framework | <!-- Add selected framework --> |
| Language | <!-- JavaScript or TypeScript --> |
| Styling | <!-- Add selected styling solution --> |
| Package manager | <!-- Add selected package manager --> |
| API | Noroff Recipe Book API v2 |
| Design | Figma |
| Version control | Git & GitHub |
| Project management | GitHub Projects |
| Performance | Google Lighthouse |
| Testing | <!-- Add selected tools --> |
| Analytics | <!-- Add selected tool --> |
| Deployment | <!-- Add hosting platform --> |

# Getting Started
Prerequisites
- Git
- Node.js (version to be confirmed)
- Access to the shared GitHub repository

# Installation
Clone the repository and navigate into the project directory:
git clone <repository-url>
cd <repository-name>

Once the application has been initialized, if npm and a dev script are selected:
npm install
npm run dev

Open the local development URL shown in the terminal.

# Git Workflow
main — production-ready code
develop — integration branch
feature/* — new features
bugfix/* — bug fixes
release/* — release preparation
hotfix/* — urgent production fixes

Create a branch for each assigned task. Use semantic commit messages and link pull requests to their corresponding GitHub issues.
Protect the shared branches. Changes must receive at least one peer approval and QA sign-off before merging into main.

# Quality Assurance
The application will be tested for functionality, responsiveness, accessibility and performance. The target is a Lighthouse score of 90+ in Performance, Accessibility and SEO.



## Documentation

- [CONTRIBUTING.md](CONTRIBUTING.md) — Contribution guidelines, Git workflow, coding standards and team collaboration.
- [AI_LOG.md](AI_LOG.md) — Responsible AI usage guidelines and documentation of AI-assisted contributions.

### Updating the AI Log

All team members are responsible for documenting significant AI usage throughout the project.

#### Option 1: During an active task

If you use AI while working on an assigned task, update `AI_LOG.md` within your existing working branch.

Open the file:

```bash
code AI_LOG.md
```

Add your entry, save the file, and commit your changes:

```bash
git add AI_LOG.md
git commit -m "docs: document AI assistance"
git push
```

Include the changes in your existing pull request. There is no need to create a separate branch or pull request.

#### Option 2: After a completed task

If you forgot to document your AI usage and your original pull request has already been merged, create a separate documentation branch.

Update your local development branch:

```bash
git switch develop
git pull origin develop
```

Create a new branch:

```bash
git switch -c docs/update-ai-log
```

Open the file:

```bash
code AI_LOG.md
```

Add your missing entry, save the file, and commit your changes:

```bash
git add AI_LOG.md
git commit -m "docs: update AI usage log"
git push -u origin docs/update-ai-log
```

Create a pull request targeting `develop` and request a peer review.

### Documentation Guidelines

- Document AI usage as part of your regular workflow.
- Link entries to the relevant issue or pull request.
- Keep entries accurate and transparent.
- Do not remove or modify another contributor's entries without agreement.
- Do not push documentation changes directly to protected branches.
- Changes to contribution guidelines must be agreed upon by the team.

