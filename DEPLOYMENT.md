# 🚀 GitHub Pages Deployment Guide

## Mission Control - European Space Network Atlas
**Deploy in 5 minutes on GitHub Pages**

---

## Quick Start

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com/new)
2. Create a new repository named: `space-network-atlas`
3. Choose **Public** (required for GitHub Pages)
4. Click **Create repository**

### Step 2: Upload Files to GitHub

You have two options:

#### Option A: Using GitHub Web Interface (Easiest)

1. On your repository page, click **Add file** → **Upload files**
2. Upload these files:
   - `index.html` (main interactive page)
   - `esa_members_data.json` (data file)
   - `DEPLOYMENT.md` (this file)
   - `README.md`

3. Click **Commit changes**

#### Option B: Using Git Command Line (Recommended)

```bash
# Navigate to your project directory
cd /path/to/Space_Lab_01

# Initialize git
git init

# Add remote
git remote add origin https://github.com/YOUR_USERNAME/space-network-atlas.git

# Add all files
git add .

# Commit
git commit -m "Initial commit: European Space Network Atlas"

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. In the left sidebar, click **Pages**
4. Under "Source", select:
   - **Branch**: `main`
   - **Folder**: `/ (root)`
5. Click **Save**

### Step 4: Access Your Live Website

GitHub will provide a URL like:
```
https://YOUR_USERNAME.github.io/space-network-atlas/
```

✅ **Your atlas is now LIVE!**

---

## Features

### 🗺️ Interactive Map
- **Leaflet.js powered** with OpenStreetMap tiles
- Click markers to view agency details
- Full coordinates and address information
- Real-time zoom and pan controls

### 📊 Data Table
- **Search functionality** - Filter by agency name, country, or city
- **Live statistics** - Total agencies, countries, founding dates
- Click rows to jump to location on map
- Responsive design works on mobile

### 📍 20 Space Agencies
- ESA member states
- Associated partner countries
- Complete headquarters information
- Latitude/longitude coordinates

---

## File Structure

```
space-network-atlas/
├── index.html                 # Main interactive page (all-in-one)
├── esa_members_data.json     # Space agencies data
├── DEPLOYMENT.md             # This guide
├── README.md                 # Project overview
└── .gitignore               # Git ignore rules (optional)
```

---

## Customization

### Add New Space Agencies

Edit `index.html`, find the `loadData()` function, and add to the array:

```javascript
{
    "name": "Agency Name",
    "country": "Country",
    "city": "City",
    "address": "Full Address",
    "latitude": 45.1234,
    "longitude": 12.5678,
    "founded": 2000
}
```

### Change Colors

Search for `#0066cc` in `index.html` and replace with your color:
- `#0066cc` = Primary blue

### Modify Map Center

In the `initMap()` function, change:
```javascript
map.setView([54.5260, 15.2551], 4);  // [latitude, longitude, zoom]
```

---

## Troubleshooting

### Page shows blank
- ✅ Check GitHub Pages is enabled in Settings
- ✅ Wait 1-2 minutes for deployment
- ✅ Hard refresh (Ctrl+Shift+R or Cmd+Shift+R)

### Map not showing
- ✅ Check internet connection (needs OpenStreetMap tiles)
- ✅ Check browser console for errors (F12)

### Data not loading
- ✅ Ensure `esa_members_data.json` is in root folder
- ✅ Clear browser cache

---

## Sharing Your Atlas

Share the live link:
```
https://YOUR_USERNAME.github.io/space-network-atlas/
```

Embed in presentations:
```html
<iframe src="https://YOUR_USERNAME.github.io/space-network-atlas/" width="100%" height="700"></iframe>
```

---

## Tech Stack

- **HTML5** - Semantic markup
- **CSS3** - Modern responsive design
- **JavaScript (Vanilla)** - No frameworks needed
- **Leaflet.js** - Interactive maps
- **OpenStreetMap** - Map tiles
- **Font Awesome** - Icons
- **GitHub Pages** - Free hosting

---

## Performance

- ⚡ **Instant load** - Static files, no backend needed
- 🔄 **Real-time updates** - Edit JSON and push to update
- 🌍 **Global CDN** - GitHub Pages uses Cloudflare globally
- 📱 **100% Responsive** - Works on all devices

---

## Next Steps

1. ✅ Deploy to GitHub Pages
2. 📊 Display to Mission Control
3. 📈 Add more space agencies
4. 🔐 Add authentication (future enhancement)
5. 🌐 Custom domain (optional)

---

**Status**: 🟢 Live on GitHub Pages  
**Last Updated**: April 8, 2026  
**Deployment Time**: < 5 minutes  

---

### Support

For issues:
1. Check browser console (F12)
2. Verify all files are in repository
3. Clear GitHub Pages cache

**Success Criteria**: ✅ Interactive map + ✅ Data table + ✅ Live web URL
