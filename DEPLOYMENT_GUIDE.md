# Cloudflare Pages Deployment Guide

## Option 1: Direct Upload (Easiest - No Git Required)

1. **Prepare your files**: Make sure all your website files are ready
   - index.html
   - about.html
   - contact.html
   - projects.html
   - resume.html
   - services.html
   - style.css
   - joseph-hero.png

2. **Go to Cloudflare Dashboard**:
   - Visit: https://dash.cloudflare.com
   - Sign in or create a free account

3. **Create a Pages Project**:
   - Click on "Workers & Pages" in the left sidebar
   - Click "Create application"
   - Select "Pages" tab
   - Click "Upload assets"

4. **Upload your files**:
   - Drag and drop all your website files OR
   - Click "Select files" and choose all files
   - Make sure `index.html` is in the root
   - Click "Deploy site"

5. **Your site will be live!**
   - Cloudflare will give you a URL like: `your-project-name.pages.dev`
   - You can customize the project name during setup

6. **Add Custom Domain (Optional)**:
   - In your Pages project, go to "Custom domains"
   - Add your domain (e.g., josephjwang.com)
   - Follow DNS setup instructions

---

## Option 2: GitHub Integration (Recommended for Updates)

### Step 1: Install Git (if not installed)
- Download from: https://git-scm.com/download/win
- Install with default settings

### Step 2: Create GitHub Repository
1. Go to: https://github.com/new
2. Create a new repository (e.g., `joseph-website`)
3. Don't initialize with README (we'll push existing files)

### Step 3: Initialize Git and Push
Open PowerShell in your project folder and run:

```powershell
# Initialize git
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: Personal website"

# Add your GitHub repository (replace YOUR_USERNAME and REPO_NAME)
git remote add origin https://github.com/YOUR_USERNAME/joseph-website.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 4: Connect to Cloudflare Pages
1. Go to Cloudflare Dashboard → Workers & Pages
2. Click "Create application" → "Pages" tab
3. Click "Connect to Git"
4. Authorize Cloudflare to access your GitHub
5. Select your repository (`joseph-website`)
6. Configure build settings:
   - **Framework preset**: None (or Static)
   - **Build command**: (leave empty - no build needed)
   - **Build output directory**: `/` (root)
7. Click "Save and Deploy"

### Step 5: Automatic Deployments
- Every time you push to GitHub, Cloudflare will automatically redeploy
- You can also trigger manual deployments from the dashboard

---

## Quick Tips

- **Free tier includes**: Unlimited requests, 500 builds/month, custom domains
- **Build time**: Usually 1-2 minutes
- **HTTPS**: Automatically enabled
- **CDN**: Global CDN included for fast loading

---

## Troubleshooting

**Issue**: Files not loading correctly
- Make sure all file paths are relative (e.g., `href="about.html"` not `href="/about.html"`)
- Check that `index.html` is in the root directory

**Issue**: Images not showing
- Verify image file names match exactly (case-sensitive)
- Check file paths in HTML

**Issue**: CSS not applying
- Ensure `style.css` is in the same directory as HTML files
- Check that `<link rel="stylesheet" href="style.css" />` is correct

---

## Need Help?
If you run into issues, check Cloudflare's documentation:
https://developers.cloudflare.com/pages/


