# Aakanksha Ghare — DevOps-Focused Portfolio

A static portfolio website built with plain HTML, CSS and JavaScript. No build step, no Node.js, no backend.

## Project structure

```text
devops-portfolio/
├── index.html
├── style.css
├── script.js
├── README.md
└── assets/
    ├── certificates/
    │   ├── docker-kubernetes.jpg
    │   ├── python-essentials-1.jpg
    │   ├── endpoint-security.jpg
    │   └── 30-day-programming-challenge.jpg
    └── resume/
        └── Aakanksha_Ghare_Resume.pdf   <- placeholder, replace with your resume
```

## Run locally

Option 1: double-click `index.html` to open it in your browser.

Option 2 (closer to how S3 serves it):

```bash
cd devops-portfolio
python3 -m http.server 8000
# open http://localhost:8000
```

## Remaining placeholders

Search for `REPLACE` in `index.html`.

| What | Where | Replace with |
|------|-------|--------------|
| NetSecureAI repo | Project card button (`href="#projects"`) | Your repository URL |
| RAG Enterprise Assistant repo | Project card button | Your repository URL |
| PaySwift repo | Project card button | Your repository URL |

Already set: resume (`assets/resume/Aakanksha_Ghare_Resume.pdf`), LinkedIn, email, GitHub profile and the WinHunt repo.
To update the resume later, replace the PDF and keep the same filename.

Note: the resume PDF contains your phone number, and the site is public once deployed. Remove it from the PDF if you don't want it shared.

## Animations

Scroll progress bar, scroll-reveal, hero entrance, drifting hero background, card spotlight, timeline drawing and the deployment-flow animation. All of them switch off for visitors who have "reduce motion" enabled.

## Deploying later (workshop plan)

Everything uses relative paths, so the whole folder can be uploaded to an S3 static website bucket as it is.
The intended flow is: Git repository -> GitHub -> GitHub Actions -> S3 bucket -> public website.
Set `index.html` as the index document in the S3 static website settings.
