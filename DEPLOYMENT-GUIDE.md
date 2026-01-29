# Quick Deployment Guide for Udyam Website

## Prerequisites
- GitHub account
- Git installed on your computer
- Your Udyam installer files ready (.exe and .dmg)

## Step-by-Step Deployment

### 1. Prepare Your Files

Create the downloads folder and add your installer files:
```bash
cd /Users/dgurjar/workspace/personal/UdyamOnWeb
mkdir downloads
# Copy your Udyam-Setup.exe and Udyam.dmg files to the downloads folder
```

### 2. Update Contact Information

Edit `contact.html` and replace:
- All email addresses (sales@udyam.app, support@udyam.app, etc.)
- Phone numbers (+91-XXXXX-XXXXX)
- Office address ([Your Address], [City, State - PIN])

### 3. Update Links

In `contact.html`, update:
- GitHub URL: Replace `yourusername` with your actual GitHub username
- Social media links (if you have them)

### 4. Initialize Git and Push to GitHub

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Udyam website"

# Create GitHub repository at https://github.com/new
# Name it: UdyamOnWeb
# Make it PUBLIC (required for free GitHub Pages)

# Add remote and push (replace 'yourusername' with your GitHub username)
git remote add origin https://github.com/yourusername/UdyamOnWeb.git
git branch -M main
git push -u origin main
```

### 5. Enable GitHub Pages

1. Go to your repository: `https://github.com/yourusername/UdyamOnWeb`
2. Click **Settings** (top menu)
3. Click **Pages** (left sidebar)
4. Under "Build and deployment":
   - Source: **Deploy from a branch**
   - Branch: **main** and **/ (root)**
5. Click **Save**

### 6. Wait and Access Your Site

- GitHub Pages takes 2-10 minutes to build and deploy
- Your site will be live at: `https://yourusername.github.io/UdyamOnWeb/`
- GitHub will show a green checkmark when deployment is complete

## Updating Your Site

After making changes to any file:

```bash
git add .
git commit -m "Description of your changes"
git push
```

GitHub Pages will automatically rebuild your site within a few minutes.

## Important Notes

### File Size Limits
- GitHub has a 100MB file size limit per file
- If your installers are larger, use **GitHub Releases** instead:
  1. Go to Releases → Create new release
  2. Upload your .exe and .dmg files there
  3. Update the download links in `index.html` to point to the release URLs

### Custom Domain (Optional)
To use your own domain (e.g., udyam.app):
1. Buy domain from any registrar
2. Add a `CNAME` file to your repository with your domain name
3. Configure DNS settings at your domain registrar
4. Enable custom domain in GitHub Pages settings

### HTTPS
- GitHub Pages automatically provides HTTPS
- Your site will be secure by default

## Testing Locally

Before deploying, test your site locally:

1. Open `index.html` in your web browser
2. Check all links work
3. Test navigation between pages
4. Verify responsive design (resize browser window)

## Troubleshooting

### Site not appearing?
- Wait 10 minutes and refresh
- Check GitHub Pages settings are correct
- Ensure repository is public

### Download links not working?
- Verify files are in the `downloads/` folder
- Check file names match exactly (case-sensitive)
- Commit and push the downloads folder

### Changes not showing up?
- Wait a few minutes for GitHub to rebuild
- Clear your browser cache (Ctrl+F5 or Cmd+Shift+R)
- Check if commit was pushed successfully

## Support

If you encounter issues:
1. Check the main README.md for detailed documentation
2. Review GitHub Pages documentation: https://docs.github.com/en/pages
3. Check GitHub Actions tab for build errors

## Quick Checklist

- [ ] Downloads folder created with installer files
- [ ] Contact information updated in contact.html
- [ ] GitHub username updated in all relevant links
- [ ] Office address updated
- [ ] Repository created on GitHub (PUBLIC)
- [ ] Code pushed to GitHub
- [ ] GitHub Pages enabled in settings
- [ ] Site is live and accessible

---

**Congratulations! Your Udyam website is now live! 🎉**
