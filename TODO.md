# Udyam Website - Setup Checklist

Complete these tasks before deploying your website:

## 📁 File Preparation

- [ ] Create `downloads` folder in this directory
- [ ] Add `Udyam-Setup.exe` to downloads folder
- [ ] Add `Udyam.dmg` to downloads folder
- [ ] (Optional) Add app screenshots to an `images` folder

## ✏️ Content Updates

### Contact Information (contact.html)
- [ ] Replace `sales@udyam.app` with your sales email
- [ ] Replace `support@udyam.app` with your support email  
- [ ] Replace `info@udyam.app` with your general email
- [ ] Replace `bugs@udyam.app` with your bug reports email
- [ ] Replace `feedback@udyam.app` with your feedback email
- [ ] Replace `partnerships@udyam.app` with your partnerships email
- [ ] Replace `+91-XXXXX-XXXXX` with your phone numbers
- [ ] Update `[Your Address]` with actual business address
- [ ] Update `[City, State - PIN]` with actual location

### Links & URLs (contact.html)
- [ ] Update GitHub URL (replace `yourusername`)
- [ ] Update website URL if different
- [ ] Add Twitter link (or remove if not applicable)
- [ ] Add LinkedIn link (or remove if not applicable)

### Optional Customizations
- [ ] Add your company logo (replace text logo in navigation)
- [ ] Change brand colors in `style.css` if desired
- [ ] Add app screenshots in features.html
- [ ] Update testimonials with real customer feedback (if available)
- [ ] Customize "Coming Soon" features if different

## 🚀 Deployment

- [ ] Create GitHub account (if you don't have one)
- [ ] Install Git on your computer
- [ ] Create new repository on GitHub named `UdyamOnWeb`
- [ ] Make repository PUBLIC (required for free GitHub Pages)
- [ ] Initialize git: `git init`
- [ ] Add files: `git add .`
- [ ] Commit: `git commit -m "Initial commit: Udyam website"`
- [ ] Add remote: `git remote add origin https://github.com/yourusername/UdyamOnWeb.git`
- [ ] Push: `git branch -M main && git push -u origin main`

## ⚙️ GitHub Pages Setup

- [ ] Go to repository Settings → Pages
- [ ] Select branch: `main`
- [ ] Select folder: `/ (root)`
- [ ] Click Save
- [ ] Wait 5-10 minutes for site to go live
- [ ] Visit: `https://yourusername.github.io/UdyamOnWeb/`

## ✅ Testing

- [ ] Test download links work
- [ ] Check all navigation works correctly
- [ ] Verify responsive design on mobile
- [ ] Test all internal links
- [ ] Check contact information is correct
- [ ] Verify social media links work

## 📝 Post-Deployment

- [ ] Share website URL with your team
- [ ] Add website link to app's about/help section
- [ ] Update email signatures with website link
- [ ] Share on social media

---

## Quick Commands

```bash
# Navigate to project
cd /Users/dgurjar/workspace/personal/UdyamOnWeb

# Create downloads folder
mkdir downloads

# Check git status
git status

# Push updates after changes
git add .
git commit -m "Update website content"
git push
```

## Need Help?

- Read `DEPLOYMENT-GUIDE.md` for detailed step-by-step instructions
- Read `README.md` for comprehensive documentation
- Check GitHub Pages docs: https://docs.github.com/en/pages

---

**Delete this file once you've completed all tasks!**
