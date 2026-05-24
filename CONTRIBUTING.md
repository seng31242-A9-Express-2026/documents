# Contributing to A9 Express Documents Repository

Welcome to the official Documents Repository for the A9 Express project.

This repository contains all project-related documentation, diagrams, requirement specifications, and presentation materials developed throughout the software engineering project lifecycle.

---

# Repository Contents

The repository currently includes:

- SRS Draft
- Activity Diagrams
- Sequence Diagrams
- Use Case Diagrams
- Functional Requirements
- Non-Functional Requirements
- Use Case Descriptions
- Pitch Presentation Materials
- Supporting Project Documents

---

# Team Members

- Thevarasa Dayastan (SE/2022/007)
- Arulanantham Mathumithan (SE/2022/015)
- Vasanthakumar Arushanth (SE/2022/016)
- Surenthiran Sathurjan (SE/2022/035)
- Ensilirukman Ronald (SE/2022/042)

---

# Branch Strategy

This repository follows a protected branching workflow to maintain document quality and repository organization.

## Branch Types

### `main`

Protected branch containing finalized and approved documents.

Direct commits to `main` are not allowed.

---

### `draft/<document-name>`

Used for creating or updating documents and diagrams.

Examples:

- `draft/activity-diagrams`
- `draft/functional-requirements`
- `draft/use-case-descriptions`
- `draft/sequence-diagrams`

---

### `fix/<issue-number>`

Used for review corrections, formatting fixes, and revisions.

Examples:

- `fix/4`
- `fix/12`

---

# Contribution Workflow

All contributors must follow the workflow below:

1. Pull the latest changes from `main`
2. Create a new draft branch
3. Make documentation or diagram updates
4. Commit changes regularly
5. Push the branch to GitHub
6. Open a Draft Pull Request
7. Request peer review
8. Address all review comments
9. Merge after approval

---

# Commit Message Convention

This repository follows the Conventional Commits specification.

## Commit Types

| Type | Purpose |
|------|------|
| docs | Documentation updates |
| feat | Add new diagrams or document sections |
| fix | Correct errors or review feedback |
| refactor | Improve structure without changing content |
| style | Formatting-only changes |
| chore | Repository maintenance |

---

# Commit Format

```text
<type>(<scope>): <short description>
