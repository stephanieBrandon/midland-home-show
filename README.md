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

