# Contributing Guidelines

Thank you for contributing to the Task Management System!  
Please follow these rules when creating branches, commits, and pull requests.

---

## Branch Strategy

- `main`  
  - Production‑ready code only.  
  - Protected branch; no direct pushes allowed.  
  - All changes must come via pull requests.

- `develop`  
  - Integration branch.  
  - All completed features are merged into `develop` first.  
  - Testing happens here before promotion to `main`.

- `feature/*`  
  - Each feature must use a separate branch.  
  - Created from `develop`.  
  - Examples:  
    - `feature/login-ui`  
    - `feature/task-api`  
    - `feature/docker-setup`  
    - `feature/testing-flow`

---

## Pull Request Rules

Every pull request must:

- Be reviewed and approved by at least one reviewer.  
- Pass all CI/CD checks (build, test, lint, security scan).  
- Have proper commit messages (see “Commit Naming Standard” below).  
- Not contain any secrets, API keys, or credentials.  
- Be tested locally before pushing.

---

## Commit Naming Standard

Use the following format:

- `feat: added login UI`
- `fix: resolved task delete issue`
- `docs: updated README`
- `refactor: cleaned API logic`

General pattern:

```text
<type>: <description>
```

Types:
- `feat`: new feature
- `fix`: bug fix
- `docs`: documentation changes
- `refactor`: code refactoring (no feature/bug change)

---

## How to Create a Pull Request

1. Create a feature branch from `develop`:
   ```bash
   git checkout develop
   git checkout -b feature/your-feature-name
   ```
2. Make changes, commit following the commit‑message format above.
3. Push the branch:
   ```bash
   git push origin feature/your-feature-name
   ```
4. Open a pull request from `feature/your-feature-name` into `develop`.
5. Fill in the PR template and link the related issue.
6. Wait for CI to pass and for at least one review approval.
