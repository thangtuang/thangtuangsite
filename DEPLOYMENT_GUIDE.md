# Deployment Guide - GitHub Pages

Follow these steps to deploy your website to GitHub Pages for free hosting.

## Prerequisites

- A GitHub account (create one at https://github.com if you don't have one)
- Your website files ready to upload

## Step-by-Step Deployment

### 1. Create a New Repository

1. Go to https://github.com
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., `personal-website` or `thang-tuang`)
5. Choose "Public" (required for free GitHub Pages)
6. **Do NOT** initialize with README, .gitignore, or license (we already have these)
7. Click "Create repository"

### 2. Upload Your Files

**Option A: Using GitHub Web Interface (Easiest)**
1. On your new repository page, click "uploading an existing file"
2. Drag and drop ALL files from this folder:
   - `index.html`
   - `README.md`
   - `.gitignore`
3. Scroll down and click "Commit changes"

**Option B: Using Git Command Line**
```bash
cd path/to/thang-tuang-website
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" (gear icon)
3. In the left sidebar, click "Pages"
4. Under "Source", select "Deploy from a branch"
5. Under "Branch", select "main" and "/ (root)"
6. Click "Save"

### 4. Access Your Website

1. Wait 1-2 minutes for GitHub to build your site
2. Your site will be available at:
   - `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`
3. The URL will be shown in the Pages settings

## Custom Domain (Optional)

If you want to use your own domain name:

1. Buy a domain from providers like Namecheap, GoDaddy, or Google Domains
2. In your repository Settings → Pages, add your custom domain
3. In your domain provider's DNS settings, add these records:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   Value: 185.199.109.153
   Value: 185.199.110.153
   Value: 185.199.111.153
   
   Type: CNAME
   Name: www
   Value: YOUR-USERNAME.github.io
   ```
4. Wait for DNS propagation (can take up to 24 hours)

## Updating Your Website

Whenever you want to update your website:

1. Edit your `index.html` file
2. Upload the updated file to GitHub (or commit and push via Git)
3. Changes will appear on your live site within a few minutes

## Troubleshooting

**Site not loading?**
- Wait a few more minutes (initial deployment can take 5-10 minutes)
- Check that your repository is public
- Verify the branch is set to "main" in Pages settings

**Changes not showing?**
- Clear your browser cache (Ctrl+F5 or Cmd+Shift+R)
- Wait a few minutes for GitHub to rebuild

## Need Help?

- GitHub Pages Documentation: https://docs.github.com/en/pages
- GitHub Support: https://support.github.com

---

**Your website will be live and accessible to anyone on the internet for free! 🎉**
