# Contributing Guidelines - SENG 31242 System Design Project

Welcome to the **A9 Express** development team! To maintain an industry-grade workspace and fully comply with the **University of Kelaniya Software Engineering Teaching Unit guidelines**, all team members must strictly adhere to the branching, committing, and peer-review workflows detailed below.

---

## 1. Team & Core Roles

To ensure accountability throughout the peer-review process, the core project responsibilities are distributed among the following team members:

- **Thevarasa Dayastan** (SE/2022/007)
- **Arulanantham Mathumithan** (SE/2022/015)
- **Vasanthakumar Arushanth** (SE/2022/016)
- **Surenthiran Sathurjan** (SE/2022/035)
- **Ensilirukman Ronald** (SE/2022/042)

---

## 2. Repository & Branching Strategy

Our organization follows a disciplined **linear branch workflow**. Direct pushes to the stable mainline are strictly restricted through GitHub branch protection configurations.

### Core Branches

- **`main`**  
  The protected production branch. It must always reflect stable, reviewed, and finalized deliverables approved by the team. Direct commits to this branch are strictly prohibited.

- **`draft/pitch-deck`**  
  Active development and research branches used for isolated work and feature implementation.



- **`fix/5`**  
  Dedicated branches used to address bugs, supervisor comments, peer-review feedback, or reported issues.



---

## 3. Main Branch Protection Rules

To prevent unreviewed additions, merge conflicts, and history inconsistencies, the `main` branch is protected with the following enforcement rules:

1. **Require Pull Requests Before Merging**  
   All changes must be submitted through a Pull Request (PR).

2. **Require Peer Approval**  
   At least **one team member** must formally review and approve a PR before merging.

3. **Dismiss Stale Approvals**  
   New commits pushed to a PR automatically invalidate previous approvals and require re-review.

4. **Require Linear History**  
   Only **Squash and Merge** or **Rebase and Merge** workflows are permitted. Traditional merge commits are disabled.

5. **Include Administrators**  
   Branch protection policies apply to all contributors, including repository owners and team leads.

---

## 4. Commit Message Convention

The project follows the **Conventional Commits Specification**, adapted for a system design engineering lifecycle. All commit messages must use the **imperative mood** (e.g., “add” instead of “added”, “fix” instead of “fixed”).

### Structural Format

```text
<type>(<scope>): <short imperative summary>

[Optional body: explain WHY the change was made, not WHAT changed]

[Optional footer: reference related GitHub issue numbers]