# Setting this up as a demo / template repo

You are setting this up so your son can copy it as his own independent
repo, with no fork link back to yours. Here is the exact path.

## 1. Create the repo

On GitHub, create a new repository named `playtest-reports` (or whatever
name you like). Make it **public**. Do not initialize it with a README,
since you already have one in this folder.

## 2. Push these files

From inside this folder:

```
git init
git add .
git commit -m "Initial playtest reports setup"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/playtest-reports.git
git push -u origin main
```

## 3. Mark it as a template repository

This is the step that matters most. On the repo page:

1. Click **Settings** (top right of the repo, not your account settings)
2. On the General tab, near the top, check the box labeled
   **Template repository**
3. That is it, no save button needed, it applies immediately

## 4. Send him the link

Once it is a template repo, anyone visiting it sees a green
**Use this template** button instead of just a fork option. He clicks it,
picks **Create a new repository**, names his own copy, and gets a fresh
repo with these same files, full commit history of his own starting at
commit one, and zero link back to your repo.

## 5. After he creates his copy

He still needs to add the labels from LABELS.md to his new repo, since
labels do not carry over through the template process. Either by hand
or with the `gh label create` commands listed there.

## Why not just have him fork it instead

Forking is meant for contributing back to the same project, and GitHub
shows "forked from [your username]/playtest-reports" permanently on a
forked repo. Since this is meant to be his own independent body of work,
a template copy reads as fully his, with no asterisk.
