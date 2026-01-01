This repo contains my CV and cover letter, generated with **RenderCV**.

- **Source of truth**: `cv/cv.yaml` and `cl/cl.yaml`
- **Automation**: When a PR is **opened** against `main/master`, GitHub Actions renders PDFs for both the **base (old)** and **PR head (new)** commits, uploads them as workflow artifacts, and comments the PR with links
- **Outputs**: `cv/JamesWong_CV.pdf`, `cl/Cover letter.pdf`
