# Push this repository to GitHub

This assumes Git is installed on Windows and you are using PowerShell or Git Bash.

## 1. Create an empty GitHub repository

On GitHub, create a new repository named:

`patient-level-biomedical-ml`

Do not add a README, .gitignore, or license during GitHub creation. This folder already contains them.

## 2. Open a terminal in this folder

```bash
cd path/to/patient-level-biomedical-ml
```

## 3. Check the files

```bash
git status
```

You should see the README, research files, folders, notebook and supporting files.

## 4. Initialize Git

```bash
git init
git branch -M main
```

## 5. Make the first commit

```bash
git add .
git commit -m "Initialize biomedical ML study repository"
```

## 6. Connect the GitHub repository

Replace `<YOUR_GITHUB_USERNAME>` with your username:

```bash
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/patient-level-biomedical-ml.git
```

Check it:

```bash
git remote -v
```

## 7. Push

```bash
git push -u origin main
```

### Important

Git does not track truly empty directories. This scaffold therefore uses `.gitkeep` files in directories that need to exist before they contain real outputs.

Do not commit the raw dataset just because the folder exists. Follow `data/provenance.md` and the root `.gitignore`.
