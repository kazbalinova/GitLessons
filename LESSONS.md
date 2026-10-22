# Lessons 13–25: practice guide

The playlist has 25 lessons. The local repository already contains its initial Git/GitHub practice; this guide picks up at lesson 13 and ties the remaining topics to this project. Video 11 covers Git Graph, and video 12 covers aliases. Use the video chapters as the source for the instructor's exact demo; the notes here are a safe practice path for this repository.

## 13. Undo changes in code

See the [lesson](https://www.youtube.com/watch?v=BSHxwpBv-WQ&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=13). First inspect `git status` and `git diff`. To discard an unstaged edit to one file, use `git restore -- path/to/file`. To unstage a file while keeping its edits, use `git restore --staged -- path/to/file`. These commands can discard work, so inspect the path and diff first. For a change already committed, prefer a new undo commit with `git revert <commit>`.

## 14–16. Branches and merging

Watch [part 1](https://www.youtube.com/watch?v=PEwtswYFvLo&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=14), [part 2](https://www.youtube.com/watch?v=gCuHWIDQMSo&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=15), and [part 3: merging](https://www.youtube.com/watch?v=hDcsxin9ZEM&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=16).

```bash
git switch -c practice/roadmap
# Make a small edit, then save it on this branch.
git add index.html
git commit -m "Improve the course roadmap"
git switch main
git merge practice/roadmap
git branch -d practice/roadmap
```

If Git reports a conflict, open the named file, choose the intended final content, remove conflict markers, then stage and commit the resolution.

## 17–18. README and Markdown

Watch [README basics](https://www.youtube.com/watch?v=8lEDTrr-G4U&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=17) and [Markdown syntax](https://www.youtube.com/watch?v=jCjuXf4WPrQ&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=18). This repository's `README.md` demonstrates headings, links, lists, inline code, fenced code blocks, and a project file list. Try adding a screenshot or a short setup note.

## 19. Editor settings sync

Watch [the short lesson](https://www.youtube.com/watch?v=4HgXlmH1yOg&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=19). In VS Code, turn on **Settings Sync** from the Accounts or Manage menu to keep editor preferences across devices. This is a personal account setting; it does not need to be committed to this project.

## 20. GitHub Gist

Watch [the Gist lesson](https://www.youtube.com/watch?v=y-zATLY24eA&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=20). A Gist is useful for sharing a small standalone snippet. Create one only when you have a snippet to share; choose public or secret visibility deliberately. Do not put credentials or private data in a Gist.

## 21. GitHub Pages

Watch [the Pages lesson](https://www.youtube.com/watch?v=o-iV85RkoHE&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=21). This project is already a plain static site. To publish it, push the project to GitHub, then select **Settings → Pages → Deploy from a branch → `main` → `/ (root)`** and save. The Pages address will appear in the repository settings.

## 22. GitHub profile page

Watch [the profile lesson](https://www.youtube.com/watch?v=w57rX5YDEio&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=22). GitHub profile READMEs live in a separate public repository named exactly like the account's username. They are not part of this `GitLessons` repository; add one only if you want a public profile page.

## 23. Fork and pull request

Watch [the collaboration lesson](https://www.youtube.com/watch?v=hQTARFi9IOY&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=23). To practice, fork a project you are allowed to contribute to, clone your fork, create a topic branch, commit a focused change, push that branch to your fork, and open a pull request from the GitHub interface. A pull request targets another repository, so the target should be chosen by you.

## 24. Ignore local files

Watch [the `.gitignore` lesson](https://www.youtube.com/watch?v=RvthmUPfcvY&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=24). The `.gitignore` in this project skips environment secrets, editor files, OS metadata, dependencies, and generated output. To stop tracking a file that was already committed, remove it from the index with `git rm --cached path/to/file`, then commit the change. Ignoring a file does not erase it from Git history.

## 25. Course recap

Watch the [course recap](https://www.youtube.com/watch?v=2ZWqy2xI1JI&list=PLuY6eeDuleIMtvOvJBAbakwcIdEt7IAXT&index=25). Practice the cycle: inspect, make a focused change, stage, commit, and push. Use branches for experiments and a README to help the next person understand the project.

## Git Graph and aliases (lessons 11–12)

- **Git Graph:** install the Git Graph extension from the official Visual Studio Code Marketplace, then open its graph view to inspect branches and commits.
- **Aliases:** define shortcuts in your own Git config, for example `git config --global alias.st status` and `git config --global alias.lg "log --oneline --graph --decorate --all"`. These modify your personal Git setup, not the repository.
