# Udyam - Smart Business Management Software Website

A modern, responsive website for Udyam - a powerful business management application designed for small businesses, retailers, and traders in India.

## 🌐 Live Demo

Once deployed, your site will be available at: `https://yourusername.github.io/UdyamOnWeb/`

## 📋 Features

- **Home Page**: Hero section with download buttons for Windows and macOS, feature highlights, testimonials, and system requirements
- **Features Page**: Comprehensive showcase of all app capabilities including sales management, inventory, payments, returns, reports, pricing plans, and roadmap
- **Contact Page**: Multiple contact methods, support options, FAQ, and business information
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Modern UI**: Clean, professional design with smooth animations and intuitive navigation
- **India-Focused**: Content tailored for Indian businesses with GST, Hindi support, and local business practices

## 🚀 Deployment to GitHub Pages

### Step 1: Initialize Git Repository

```bash
cd /Users/dgurjar/workspace/personal/UdyamOnWeb
git init
git add .
git commit -m "Initial commit: Udyam website"
```

### Step 2: Create GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository named `UdyamOnWeb`
2. Make it **public** (required for free GitHub Pages)
3. Don't initialize it with README, .gitignore, or license

### Step 3: Push to GitHub

```bash
git remote add origin https://github.com/yourusername/UdyamOnWeb.git
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** → **Pages**
3. Under "Source", select **main** branch and **/ (root)** folder
4. Click **Save**
5. Your site will be live in a few minutes at `https://yourusername.github.io/UdyamOnWeb/`

**Note:** Replace `yourusername` with your actual GitHub username.

## 📦 Adding Download Files

### Option 1: Store Files in Repository (Current Setup)

The site is currently configured to look for files in a `downloads` folder:

1. Create a `downloads` folder in your repository:
   ```bash
   mkdir downloads
   ```

2. Add your installer files:
   - `Udyam-Setup.exe` (Windows installer)
   - `Udyam.dmg` (macOS installer)

3. Commit and push:
   ```bash
   git add downloads/
   git commit -m "Add installer files"
   git push
   ```

**Current download links in the HTML:**
- Windows: `./downloads/Udyam-Setup.exe`
- macOS: `./downloads/Udyam.dmg`

### Option 2: Using GitHub Releases (Recommended for Large Files)

If your installer files are large (>100MB), use GitHub Releases:

1. Go to your repository on GitHub
2. Click on **Releases** → **Create a new release**
3. Tag version (e.g., `v1.0.0`)
4. Upload your `Udyam-Setup.exe` and `Udyam.dmg` files
5. Publish the release
6. Update the download links in `index.html`:

```html
<!-- Change from -->
<a href="./downloads/Udyam-Setup.exe" class="btn btn-primary download-btn">

<!-- To -->
<a href="https://github.com/yourusername/UdyamOnWeb/releases/download/v1.0.0/Udyam-Setup.exe" class="btn btn-primary download-btn">
```

### Option 3: External Storage

For very large files or bandwidth concerns, use cloud storage:
- Google Drive (get shareable link)
- Dropbox
- AWS S3
- Azure Blob Storage

Then update the `href` attributes in `index.html` with the direct download links.

## 📧 Contact Information

The contact page displays multiple contact methods. Update these with your actual contact details:

### Update Email Addresses

In `contact.html`, replace the placeholder emails:
- `sales@udyam.app` → Your sales email
- `support@udyam.app` → Your support email
- `info@udyam.app` → Your general inquiries email
- `bugs@udyam.app` → Your bug reports email
- `feedback@udyam.app` → Your feedback email
- `partnerships@udyam.app` → Your partnerships email

### Update Phone Numbers

Replace `+91-XXXXX-XXXXX` with your actual phone numbers.

### Update Business Address

In the "Office Address" section, replace:
- `[Your Address]`
- `[City, State - PIN]`

With your actual business address.

### Optional: Add Contact Form

The current design focuses on direct contact methods. If you want to add a contact form:

1. Use a service like [FormSubmit.co](https://formsubmit.co/) (free, no backend)
2. Or [Formspree.io](https://formspree.io/) (free tier available)
3. Add the form HTML in the contact page

## 🎨 Customization

### Change Brand Colors

Edit the CSS variables in `style.css` (lines 13-24):

```css
:root {
    --primary-color: #4f46e5;      /* Main brand color - buttons, links */
    --primary-dark: #4338ca;       /* Darker shade for hover states */
    --secondary-color: #10b981;    /* Accent color for checkmarks, highlights */
    --text-dark: #1f2937;          /* Primary text color */
    --text-light: #6b7280;         /* Secondary text color */
    --bg-light: #f9fafb;           /* Light background sections */
    --bg-white: #ffffff;           /* White backgrounds */
    --border-color: #e5e7eb;       /* Border and divider lines */
}
```

### Add Your Logo

Replace the text logo in the navigation (in all 3 HTML files):

```html
<!-- Change from -->
<div class="logo">
    <h2>Udyam</h2>
</div>

<!-- To -->
<div class="logo">
    <img src="images/logo.png" alt="Udyam Logo" height="40">
</div>
```

### Add App Screenshots

Replace the emoji placeholders in `features.html` with actual screenshots:

```html
<!-- Change from -->
<div class="placeholder-image">🛍️</div>

<!-- To -->
<img src="images/sales-screenshot.png" alt="Sales Management" style="width: 100%; border-radius: 12px;">
```

Create an `images` folder and add your screenshots:
```bash
mkdir images
# Add your images to this folder
```

### Update Links

Replace placeholder URLs:
- In `contact.html`: Update GitHub, Twitter, LinkedIn links
- In `README.md`: Update repository URLs with your GitHub username

## 📱 Testing Locally

Open `index.html` in your web browser to test the site locally before deploying.

## 🔧 Troubleshooting

### Site not showing up?
- Wait 5-10 minutes after enabling GitHub Pages
- Check that the repository is public
- Verify the correct branch and folder are selected in Settings → Pages

### Download links not working?
- Make sure file URLs are correct
- Check that files are accessible (not in a private release)
- Test the URLs directly in the browser

### Contact form not working?
- Integrate with a form handling service (see above)
- Check browser console for errors

## 📄 File Structure

```
UdyamOnWeb/
├── index.html          # Home page (hero, features overview, testimonials, system requirements)
├── features.html       # Features page (detailed features, coming soon, pricing)
├── contact.html        # Contact page (all contact methods, support, FAQ)
├── style.css          # Complete styling for all pages
├── README.md          # Documentation and deployment guide
└── downloads/         # (Create this folder) Place your .exe and .dmg files here
    ├── Udyam-Setup.exe
    └── Udyam.dmg
```

### Content Breakdown

**index.html includes:**
- Navigation bar
- Hero section with download buttons
- Why Choose Udyam (6 reasons)
- Perfect For (5 business types)
- User testimonials
- System requirements
- CTA banner
- Footer

**features.html includes:**
- Sales Management (transactions, customers)
- Inventory Management (products, stock)
- Payment Tracking
- Returns Management
- Debitor & Creditor Management
- Reports & Analytics
- Multi-Language Support
- Security & Privacy
- Advanced Features
- Coming Soon section (7 upcoming features)
- Pricing (3 plans)

**contact.html includes:**
- Sales, Technical Support, General contact info
- Support options (email, phone, chat, knowledge base)
- Bug reports and feature requests
- Partnership opportunities
- Business information
- Social media links
- FAQ (6 questions)
- Office address
- Resources links

## 🤝 Contributing

Feel free to customize this site for your needs. The code is clean and well-commented for easy modifications.

## 📝 License

This template is free to use for your project.

---

**Need help?** Open an issue or check the GitHub Pages documentation at https://docs.github.com/en/pages
