# GeoHeatWhisper Static Documentation

This is the static `/docs` site for GeoHeatWhisper that makes your content crawlable by LLMs and search engines, even though your main app is a Lovable React SPA.

## What's Included

- **docs/** - Complete static documentation site
  - `index.html` - Documentation landing page
  - `how-it-works.html` - Step-by-step guide to geo-grid tracking
  - `features.html` - Complete feature breakdown
  - `pricing.html` - Pricing plans comparison
  - `use-cases.html` - Real-world applications
  - `faq.html` - Frequently asked questions

- **llms.txt** - Machine-readable file pointing LLM crawlers to your docs

## Quick Deploy to GitHub Pages (FREE)

### Option 1: GitHub Web Interface (Easiest)

1. **Create a new repo** called `geoheatwhisper-docs` (or any name)

2. **Upload files:**
   - Go to your new repo
   - Click "Add file" > "Upload files"
   - Drag and drop the entire `docs/` folder and `llms.txt`
   - Commit

3. **Enable GitHub Pages:**
   - Go to repo Settings > Pages
   - Source: Deploy from branch
   - Branch: `main`, folder: `/ (root)`
   - Save

4. **Update your DNS:**
   - Your docs will be live at `https://yourusername.github.io/geoheatwhisper-docs/`
   - To use a custom domain like `docs.geoheatwhisper.com`:
     - Add a `CNAME` file to your repo with content: `docs.geoheatwhisper.com`
     - Add a CNAME record in your DNS pointing to `yourusername.github.io`

### Option 2: GitHub CLI (If you have git installed)

```bash
# Clone or create a new repo
git init geoheatwhisper-docs
cd geoheatwhisper-docs

# Copy files into the repo
cp -r /path/to/docs .
cp /path/to/llms.txt .

# Commit and push
git add .
git commit -m "Initial docs site"
git branch -M main
git remote add origin https://github.com/yourusername/geoheatwhisper-docs.git
git push -u origin main

# Enable Pages via Settings > Pages in GitHub web interface
```

## Linking from Your Main Lovable App

Once deployed, update your main Lovable app to link to the docs:

1. **Add prominent link in your nav/header:**
   ```jsx
   <a href="https://docs.geoheatwhisper.com">Documentation</a>
   ```

2. **Update your main llms.txt** at the root of geoheatwhisper.com:
   ```
   # GeoHeatWhisper Documentation
   
   > For comprehensive documentation, visit https://docs.geoheatwhisper.com
   
   ## Key Pages
   - Documentation: https://docs.geoheatwhisper.com/
   - How It Works: https://docs.geoheatwhisper.com/how-it-works.html
   - Features: https://docs.geoheatwhisper.com/features.html
   - Pricing: https://docs.geoheatwhisper.com/pricing.html
   ```

## Alternative Hosting Options

If you prefer not to use GitHub Pages:

### Netlify (Also Free)
1. Create account at netlify.com
2. Drag and drop your files
3. Custom domain: Settings > Domain Management

### Cloudflare Pages (Also Free)
1. Create account at pages.cloudflare.com
2. Connect GitHub repo or upload files
3. Custom domain: Settings > Custom Domains

### Vercel (Also Free)
1. Create account at vercel.com
2. Import GitHub repo
3. Custom domain: Settings > Domains

## Updating Content

To update docs after initial deploy:

1. Edit the HTML files locally
2. Commit and push changes (git method) or re-upload via GitHub interface
3. Changes go live automatically (typically within 1-2 minutes)

## SEO Tips

Once live, help search engines discover your docs:

1. **Submit sitemap** to Google Search Console
2. **Internal linking:** Link to docs from your main app
3. **Update meta tags** if needed (already included in HTML)
4. **Build backlinks:** Link to docs from blog posts, social media

## Testing

Before going live, test locally:

```bash
# Use Python's built-in HTTP server
cd docs
python -m http.server 8000

# Or use Node's http-server
npx http-server . -p 8000
```

Visit `http://localhost:8000` to preview.

## Questions?

- GitHub Pages docs: https://docs.github.com/pages
- Need help? Open an issue or contact support
