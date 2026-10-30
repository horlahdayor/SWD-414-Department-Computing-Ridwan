# Git and GitHub practical steps

Run these commands from a terminal in the project folder. Replace `YOUR-USERNAME` with your GitHub username and create an empty GitHub repository named `swd414-computing-website` first.

## 1. Initialise and record the initial website
```bash
git init
git status
git add .
git commit -m "Create initial Department of Computing website"
```

## 2. Record a homepage improvement
Make a small change to `index.html` or `styles.css`, save it, then run:
```bash
git status
git add index.html styles.css
git commit -m "Improve homepage content and design"
git log --oneline
```

## 3. Create a branch for Contact Us
```bash
git switch -c feature/contact-us
```
Edit `contact.html` (for example, personalise the contact details), then:
```bash
git add contact.html
git commit -m "Build Contact Us page"
git switch main
git merge feature/contact-us
git log --oneline --graph --all
```
If your default branch is named `master`, use `master` instead of `main`, or rename it with `git branch -M main`.

## 4. Connect to GitHub and push
```bash
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/swd414-computing-website.git
git push -u origin main
git push -u origin feature/contact-us
```
If `origin` already exists, check it with `git remote -v` instead of adding it again.

## 5. Make a later update and push it
Edit a page, then:
```bash
git status
git add .
git commit -m "Update website after GitHub upload"
git push
```

## Key explanation
- **Commit:** saves a snapshot of staged changes in the local Git repository.
- **Push:** transfers local commits to a remote repository such as GitHub so they are available online.

## Evidence screenshots to capture yourself
1. The website homepage in a browser.
2. The About Us, Programmes, and Contact Us pages.
3. Terminal showing `git log --oneline --graph --all` with at least three commits and the feature branch/merge.
4. GitHub repository page showing the uploaded files and commit history.
5. Optional: terminal showing `git status` and successful `git push`.

Do not claim a push or screenshot is complete until you have actually done it.
