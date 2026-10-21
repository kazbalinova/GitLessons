# Git Lessons

A small static website and practice repository for learning Git and GitHub. The site is plain HTML and CSS, so it works without a build step or dependencies.

## Preview locally

Open `index.html` in a browser. For a local server, run one of these commands from this folder:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Everyday Git workflow

```bash
git status
git add .
git commit -m "Describe the change"
git push
```

Use `git status` before and after a change. It shows which branch is checked out and which files are modified, staged, or untracked.

## Course

This project follows the [Git and GitHub for beginners video course](https://www.youtube.com/playlist?list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT). See [LESSONS.md](LESSONS.md) for the lesson 13–25 practice guide, commands, and GitHub steps.

## Project files

- `index.html` — the responsive course landing page.
- `styles.css` — its layout, colors, and mobile styles.
- `.gitignore` — local files and generated output Git should skip.
- `LESSONS.md` — a practical checklist for the remaining course topics.

## Publish with GitHub Pages

The site is static and can be hosted by GitHub Pages. In the repository on GitHub, open **Settings → Pages**, choose the `main` branch and `/ (root)` as the publishing source, then save. GitHub will show the published address in the Pages settings when the build is ready.

## License

Course practice project. Adapt it as you learn.
