# Publish your GitHub Profile README

Your custom profile files are configured for **[vedantDube](https://github.com/vedantDube)**.

---

## 🚀 1. Push to your `vedantDube` repository

Since you already have a repository named `vedantDube` on GitHub with commit history, follow these quick steps in PowerShell or your terminal from this folder:

```sh
# Initialize git if not already initialized
git init -b main

# Add your GitHub remote repository
git remote add origin https://github.com/vedantDube/vedantDube.git

# Pull existing history to avoid conflicts
git pull origin main --rebase

# Stage all files (README, workflow, banner, and assets)
git add .

# Commit your upgraded profile
git commit -m "Upgrade GitHub profile: 3D contribution calendar, contribution snake, and interactive showcase"

# Push to your main branch
git push -u origin main
```

> **Note:** If prompted for authentication, use your GitHub Credential Manager or Personal Access Token (PAT).

---

## ⚙️ 2. Configure GitHub Actions Workflow Permissions

The automated visuals (3D calendar and snake animation) need write permissions to push generated graphics to your repository:

1. Open your repository on GitHub: **`https://github.com/vedantDube/vedantDube`**
2. Click **Settings** (tab at the top)
3. In the left sidebar, click **Actions** → **General**
4. Scroll down to **Workflow permissions**:
   - Select **Read and write permissions**
   - Check **Allow GitHub Actions to create and approve pull requests**
5. Click **Save**

---

## 🎨 3. Generate Contribution Visuals

1. On GitHub, navigate to the **Actions** tab of your `vedantDube` repo.
2. Under "Workflows", select **Generate contribution visuals**.
3. Click the **Run workflow** dropdown button, select branch `main`, and click **Run workflow**.
4. The workflow runs two parallel jobs:
   - **`three-dimensional-calendar`**: Generates and commits 3D contribution calendar SVGs into the `profile-3d-contrib/` folder on branch `main`.
   - **`contribution-snake`**: Generates the animated snake game eating your contribution squares and publishes it to the `output` branch.
5. Once completed (typically 1–2 minutes), refresh `https://github.com/vedantDube` to see your 3D calendar and animated snake live!

---

## 🔄 Automatic Daily Updates

The `.github/workflows/contribution-art.yml` workflow is scheduled to run automatically daily at 02:23 UTC (07:53 IST) and whenever you push updates to `README.md`. Your 3D calendar and snake will stay updated with your contributions continuously!

---

## 🖼️ Personal Photo / Banner

- **Banner**: Currently using `banner.png` (a futuristic high-tech developer hero banner).
- **Photo**: If you prefer to display your personal portrait instead, drop your photo into the folder as `profile.png` (or `profile.jpg`), adjust the `<img src="./banner.png" ...>` in `README.md` to point to `./profile.png`, commit, and push.
