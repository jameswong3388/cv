This repo contains my CV and cover letter, generated with **RenderCV**.

- **Source of truth**: `cv/cv.yaml` and `cl/cl.yaml`
- **Automation**: On every push to `main`, GitHub Actions runs `rendercv render` to regenerate the PDFs and **commits the updated PDFs back to the repo**
- **Outputs**: `cv/JamesWong_CV.pdf`, `cl/Cover letter.pdf`
