# <h1>How to Set Up a GitHub Repository and GitHub Actions Workflow</h1>
====================================================================

## 1. Open GitHub Account
Log in to your GitHub account on GitHub.

---

## 2. Create a New Repository
- Go to **New Repository**
- Enter repository name
- Choose visibility (Public or Private)
- Click **Create Repository**

---

## 3. Open Terminal or Visual Studio Code
Open **Visual Studio Code** or any terminal and navigate to the folder where you want to store the project.

---
## 4. Clone the Repository Using SSH
```bash
git clone git@github.com:username/repository-name.git

---

## 5. Navigate to the Repository
cd repository-name
6. Create GitHub Actions Folder

Create the required directory structure:

mkdir -p .github/workflows
7. Create a Workflow File

Create a workflow file:

touch .github/workflows/main.yml

Open the file and add your workflow configuration based on your project requirements.

Example:

name: CI Pipeline

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Run a script
        run: echo "Hello GitHub Actions!"
8. Stage Changes
git add .
9. Commit Changes
git commit -m "commit_name"
10. Push Changes to GitHub
git push origin main
11. Verify GitHub Actions

Go to your repository in GitHub → Click on the Actions tab → Check your workflow run.