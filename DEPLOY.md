# Quick Deployment Guide to GitHub Pages

Follow these steps to deploy your Physio Counter PWA to GitHub Pages:

## Prerequisites

- Git installed on your computer
- A GitHub account

## Step-by-Step Instructions

### 1. Initialize Git Repository

Open Terminal and navigate to your counter directory:

```bash
cd /Users/kanantharamu/Desktop/counter
```

Initialize git (if not already done):

```bash
git init
```

### 2. Stage All Files

Add all files to git:

```bash
git add .
```

### 3. Create Initial Commit

```bash
git commit -m "Initial commit: Physio Counter PWA v4.6.1"
```

### 4. Create GitHub Repository

1. Go to https://github.com
2. Click the "+" icon in the top right
3. Select "New repository"
4. Choose a repository name (e.g., `physio-counter`)
5. Keep it public (required for free GitHub Pages)
6. **Do NOT** initialize with README, .gitignore, or license (we already have these)
7. Click "Create repository"

### 5. Connect Local Repository to GitHub

Copy the commands from GitHub's "push an existing repository" section, or use:

```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
```

**Replace:**
- `YOUR_USERNAME` with your GitHub username
- `YOUR_REPO_NAME` with your repository name

### 6. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click the "Settings" tab
3. In the left sidebar, click "Pages"
4. Under "Source", select "Deploy from a branch"
5. Under "Branch", select "main" and "/ (root)"
6. Click "Save"

### 7. Wait for Deployment

- GitHub will build your site (usually takes 1-3 minutes)
- You'll see a message: "Your site is live at https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/"
- Click the link to visit your deployed app!

### 8. Test the PWA

1. Visit your deployed URL
2. You should see an "Install" button in the browser
3. Click install to add it to your home screen
4. Test offline functionality by turning off WiFi

## Updating Your App

Whenever you make changes:

```bash
git add .
git commit -m "Description of your changes"
git push
```

GitHub Pages will automatically redeploy (takes 1-3 minutes).

## Troubleshooting

### Issue: Pages not showing up
- Wait a few minutes and refresh
- Check the "Actions" tab in your repo to see build status
- Ensure the repository is public

### Issue: Install button not appearing
- Make sure you're accessing via HTTPS (GitHub Pages uses HTTPS by default)
- Check browser console for errors
- Try a different browser (Chrome/Edge work best)

### Issue: Service worker not registering
- Check that all files (manifest.json, sw.js, icons) are present
- Clear browser cache and reload
- Check browser console for specific errors

## Custom Domain (Optional)

To use your own domain:

1. Add a file named `CNAME` (no extension) with your domain:
   ```bash
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

2. Configure DNS with your domain provider:
   - Add a CNAME record pointing to `YOUR_USERNAME.github.io`
   - Or add A records pointing to GitHub's IPs

3. In GitHub Settings → Pages, enter your custom domain

## Success!

Your PWA is now live and installable! Share the URL with anyone who needs a physio counter app.

**Your app URL will be:**
`https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

---

Need help? Check GitHub Pages documentation: https://docs.github.com/en/pages

