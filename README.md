# flavorcraft-agency-2 Team Alpha

Description:
A recipe discovery web application developed for FlavorCraft Labs as part of Noroff's Agency 2 course. The application aims to reduce food waste and simplify recipe discovery through intuitive search, filtering and a distraction-free cooking experience.

Product Owner: Monde Sineke

## Project Links

- [Noroff API Documentation](https://docs.noroff.dev/)
- [Recipe Book API](https://v2.api.noroff.dev/recipe-book/recipes)
- [Figma – Client Design Reference](https://www.figma.com/design/FAGzx9gqzNiLzP17GTyMQ1/Smart-Recipe-Book-Design?node-id=0-1&t=6xM4B1kADaljVm83-1)
- Team Figma Design: (https://www.figma.com/design/GEcU5wTsvtKA4qcJuANcV9/flavorcraft?node-id=0-1&t=rv71A1LM9GEsDKcL-1)
- GitHub Projects: (https://github.com/users/MissAdelliah/projects/11)
- Live Application: TBD

## Design System & UI Customization

The client has provided a preliminary Figma design as a baseline reference.
The provided design must not be directly replicated. The team is expected to develop its own visual identity, design system and user experience based on customer interviews, research findings and client requirements.
The final design should prioritise accessibility, responsiveness, usability and a distraction-free recipe discovery experience.

# Team Members

Name - Role - GitHub

- Silje Reppe | Scrum | MissAdelliah
- Julie Thronæs | QA | juliethron
- Anthony Apicella | Designer
- Priscilla Neeraas | Developer
- Nicklas Øen | Developer
- Tomine Rønningen Haug | SEO & Analytics | tominehaug

# Features

- Recipe feed, text search and category filtering
- Individual recipe pages with ingredients and instructions
- Saved recipes using localStorage
- Responsive and accessible design
- Dynamic metadata, Open Graph and Recipe JSON-LD
- Analytics and heatmapping

## Tech Stack

| Tool               | Technology                 |
| ------------------ | -------------------------- |
| Framework          | Next.js (React)            |
| Language           | TypeScript                 |
| Styling            | Tailwind                   |
| Package manager    | npm                        |
| API                | Noroff Recipe Book API v2  |
| Design             | Figma                      |
| Version control    | Git & GitHub               |
| Project management | GitHub Projects            |
| Performance        | Google Lighthouse          |
| Testing            | Manual testing             |
| Analytics          | <!-- Add selected tool --> |
| Deployment         | Vercel                     |

## Project Folder Structure EXAMPLE (needs to be established) (devs to update)

The project follows a modular folder structure based on introduced in the Agency 2 course material.
The proposed structure is subject to the team's final framework and technology stack decisions.

```text
flavorcraft-agency-2/
├── .github/
│   └── pull_request_template.md
│
├── public/
│
├── src/
│   ├── assets/ (logo, favicon)
│
│   ├── app/
│   │   ├── page.tsx
│   │   ├── layout.tsx
│   │   ├── recipe/[id]/page.tsx
│   │   ├── favorites/page.tsx
│   │
│   │
│   ├── components/
│   │   ├── ui/ Header.tsx, Footer.tsx
│   │   ├── recipes/ RecipeCard.tsx
│   │   ├── search/ SearchBar.tsx
│   │   └── favorites/
│   │
│   ├── hooks/ useFavorites.ts (read and write favorites in localStorage)
│   ├── services/
│   │   ├── api/ (all api calls)
│   │   └── analytics/
│   │
│   ├── types/ product.ts
│   ├── utils/
│   │   └── seo/
│   │
│
├── .gitignore
├── .prettierrc
├── eslint.config.js
├── package.json
├── package-lock.json
├── tsconfig.json
│
├── AI_LOG.md
├── CLIENT_BRIEF.md
├── CONTRIBUTING.md
├── QA_TEST_PLAN.md
├── WORKFLOW_FRAMEWORK_CONDUCT.md
└── README.md
```

# Getting Started

Prerequisites

- Git
- Node.js **v20.9.0 or higher**
- npm (comes with Node.js)

Check your node version with `node -v`

- Access to the shared GitHub repository

# Installation

Clone the repository and navigate into the project directory:
`git clone https://github.com/MissAdelliah/flavorcraft-agency-2.git`
`cd flavorcraft-agency-2`

Once the application has been initialized:
`npm install`
`npm run dev`

Open the local development URL shown in the terminal (usually http://localhost:3000)

# Git Workflow

main — production-ready code
develop — integration branch
feature/_ — new features
bugfix/_ — bug fixes
release/_ — release preparation
hotfix/_ — urgent production fixes

Create a branch for each assigned task. Use semantic commit messages and link pull requests to their corresponding GitHub issues.
Protect the shared branches. Changes must receive at least one peer approval and QA sign-off before merging into main.

# Quality Assurance

The application will undergo manual and automated testing to ensure functionality, responsiveness, accessibility and reliability.

## Testing Tools

- **Manual Testing:** Browser testing using Chrome DevTools to verify functionality and responsive layouts across different screen sizes.
- **Bug Tracking:** GitHub Issues to document, track and manage reported bugs.
- **Automated Testing:** Testing framework to be confirmed with the development team.
- **Code Quality:** ESLint for identifying potential code issues and Prettier for consistent code formatting.
- **Performance Testing:** Google Lighthouse to evaluate Performance, Accessibility and SEO.

## Testing Procedures

1. Developers implement and perform initial checks on their assigned features.
2. Completed features are moved to the In Review/QA column on GitHub Projects.
3. QA tests functionality against the relevant requirements and acceptance criteria.
4. Bugs are documented in GitHub Issues and assigned for resolution.
5. Developers address reported issues and request another QA review.
6. QA approval is required before changes are merged into the main branch.

## Testing Commands

Testing and code quality commands will be documented once the development environment and tooling have been finalised.

## Quality Standards

- Test functionality across desktop, tablet and mobile layouts.
- Verify loading states, empty states and API error handling.
- Check accessibility and usability.
- Perform regression testing when new features are introduced.
- Aim for Lighthouse scores of 90+ in Performance, Accessibility and SEO.

## Documentation

- [CONTRIBUTING.md](CONTRIBUTING.md) — Contribution guidelines, Git workflow, coding standards and team collaboration.
- [AI_LOG.md](AI_LOG.md) — Responsible AI usage guidelines and documentation of AI-assisted contributions.
- [WORKFLOW_FRAMEWORK_CONDUCT.md](WORKFLOW_FRAMEWORK_CONDUCT.md) - Not supposed to be updated or added to, Agile workflow, team responsibilities, communication, professional conduct and conflict resolution.

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
