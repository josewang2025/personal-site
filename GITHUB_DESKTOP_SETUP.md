# GitHub Desktop Setup - Step by Step

## Step 1: Add Your Project to GitHub Desktop

1. **Open GitHub Desktop**
2. **File** → **Add Local Repository**
3. Click **"Choose..."** and navigate to:
   ```
   C:\Users\josewang\OneDrive\Desktop\joseph_website_full
   ```
4. Click **"Add repository"**

---

## Step 2: Create Initial Commit

1. You'll see all your files listed as changes
2. At the bottom left, type a commit message:
   ```
   Initial commit: Personal website
   ```
3. Click **"Commit to main"** (or "Commit to master")

---

## Step 3: Create GitHub Repository and Push

1. Click **"Publish repository"** button (top right)
2. A dialog will open:
   - **Name**: `joseph-website` (or any name you prefer)
   - **Description**: "Personal portfolio website"
   - **Keep this code private**: Uncheck (make it public) OR check if you want private
3. Click **"Publish Repository"**
4. GitHub Desktop will push your code to GitHub

---

## Step 4: Verify on GitHub

1. Go to: https://github.com/josewang2025
2. You should see your new repository: `joseph-website`
3. Click on it to verify all files are there

---

## Step 5: Connect to Cloudflare Pages

1. Go to: https://dash.cloudflare.com
2. Navigate to **Workers & Pages**
3. Click on your existing project (or create new one)
4. Go to **Settings** tab
5. Scroll down to **Builds & deployments**
6. Click **"Connect to Git"** or **"Configure build"**
7. Click **"Connect to Git"** button
8. Authorize Cloudflare to access your GitHub account
9. Select your repository: `joseph-website`
10. Configure build settings:
    - **Framework preset**: None
    - **Build command**: (leave empty - no build needed)
    - **Build output directory**: `/` (root directory)
11. Click **"Save and Deploy"**

---

## Step 6: Future Updates

Now whenever you make changes to your website:

1. **Make your changes** (edit HTML, CSS, etc.)
2. **Open GitHub Desktop**
3. You'll see your changes listed
4. **Type a commit message** (e.g., "Update Yelp project description")
5. Click **"Commit to main"**
6. Click **"Push origin"** (top right)
7. **Cloudflare will automatically deploy** your changes in 1-2 minutes!

---

## Troubleshooting

**Issue: "Publish repository" button not showing**
- Make sure you've committed your files first
- The button appears after the initial commit

**Issue: Can't find repository in Cloudflare**
- Make sure you authorized Cloudflare to access GitHub
- Check that the repository name matches exactly

**Issue: Build fails in Cloudflare**
- Make sure build command is empty
- Build output directory should be `/` (root)

---

That's it! Your site will now automatically update whenever you push changes to GitHub.

