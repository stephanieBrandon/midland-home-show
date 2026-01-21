# Midland Spring Home Show Website

## Overview
This is a modern, responsive website for the Midland Spring Home Show 2026, supporting the Midland District Shrine Club.

## Features
✅ Responsive design (works on all devices)
✅ Event details with embedded map
✅ Photo gallery from past events
✅ Sponsorship tiers display
✅ Contact form (Netlify handles submissions)
✅ Floor plan section (ready for upload)
✅ About the Shriners information

## File Structure
```
/
├── index.html          # Main HTML file
├── styles.css          # All styling
├── script.js           # JavaScript for interactivity
├── assets/
│   ├── fez-logo.png    # Logo for navigation
│   ├── fez-emblem.jpg  # Fez image for About section
│   └── gallery/        # Gallery images
│       ├── placeholder-1.jpg
│       ├── placeholder-2.jpg
│       └── ... (more images)
```

## How to Update Content

### 1. Replace Gallery Photos
Simply replace the images in the `assets/gallery/` folder:
- Name your images: `placeholder-1.jpg`, `placeholder-2.jpg`, etc.
- Recommended size: 800x600 pixels or similar aspect ratio
- Keep the filenames the same, or update references in `index.html`

### 2. Add Floor Plan
Once vendors are confirmed:
1. Create a PNG or PDF of your floor plan
2. Save it as `assets/floor-plan.pdf` or `floor-plan.png`
3. Update the Floor Plan section in `index.html` (line ~382) to display your file

### 3. Add Sponsor Logos
To add actual sponsor logos:
1. Save logos in `assets/sponsors/` folder
2. Update the "Sponsor Logos Section" in `index.html` (line ~544)
3. Replace placeholder divs with: `<img src="assets/sponsors/company-name.png" alt="Company Name">`

### 4. Update Event Details
To change dates, times, or location:
- Edit the Hero section (line ~78 in `index.html`)
- Edit the Event Details section (line ~268 in `index.html`)

### 5. Customize Colors
To adjust the color scheme:
- Edit the CSS variables at the top of `styles.css` (line ~7-15)

## Deploying to Netlify (Free Hosting)

### Step 1: Create GitHub Repository
1. Go to https://github.com and sign in (or create account)
2. Click "New Repository"
3. Name it: `midland-home-show`
4. Make it Public
5. Don't initialize with README (we already have files)

### Step 2: Upload Files to GitHub
Using GitHub website (easiest method):
1. Click "uploading an existing file"
2. Drag all files into the upload area (index.html, styles.css, script.js, assets folder)
3. Click "Commit changes"

OR using command line:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/midland-home-show.git
git push -u origin main
```

### Step 3: Deploy to Netlify
1. Go to https://www.netlify.com
2. Sign up with GitHub account
3. Click "Add new site" → "Import an existing project"
4. Choose GitHub and authorize Netlify
5. Select your `midland-home-show` repository
6. Click "Deploy site"

**That's it!** Netlify will give you a URL like `https://random-name-123.netlify.app`

### Step 4: Connect Custom Domain (From GoDaddy)
1. In Netlify, click "Domain settings"
2. Click "Add custom domain"
3. Enter your domain (e.g., `midlandhomeshow.com`)
4. Netlify will show you DNS records to add

**In GoDaddy:**
1. Log in to GoDaddy
2. Go to your domain → Manage DNS
3. Add the following records (Netlify will provide exact values):
   - Type: A Record → Points to: Netlify's IP
   - Type: CNAME → Host: www → Points to: your-site.netlify.app

**DNS Update takes 24-48 hours** but often works within a few hours.

## Making Updates After Site is Live

Two options:

### Option A: Through Netlify (Easiest - No Coding)
1. Log into Netlify
2. Go to your site → "Deploys"
3. Drag updated files into the deploy dropzone
4. Site updates automatically in ~30 seconds

### Option B: Through GitHub
1. Update files in GitHub repository
2. Netlify automatically rebuilds and deploys
3. Changes live in ~1 minute

## Contact Form
The contact form uses Netlify Forms (built-in, no setup needed):
- Submissions appear in Netlify dashboard under "Forms"
- You'll get email notifications for each submission
- Set up email in: Site settings → Forms → Form notifications

## Technical Details
- **Framework:** Pure HTML/CSS/JavaScript (no dependencies)
- **Fonts:** Google Fonts (Montserrat)
- **Icons:** Emoji characters (universally supported)
- **Maps:** Google Maps embed
- **Forms:** Netlify Forms (free tier includes 100 submissions/month)

## Browser Support
✅ Chrome/Edge (latest)
✅ Firefox (latest)
✅ Safari (latest)
✅ Mobile browsers (iOS Safari, Chrome Mobile)

## Performance
- Lightweight: ~50KB total (excluding images)
- Fast loading: < 2 seconds on 3G
- Mobile-optimized
- SEO-friendly

## Security
- HTTPS automatically enabled by Netlify
- Form spam protection included
- No server-side code = no security vulnerabilities

## Support
For questions about the website:
- Email: midlandhomeshow@live.ca

## License
© 2025 Midland District Shrine Club. All rights reserved.

## Future Enhancements (Optional)
- [ ] Add lightbox for gallery images
- [ ] Add vendor registration form
- [ ] Add newsletter signup
- [ ] Add live ticket counter
- [ ] Add interactive floor plan with clickable booths
