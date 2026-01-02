This repo contains my CV, generated with **RenderCV**.

- **Source of truth**: `cv/cv.yaml`
- **Automation**:
  - **PR opened/updated**: renders **old (base)** vs **new (PR head)** CV PDFs, uploads both as artifacts, and comments the PR with links
  - **PR merged**: re-renders the CV on the base branch and commits the updated PDF back to the repo (or opens a fallback PR if the base branch is protected)
- **Tracked output**: `cv/JamesWong_CV.pdf`

### Local generation

RenderCV writes the generated PDF into `cv/rendercv_output/` (ignored by git). To update the tracked PDF locally:

```bash
rendercv render cv/cv.yaml -nomd -nohtml -nopng
cp -f cv/rendercv_output/*.pdf cv/JamesWong_CV.pdf
```

## GitHub repo settings (required for the merge workflow)

If the "PR merged" workflow can't push updates back to `main`, check:

- **Actions token permissions**: Settings → Actions → General → Workflow permissions → **Read and write permissions**
- **If `main` is protected**:
  - Either allow GitHub Actions to push/merge via your branch rules, or
  - Allow Actions to create PRs: Settings → Actions → General → **Allow GitHub Actions to create and approve pull requests**
