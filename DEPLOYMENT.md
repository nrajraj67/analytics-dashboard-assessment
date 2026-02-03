# Deployment Guide

This guide will help you deploy your EV Analytics Dashboard to various hosting platforms.

## Quick Deploy Options

### Option 1: Netlify (Recommended - Easiest)

1. **Via Netlify Drop**
   - Go to https://app.netlify.com/drop
   - Drag and drop your project folder
   - Your site will be live instantly!

2. **Via GitHub**
   - Push your code to GitHub
   - Go to https://app.netlify.com
   - Click "New site from Git"
   - Connect your repository
   - Deploy settings:
     - Build command: (leave empty)
     - Publish directory: `.`
   - Click "Deploy site"

3. **Via Netlify CLI**
   ```bash
   npm install -g netlify-cli
   netlify login
   netlify init
   netlify deploy --prod
   ```

### Option 2: Vercel

1. **Via Vercel CLI**
   ```bash
   npm i -g vercel
   vercel login
   vercel
   ```

2. **Via GitHub**
   - Push code to GitHub
   - Go to https://vercel.com
   - Click "New Project"
   - Import your repository
   - Click "Deploy"

### Option 3: GitHub Pages

1. Push your code to GitHub
2. Go to repository Settings
3. Navigate to Pages section
4. Source: Select "main" branch
5. Click Save
6. Your site will be at: `https://yourusername.github.io/repository-name`

### Option 4: Render

1. Push code to GitHub
2. Go to https://render.com
3. Click "New Static Site"
4. Connect your repository
5. Settings:
   - Build Command: (leave empty)
   - Publish Directory: `.`
6. Click "Create Static Site"

## File Structure for Deployment

Your deployment should include:
```
ev-analytics-dashboard/
├── index.html          (main file)
├── data/
│   └── ev-data.csv    (your CSV file - optional)
├── README.md
├── package.json
├── netlify.toml       (for Netlify)
├── vercel.json        (for Vercel)
└── .gitignore
```

## Using Your Own CSV Data

To use your actual EV dataset:

1. Create a `data` folder in your project
2. Place your CSV file as `data/ev-data.csv`
3. The dashboard will automatically load it
4. Make sure your CSV has these columns:
   - VIN
   - County
   - City
   - State
   - Postal Code
   - Model Year
   - Make
   - Model
   - Electric Vehicle Type
   - Electric Range

Alternatively, you can upload CSV files directly through the dashboard interface.

## Post-Deployment Steps

1. **Test Your Site**
   - Open the deployed URL
   - Check all visualizations load
   - Test filters work correctly
   - Verify CSV upload works (if using)

2. **Update README**
   - Add your live dashboard URL to README.md
   - Commit and push changes

3. **Share Your Link**
   - Copy your deployment URL
   - Add collaborators to your GitHub repo:
     - vedantp@mapup.ai
     - ajayap@mapup.ai
     - atharvd@mapup.ai
   - Fill out the submission form

## Common Issues

### Issue: CSV file not loading
**Solution**: Make sure the CSV file path is correct in the code or use the upload feature

### Issue: Charts not displaying
**Solution**: Check browser console for errors. Ensure Chart.js CDN is accessible

### Issue: 404 errors on page refresh
**Solution**: Add redirect rules (already included in netlify.toml and vercel.json)

## Performance Tips

1. **Keep CSV file size reasonable** (<5MB recommended)
2. **Use browser caching** (automatic with most hosts)
3. **Compress images** if you add any
4. **Monitor loading times** and optimize if needed

## Custom Domain (Optional)

Most platforms allow custom domains:
- Netlify: Settings → Domain management
- Vercel: Settings → Domains
- GitHub Pages: Settings → Pages → Custom domain

## Need Help?

- Netlify Docs: https://docs.netlify.com
- Vercel Docs: https://vercel.com/docs
- GitHub Pages: https://docs.github.com/pages

---

**Note**: The dashboard works as a static site - no server-side code required!
