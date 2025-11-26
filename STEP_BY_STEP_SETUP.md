# Step-by-Step Setup Guide

## STEP 1: Add Your Project to GitHub Desktop

1. **Open GitHub Desktop** (make sure it's installed and you're signed in)

2. **Click "File"** in the top menu → **"Add Local Repository"**

3. **Click "Choose..."** button

4. **Navigate to your project folder:**
   ```
   C:\Users\josewang\OneDrive\Desktop\joseph_website_full
   ```

5. **Select the folder** and click "Select Folder" or "OK"

6. **Click "Add repository"** button

7. You should now see all your files listed in GitHub Desktop!

---

## STEP 2: Create Your First Commit

1. **In GitHub Desktop**, you'll see all your files listed on the left side under "Changes"

2. **At the bottom left**, you'll see a text box that says "Summary (required)"

3. **Type this message:**
   ```
   Initial commit: Personal website with analytical UI
   ```

4. **Click the "Commit to main"** button (bottom left)

5. ✅ Your files are now committed locally!

---

## STEP 3: Create GitHub Repository and Push

1. **After committing**, you'll see a button at the top that says **"Publish repository"** - Click it!

2. **A dialog box will open** with these options:
   - **Name:** Type `joseph-website` (or any name you like)
   - **Description:** Type `Personal portfolio website`
   - **Keep this code private:** 
     - ✅ Check this if you want it private
     - ❌ Uncheck this if you want it public (recommended for portfolio)

3. **Click "Publish Repository"** button

4. **Wait a few seconds** - GitHub Desktop will push your code to GitHub

5. ✅ **Done!** Your code is now on GitHub!

6. **Verify:** You can click "View on GitHub" button to see your repository online

---

## STEP 4: Connect to Cloudflare Pages

1. **Go to Cloudflare Dashboard:**
   - Open your browser
   - Go to: https://dash.cloudflare.com
   - Sign in to your account

2. **Navigate to Pages:**
   - In the left sidebar, click **"Workers & Pages"**
   - You should see your existing project (or create a new one)

3. **Open Your Project:**
   - Click on your project name

4. **Go to Settings:**
   - Click the **"Settings"** tab at the top

5. **Connect to Git:**
   - Scroll down to find **"Builds & deployments"** section
   - Look for **"Connect to Git"** button or **"Configure build"** link
   - Click it

6. **Authorize Cloudflare:**
   - If prompted, click **"Connect to Git"** or **"Authorize Cloudflare"**
   - You'll be redirected to GitHub to authorize
   - Click **"Authorize Cloudflare"** on GitHub
   - You may need to enter your GitHub password or use 2FA

7. **Select Your Repository:**
   - After authorization, you'll see a list of your repositories
   - Find and click on **"joseph-website"** (or whatever you named it)

8. **Configure Build Settings:**
   - **Framework preset:** Select **"None"** from the dropdown
   - **Build command:** Leave this **EMPTY** (don't type anything)
   - **Build output directory:** Type `/` (just a forward slash - this means root directory)

9. **Save and Deploy:**
   - Click **"Save and Deploy"** button
   - Cloudflare will start building your site

10. **Wait for Deployment:**
    - You'll see a progress indicator
    - Usually takes 1-2 minutes
    - When it says "Success" or shows a green checkmark, you're done!

11. **Your Site is Live!**
    - Click on your project name
    - You'll see a URL like: `your-project-name.pages.dev`
    - Click it to see your live website!

---

## STEP 5: Future Updates (How to Update Your Site)

Whenever you make changes to your website:

1. **Make your changes** (edit HTML, CSS, etc. in your code editor)

2. **Open GitHub Desktop**

3. **You'll see your changed files** listed under "Changes"

4. **Type a commit message** (e.g., "Updated project descriptions")

5. **Click "Commit to main"**

6. **Click "Push origin"** button (top right, looks like an up arrow)

7. **Cloudflare automatically deploys!** 
   - Wait 1-2 minutes
   - Your site will update automatically!

---

## Troubleshooting

**Problem: "Publish repository" button not showing**
- Make sure you've committed your files first (Step 2)
- The button appears after you make your first commit

**Problem: Can't find repository in Cloudflare**
- Make sure you authorized Cloudflare to access GitHub
- Try disconnecting and reconnecting
- Check that the repository name matches exactly

**Problem: Build fails in Cloudflare**
- Make sure "Build command" is EMPTY
- Make sure "Build output directory" is just `/`
- Check that all your HTML files are in the root directory

**Problem: Site looks broken**
- Check the Cloudflare build logs for errors
- Make sure all file paths are relative (e.g., `href="about.html"` not `href="/about.html"`)
- Verify `index.html` is in the root directory

---

## Quick Checklist

- [ ] Step 1: Added project to GitHub Desktop
- [ ] Step 2: Made first commit
- [ ] Step 3: Published to GitHub
- [ ] Step 4: Connected to Cloudflare Pages
- [ ] Step 5: Site is live!

---

**Need help?** Let me know which step you're on and I'll help you through it!

