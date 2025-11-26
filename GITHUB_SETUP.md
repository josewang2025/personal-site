# GitHub Integration Setup Guide

## Step 1: Install Git

### Download and Install:
1. Go to: https://git-scm.com/download/win
2. Download the latest version for Windows
3. Run the installer with **default settings** (just click Next)
4. Restart your terminal/PowerShell after installation

### Verify Installation:
Open a new PowerShell window and run:
```powershell
git --version
```
You should see something like: `git version 2.x.x`

---

## Step 2: Configure Git (First Time Only)

Run these commands in PowerShell (replace with your info):
```powershell
git config --global user.name "Your Name"
git config --global user.email "joseph@josephjwang.com"
```

---

## Step 3: Initialize Repository

In your project folder, run:
```powershell
# Navigate to your project (if not already there)
cd "C:\Users\josewang\OneDrive\Desktop\joseph_website_full"

# Initialize git
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: Personal website"
```

---

## Step 4: Create GitHub Repository

1. Go to: https://github.com/new
2. Repository name: `joseph-website` (or any name you prefer)
3. Description: "Personal portfolio website"
4. Make it **Public** (or Private if you prefer)
5. **DO NOT** check "Initialize with README" (we already have files)
6. Click "Create repository"

---

## Step 5: Connect and Push to GitHub

After creating the repo, GitHub will show you commands. Use these:

```powershell
# Add your GitHub repository (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/joseph-website.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

**Note:** GitHub will ask for your username and password. Use a **Personal Access Token** instead of password:
- Go to: https://github.com/settings/tokens
- Generate new token (classic)
- Select scope: `repo` (full control)
- Copy the token and use it as password when pushing

---

## Step 6: Connect to Cloudflare Pages

1. Go to: https://dash.cloudflare.com
2. Navigate to **Workers & Pages** → Your project
3. Click **"Create deployment"** or go to **Settings**
4. Click **"Connect to Git"** or **"Configure build"**
5. Click **"Connect to Git"** button
6. Authorize Cloudflare to access your GitHub account
7. Select your repository: `joseph-website`
8. Configure build settings:
   - **Framework preset**: None
   - **Build command**: (leave empty)
   - **Build output directory**: `/` (root)
9. Click **"Save and Deploy"**

---

## Step 7: Future Updates

Now whenever you make changes:

```powershell
# Add changed files
git add .

# Commit changes
git commit -m "Description of changes"

# Push to GitHub (triggers automatic Cloudflare deployment)
git push
```

Cloudflare will automatically detect the push and redeploy your site in 1-2 minutes!

---

## Troubleshooting

**Issue: Git not found after installation**
- Close and reopen PowerShell
- Or restart your computer

**Issue: Authentication failed**
- Use Personal Access Token instead of password
- Make sure token has `repo` scope

**Issue: Repository already exists**
- If you already have a repo, you can delete it and recreate, OR
- Use `git remote set-url origin https://github.com/YOUR_USERNAME/joseph-website.git`

---

## Alternative: GitHub Desktop (GUI Option)

If you prefer a visual interface:
1. Download: https://desktop.github.com/
2. Sign in with GitHub
3. File → Add Local Repository → Select your folder
4. Commit and push using the GUI

