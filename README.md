<h1 align="center">
📄<br>Semantic Commits Patterns 
  
  Prometeon Tyre Group
</h1>

<h1 align="center">
  <img src="gitcommit.png">
</h1>

<p>
  This repository was created based on the <a href="https://github.com/iuricode">@iuricode</a> user repository and seeks to standardize commits and suggest a workflow to employees using Git and Github tools within the company.
</p>

## ⌨️ Type and Description

The semantic commit has the following structural elements (types), which inform the user of your code of the intent of your commit:

- `feat`: (new feature for the user, not a new feature for build script)
 
- `fix`: (bug fix for the user, not a fix to a build script)

- `docs`: (changes to the documentation)

- `style`: (formatting, missing semi colons, etc; no production code change)

- `refactor`: (refactoring production code, eg. renaming a variable)

- `build`: (modifications to build files and dependencies)

- `test`: (adding missing tests, refactoring tests; no production code change)

- `chore`: (updating grunt tasks etc; no production code change)


## 🧭 Issue Reference

- Apply the suffix `'...: ref issue #00'` to reference the open issue through the commit message, where _00_ is replaced by the issue number

## 🌗 Stage

- `partial` - (used when partial changes are made within the branch used that already carry a relevant amount of change, but have not yet been finalized)

- `final` - (indicate that the issue has been completely resolved and that this is the final version to be merged with the _master_ branch)

## 🪜 Workflow step by step

<p>
  After opening the issue by the project admin, on your desktop follow these commands (example new field in the app):
</p>

- Access the main branch of the repository (usually **master** or **main**) and import the latest data from the remote repository:

```bash
git checkout master
git pull master
```

- Then create a new branch with the type of task to be performed and the name of the task:

```bash
git checkout -b feat/new-field
```

- After completing the task or step, add the edited files to the staging area:

```bash
git add .             # to add all files
git add file.py    # to add a specific file
```

- Perform a save of the edits stored in the staging area via git commit **complying with commit patterns** and using the suffix, then perform a push on the remote repository:

```bash
git commit -m 'feat (new-field): ref issue #93 - final'
git push
```

## 💻 Pull Request

- After performing a push on the remote repository, make a pull request inside Github by selecting the main branch and the branch related to the resolved issue and wait for the project admin's approval.

<br>[⬆ Back to top](#semantic-commits-patterns-) <br>
