This repo contains my CV and cover letter, generated with **RenderCV**.

- **Source of truth**: `cv/cv.yaml` and `cl/cl.yaml`
- **Automation**:
  - **PR opened**: renders **old (base)** vs **new (PR head)** PDFs, uploads both as artifacts, and comments the PR with links
  - **PR merged**: re-renders PDFs on the base branch and commits updated PDFs back to the repo
- **Outputs**: `cv/JamesWong_CV.pdf`, `cl/Cover letter.pdf`
