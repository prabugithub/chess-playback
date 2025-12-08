# 🚀 Deployment Guide - Chess Playback Viewer

This guide will help you deploy your Chess Playback Viewer to various free hosting platforms.

## Quick Comparison

| Platform | Difficulty | Custom Domain | Build Time | Best For |
|----------|-----------|---------------|------------|----------|
| **GitHub Pages** | Easy | ✅ Yes (Free) | ~2 min | Open source projects |
| **Netlify** | Very Easy | ✅ Yes (Free) | ~1 min | Fastest deployment |
| **Vercel** | Easy | ✅ Yes (Free) | ~2 min | Modern workflow |
| **Firebase** | Medium | ✅ Yes (Free) | ~5 min | Google ecosystem |

---

## 1. GitHub Pages (Recommended for Beginners)

### Step-by-Step Instructions:

**Prerequisites:**
- GitHub account
- Git installed (optional)

**Method A: Using GitHub Web Interface**

1. **Create Repository**
   - Go to [GitHub](https://github.com)
   - Click "New Repository"
   - Name it: `chess-playback` (or any name)
   - Make it **Public**
   - Click "Create repository"

2. **Upload File**
   - Click "uploading an existing file"
   - Rename `chess-playback-standalone.html` to `index.html`
   - Drag & drop `index.html`
   - Click "Commit changes"

3. **Enable GitHub Pages**
   - Go to Settings → Pages
   - Source: Deploy from branch
   - Branch: `main` → `/ (root)`
   - Click Save

4. **Access Your Site**
   - Wait 2-3 minutes
   - Visit: `https://yourusername.github.io/chess-playback`

**Method B: Using Git Command Line**

```bash
# 1. Create a new directory
mkdir chess-playback
cd chess-playback

# 2. Initialize Git
git init

# 3. Copy your HTML file and rename it
cp /path/to/chess-playback-standalone.html index.html

# 4. Add and commit
git add index.html
git commit -m "Initial commit"

# 5. Connect to GitHub
git branch -M main
git remote add origin https://github.com/yourusername/chess-playback.git
git push -u origin main

# 6. Enable GitHub Pages in repository settings
```

### Custom Domain (Optional)
1. Buy domain from Namecheap, GoDaddy, etc.
2. Add CNAME file with your domain
3. Configure DNS settings in your domain provider
4. Add custom domain in GitHub Pages settings

---

## 2. Netlify (Fastest Deployment)

### Method A: Drag & Drop (Easiest!)

1. **Visit Netlify Drop**
   - Go to [Netlify Drop](https://app.netlify.com/drop)
   - No account needed for this!

2. **Upload File**
   - Drag & drop `chess-playback-standalone.html`
   - Rename it to `index.html` before uploading

3. **Get Your URL**
   - Instantly get: `https://random-name.netlify.app`
   - Can change name in site settings

### Method B: Using Netlify CLI

```bash
# 1. Install Netlify CLI
npm install -g netlify-cli

# 2. Login to Netlify
netlify login

# 3. Create directory and add file
mkdir chess-playback
cp chess-playback-standalone.html chess-playback/index.html

# 4. Deploy
cd chess-playback
netlify deploy --prod

# Follow prompts to create new site
```

### Method C: GitHub Integration

1. Push code to GitHub (see GitHub Pages method)
2. Go to [Netlify](https://app.netlify.com)
3. Click "Import from Git"
4. Select your GitHub repo
5. Click "Deploy site"
6. Auto-deploys on every GitHub push!

### Custom Domain on Netlify
1. Go to Domain settings
2. Add custom domain
3. Configure DNS with your provider
4. Netlify handles SSL automatically!

---

## 3. Vercel (Modern & Fast)

### Method A: Vercel CLI

```bash
# 1. Install Vercel CLI
npm install -g vercel

# 2. Create directory
mkdir chess-playback
cp chess-playback-standalone.html chess-playback/index.html
cd chess-playback

# 3. Deploy
vercel

# Follow prompts:
# - Set up and deploy? Yes
# - Which scope? Your username
# - Link to existing project? No
# - Project name? chess-playback
# - Directory? ./
# - Override settings? No
```

### Method B: GitHub Integration

1. Push to GitHub
2. Go to [Vercel](https://vercel.com)
3. Click "Import Project"
4. Select GitHub repository
5. Click "Deploy"

### Features
- Automatic HTTPS
- Global CDN
- Instant deployments
- Auto-preview for branches

---

## 4. Firebase Hosting

### Prerequisites
- Google account
- Node.js installed

### Setup Instructions

```bash
# 1. Install Firebase CLI
npm install -g firebase-tools

# 2. Login to Firebase
firebase login

# 3. Create project directory
mkdir chess-playback
cd chess-playback

# 4. Initialize Firebase
firebase init hosting

# Select options:
# - Create new project or select existing
# - Public directory: . (current directory)
# - Single-page app: No
# - Set up automatic builds: No

# 5. Copy your file
cp /path/to/chess-playback-standalone.html index.html

# 6. Deploy
firebase deploy
```

### Your site will be at:
```
https://your-project-id.web.app
```

---

## 5. Alternative Free Hosting Options

### A. Surge.sh (Super Simple)

```bash
# Install
npm install -g surge

# Deploy
surge chess-playback-standalone.html

# You'll get: https://random-name.surge.sh
```

### B. Render

1. Go to [Render](https://render.com)
2. New Static Site
3. Connect GitHub repo
4. Deploy

### C. Cloudflare Pages

1. Go to [Cloudflare Pages](https://pages.cloudflare.com)
2. Connect GitHub
3. Deploy
4. Free SSL + CDN

---

## 📝 Pre-Deployment Checklist

Before deploying, ensure:

- [ ] File is renamed to `index.html`
- [ ] Test locally in browser
- [ ] Check all features work
- [ ] Sample game loads correctly
- [ ] Share link generation works
- [ ] Mobile responsive (test on phone)

---

## 🎯 Post-Deployment

### Testing Your Deployment

1. **Open in incognito/private window**
   - Ensures no cache issues

2. **Test on multiple devices**
   - Desktop
   - Mobile
   - Tablet

3. **Test all features**
   - Upload JSON
   - Paste JSON
   - Play/Pause
   - Speed controls
   - Share link generation

### Share Your Chess Viewer!

Once deployed, share your link:
```
https://your-username.github.io/chess-playback
https://your-site.netlify.app
https://your-site.vercel.app
```

---

## 🔧 Troubleshooting

### Common Issues

**1. "404 Not Found"**
- Wait 5 minutes after deployment
- Check if file is named `index.html`
- Clear browser cache

**2. "Site Not Found"**
- Verify GitHub Pages is enabled
- Check branch is correct (usually `main`)
- Ensure repository is public

**3. "Styles Not Loading"**
- Everything is in one HTML file, so this shouldn't happen
- Clear cache and hard refresh (Ctrl+F5)

**4. "JSON Upload Not Working"**
- Check browser console for errors
- Ensure JSON format is correct
- Try paste JSON method instead

---

## 🎨 Customization After Deployment

To update your deployed site:

**GitHub Pages:**
```bash
git add index.html
git commit -m "Update chess viewer"
git push
```

**Netlify Drag & Drop:**
- Simply drag new version to existing site

**Netlify/Vercel with Git:**
- Push to GitHub
- Auto-deploys!

---

## 💰 Cost Summary

| Platform | Free Tier | Bandwidth | Storage | Custom Domain |
|----------|-----------|-----------|---------|---------------|
| GitHub Pages | ✅ Unlimited | 100GB/month | 1GB | Free |
| Netlify | ✅ Unlimited | 100GB/month | Unlimited | Free |
| Vercel | ✅ Unlimited | 100GB/month | Unlimited | Free |
| Firebase | ✅ Unlimited | 10GB/month | 10GB | Free |

**All platforms offer:**
- Free SSL certificates
- Custom domains at no extra cost
- No credit card required for free tier

---

## 🌟 Recommended Setup

**For Personal Use:**
→ GitHub Pages (simplest)

**For Frequent Updates:**
→ Netlify + GitHub (auto-deploy)

**For Maximum Performance:**
→ Vercel (fastest CDN)

**For Google Ecosystem:**
→ Firebase Hosting

---

## 📱 Mobile Testing

After deployment, test on:
- Chrome (Android/iOS)
- Safari (iOS)
- Firefox (Android)

Use these tools:
- [BrowserStack](https://www.browserstack.com) (free trial)
- Chrome DevTools (F12 → Device Toolbar)
- [Responsively App](https://responsively.app) (free)

---

## 🔗 Useful Resources

- [GitHub Pages Docs](https://docs.github.com/en/pages)
- [Netlify Docs](https://docs.netlify.com)
- [Vercel Docs](https://vercel.com/docs)
- [Firebase Docs](https://firebase.google.com/docs/hosting)

---

**Need help? Common issues are usually:**
1. File not named `index.html`
2. Waiting for DNS propagation (can take up to 48h)
3. Browser cache (clear it!)

Good luck with your deployment! 🚀♟️
