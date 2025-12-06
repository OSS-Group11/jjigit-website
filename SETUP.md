# Jjigit Website - Setup & Deployment Guide

## 📋 Table of Contents
- [Initial Setup](#initial-setup)
- [Configuration](#configuration)
- [GitHub Pages Deployment](#github-pages-deployment)
- [Custom Domain Setup](#custom-domain-setup)
- [Community Platform Setup](#community-platform-setup)
- [Troubleshooting](#troubleshooting)

## 🚀 Initial Setup

### 1. Update _config.yml

Replace the placeholder values with your actual information:

```yaml
# Basic Info
title: Jjigit
url: "https://yourusername.github.io"  # Change to your GitHub Pages URL

# Social
github_username: your-github-username  # Your GitHub username
email: contact@jjigit.io              # Your contact email

# Project URLs
project:
  live_url: "https://jjigit-fe.vercel.app/"
  docs_url: "https://jjigit-be.readthedocs.io/en/latest/"
  github_url: "https://github.com/yourusername/jjigit"  # Your repo URL
  discord_url: "https://discord.gg/your-invite-code"    # Your Discord invite
  discussions_url: "https://github.com/yourusername/jjigit/discussions"
```

### 2. Update Repository URLs

Search and replace throughout the project:
- Find: `yourusername`
- Replace with: Your actual GitHub username

Files to update:
- `_config.yml`
- `README.md`
- `SETUP.md` (this file)

## ⚙️ Configuration

### Update Contact Form

In `contact.md`, replace the Formspree form ID:

```html
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

To get a form ID:
1. Sign up at https://formspree.io
2. Create a new form
3. Copy your form ID
4. Replace `YOUR_FORM_ID` in the code

### Customize Colors

Edit `assets/css/style.css`:

```css
:root {
  --primary: #4F46E5;      /* Main brand color - Indigo */
  --secondary: #06B6D4;    /* Secondary color - Cyan */
  --accent: #F59E0B;       /* Accent color - Amber */
  /* Adjust these to match your brand */
}
```

### Add Logo/Favicon

1. Create a `assets/images/` directory
2. Add your logo and favicon images:
   - `favicon.png` (32x32 or 64x64)
   - `logo.png` (optional)
3. Update the logo emoji in `_layouts/default.html`:
   - Find: `🗳️`
   - Replace with: `<img src="/assets/images/logo.png" alt="Jjigit">` (if using image)

## 🌐 GitHub Pages Deployment

### Method 1: Automatic Deployment (Recommended)

1. Push your code to GitHub:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/jjigit-website.git
git push -u origin main
```

2. Enable GitHub Pages:
   - Go to your repository on GitHub
   - Click **Settings**
   - Navigate to **Pages** (in the left sidebar)
   - Under **Source**, select **GitHub Actions**
   - The workflow will automatically deploy your site

3. Access your site:
   - URL: `https://yourusername.github.io/jjigit-website`
   - Or: `https://yourusername.github.io` (if repo name is `yourusername.github.io`)

### Method 2: Manual Deployment

1. Build the site locally:
```bash
bundle exec jekyll build
```

2. The built site will be in the `_site/` directory

3. Deploy to GitHub Pages manually:
   - Create a `gh-pages` branch
   - Push the `_site/` contents to this branch

## 🔗 Custom Domain Setup

### 1. Add CNAME File

Create a file named `CNAME` in the root directory with your domain:

```
www.jjigit.io
```

### 2. Configure DNS

Add these records to your domain's DNS settings:

For **apex domain** (jjigit.io):
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
```

For **www subdomain** (www.jjigit.io):
```
Type: CNAME
Name: www
Value: yourusername.github.io
```

### 3. Enable HTTPS

1. Go to repository **Settings** > **Pages**
2. Check **Enforce HTTPS**
3. Wait for SSL certificate to be provisioned (can take up to 24 hours)

## 👥 Community Platform Setup

### GitHub Discussions

1. Enable Discussions:
   - Go to repository **Settings**
   - Scroll to **Features**
   - Check **Discussions**

2. Configure categories:
   - General
   - Ideas
   - Q&A
   - Show and Tell

3. Update the URL in `_config.yml`:
```yaml
discussions_url: "https://github.com/yourusername/jjigit/discussions"
```

### Discord Server

1. Create a Discord server
2. Set up channels:
   - #general
   - #announcements
   - #support
   - #development
   - #showcase

3. Create an invite link:
   - Server Settings > Invites
   - Create a permanent invite
   - Update `_config.yml`:
   ```yaml
   discord_url: "https://discord.gg/your-invite-code"
   ```

### Mailing List

#### Option 1: Mailchimp

1. Sign up at https://mailchimp.com
2. Create a new audience
3. Get the embedded form code
4. Replace the email form in `community.md`

#### Option 2: Buttondown

1. Sign up at https://buttondown.email
2. Create your newsletter
3. Get the subscription form
4. Update `community.md`

### Stack Overflow Tag

1. Build reputation on Stack Overflow
2. Create the `jjigit` tag when you have enough reputation
3. Or ask questions with existing tags and mention Jjigit

### Social Media

Set up official accounts:
- Twitter/X: @jjigit_official
- LinkedIn: /company/jjigit
- Reddit: r/jjigit
- YouTube: @jjigit

Update all social links in:
- `_config.yml`
- `contact.md`
- `_layouts/default.html`

## 🔍 Analytics Setup

### Google Analytics

1. Create a GA4 property at https://analytics.google.com
2. Get your measurement ID (G-XXXXXXXXXX)
3. Add to `_layouts/default.html`:

```html
{% if jekyll.environment == 'production' %}
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
{% endif %}
```

## 🐛 Troubleshooting

### Build Failures

**Problem**: Jekyll build fails
**Solution**: 
```bash
bundle install
bundle update
bundle exec jekyll build --verbose
```

### Styles Not Loading

**Problem**: CSS not applying
**Solution**:
1. Check `_config.yml` for correct `baseurl`
2. Clear browser cache
3. Check browser console for 404 errors

### Images Not Displaying

**Problem**: Images return 404
**Solution**:
1. Verify images are in `assets/images/`
2. Use correct relative paths: `/assets/images/image.png`
3. Check file names for typos

### Forms Not Working

**Problem**: Contact form doesn't submit
**Solution**:
1. Verify Formspree form ID is correct
2. Check browser console for errors
3. Test with a different email

### GitHub Pages Not Updating

**Problem**: Changes not reflected on live site
**Solution**:
1. Check GitHub Actions tab for build status
2. Clear browser cache
3. Wait 5-10 minutes for propagation
4. Check repository Settings > Pages for errors

## 📝 Checklist Before Going Live

- [ ] Update all placeholder URLs in `_config.yml`
- [ ] Replace `YOUR_FORM_ID` in contact form
- [ ] Set up Discord server and update invite link
- [ ] Enable GitHub Discussions
- [ ] Configure custom domain (if applicable)
- [ ] Add favicon and logo images
- [ ] Set up analytics
- [ ] Test all links
- [ ] Test contact form
- [ ] Review responsive design on mobile
- [ ] Set up HTTPS
- [ ] Create social media accounts
- [ ] Write initial blog post/announcement

## 🆘 Getting Help

If you encounter issues:

1. Check the [Jekyll Documentation](https://jekyllrb.com/docs/)
2. Review [GitHub Pages Documentation](https://docs.github.com/en/pages)
3. Open an issue on the repository
4. Ask in GitHub Discussions
5. Join our Discord server

## 📚 Additional Resources

- [Jekyll Themes](https://jekyllrb.com/docs/themes/)
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Pages Custom Domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Formspree Documentation](https://help.formspree.io/)
- [Discord Server Setup Guide](https://support.discord.com/hc/en-us/articles/204849977-How-do-I-create-a-server-)

---

**Happy Building! 🚀**

Need help? Contact us at contact@jjigit.io
