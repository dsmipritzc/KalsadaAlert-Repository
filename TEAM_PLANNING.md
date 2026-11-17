# KalsadaAlert-Project Team Planning

This document provides a simple, step‑by‑step guide to create a **team planning project** (Kanban board) for the `KalsadaAlert-Repository` using the GitHub CLI.

---

## Prerequisites

1. **GitHub CLI (`gh`) installed** – you can verify with:
   ```
   gh --version
   ```
2. You are **authenticated** to GitHub:
   ```
   gh auth login
   ```
   Choose the appropriate account/organization (the repository belongs to `dsmipritzc`).
3. The repository is **cloned locally** (already done in `C:\Users\Gem\.gemini\antigravity\scratch\KalsadaAlert-Project`).

---

## Create the Kanban Project

Run the following command **inside the repository directory**:

```bash
cd C:\Users\Gem\.gemini\antigravity\scratch\KalsadaAlert-Project

gh project create \
  --repo dsmipritzc/KalsadaAlert-Repository \
  --title KalsadaAlert-Project \
  --template basic
```

- `--template basic` creates a simple **To‑Do / In‑Progress / Done** board (Kanban).
- The command will output the URL of the newly created project.

---

## Add Initial Columns (Optional)

If you prefer custom column names, you can edit the project in the GitHub UI or use:

```bash
gh project edit <PROJECT_NUMBER> --add-column "Backlog"
```

Replace `<PROJECT_NUMBER>` with the number shown after creation.

---

## Add Tasks (Issues) to the Project

For each task you want on the board, create an issue (if it does not already exist) and add it to the project:

```bash
# Example: create an issue
gh issue create \
  --title "Define alert criteria" \
  --body "Describe the criteria for road alerts."

# Add the issue to the project (replace ISSUE_NUMBER and PROJECT_NUMBER)
gh project add <PROJECT_NUMBER> --issue <ISSUE_NUMBER>
```

Repeat for all tasks listed in the original context document.

---

## Verify the Project

Open the project URL in a browser to see the board and ensure all columns and tasks appear as expected.

---

## Summary

- Clone repo (already done).
- Authenticate `gh`.
- Run the `gh project create` command above.
- Optionally modify columns and add issues.

You can now use the Kanban board to plan and track work for **KalsadaAlert-Project**.
