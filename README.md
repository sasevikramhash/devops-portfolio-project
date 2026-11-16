# DevOps Portfolio – HTML & CSS Starter

A beginner-friendly responsive portfolio website built with plain HTML and CSS. Use it to practise Git, GitHub and Jenkins CI/CD.

## Project files

```text
devops-portfolio-project/
├── index.html
├── style.css
├── Jenkinsfile
├── README.md
└── .gitignore
```

## Run locally

No build tools are required.

1. Open the project folder.
2. Double-click `index.html`, or use VS Code Live Server.
3. Edit `index.html` and `style.css`, save, and refresh your browser.

## Personalize it

- Replace `Alex Morgan` and `AM` with your own details.
- Update the About section and skills.
- Add links to your GitHub projects.
- Change the contact email from `hello@example.com`.

## Push to GitHub

Create an empty repository on GitHub, then run these commands from this folder:

```bash
git init
git add .
git commit -m "Add responsive portfolio website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Replace the URL with your own GitHub repository URL.

## Jenkins practice

The included `Jenkinsfile` checks that the HTML and CSS files exist, validates a few expected HTML elements, and creates a `dist/` folder containing the website files.

In Jenkins, create a Pipeline job and choose **Pipeline script from SCM**:
- SCM: Git
- Repository URL: your GitHub repository URL
- Branch: `*/main`
- Script Path: `Jenkinsfile`

Then save and run **Build Now**.

This starter pipeline validates and packages the static site; it does not deploy it to a server yet.
