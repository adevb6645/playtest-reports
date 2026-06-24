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

If you would rather not use git, you can also drag the files into the
repo through the GitHub web UI using "Add file" > "Upload files." The one
catch: the upload UI sometimes flattens nested folders, so the issue
template can land outside of `.github/ISSUE_TEMPLATE/` if you are not
careful. If that happens, use "Create new file" and type the full path
`.github/ISSUE_TEMPLATE/bug_report.yml` directly into the filename box,
which makes GitHub create the folders for you.

## 3. Mark it as a template repository

On the repo page:

1. Click **Settings** (top right of the repo, not your account settings)
2. On the General tab, near the top, check the box labeled
   **Template repository**
3. That is it, no save button needed, it applies immediately

## 4. Turn on GitHub Pages for the live dashboard

This is an easy one to forget, since nothing prompts you to do it.
Without this step, `playtest-dashboard.html` only works if someone
downloads it and opens it locally.

1. Still in **Settings**, click **Pages** in the left sidebar
2. Under "Build and deployment," set **Source** to **Deploy from a branch**
3. Set **Branch** to **main**, folder to **/ (root)**, click **Save**
4. Wait a minute or two, then refresh the Pages settings screen. It will
   show a banner with the live URL once the site is built, something like
   `https://YOUR-USERNAME.github.io/playtest-reports/playtest-dashboard.html`

## 5. Send him the link

Once it is a template repo, anyone visiting it sees a green
**Use this template** button instead of just a fork option. He clicks it,
picks **Create a new repository**, names his own copy, and gets a fresh
repo with these same files, full commit history of his own starting at
commit one, and zero link back to your repo.

## 6. After he creates his copy

A few things do not carry over automatically through the template process
and he will need to redo them in his own copy:

- **Labels** - add them from LABELS.md, either by hand or with the
  `gh label create` commands listed there
- **GitHub Pages** - repeat step 4 above in his own repo's Settings if he
  wants the live dashboard reachable at a public URL
- **Manually labeling each issue** - filling out the bug report form does
  not automatically apply matching labels. After filing a report, he
  needs to open the issue and apply game/severity/type/status labels
  himself using the gear icon in the sidebar. This is what makes the
  dashboard's breakdowns work.

## Why not just have him fork it instead

Forking is meant for contributing back to the same project, and GitHub
shows "forked from [your username]/playtest-reports" permanently on a
forked repo. Since this is meant to be his own independent body of work,
a template copy reads as fully his, with no asterisk.
