This repo contains my CV and cover letter, generated with **RenderCV**.

- **Source of truth**: `cv/cv.yaml` and `cl/cl.yaml`
- **Automation**:
  - **PR opened**: renders **old (base)** vs **new (PR head)** PDFs, uploads both as artifacts, and comments the PR with links
  - **PR merged**: re-renders PDFs on the base branch and commits updated PDFs back to the repo
- **Outputs**: `cv/JamesWong_CV.pdf`, `cl/Cover letter.pdf`

## GitHub repo settings (required for the merge workflow)

If the "PR merged" workflow can't push updates back to `main`, check:

- **Actions token permissions**: Settings → Actions → General → Workflow permissions → **Read and write permissions**
- **If `main` is protected**:
  - Either allow GitHub Actions to push/merge via your branch rules, or
  - Allow Actions to create PRs: Settings → Actions → General → **Allow GitHub Actions to create and approve pull requests**
