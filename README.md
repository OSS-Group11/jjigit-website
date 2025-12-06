# Jjigit Website

Official website for Jjigit - An AI-powered voting and discussion platform.

## 🚀 Quick Start

### Prerequisites

- Ruby 2.7 or higher
- Bundler

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/jjigit-website.git
cd jjigit-website
```

2. Install dependencies:
```bash
bundle install
```

3. Run the development server:
```bash
bundle exec jekyll serve
```

4. Open your browser and visit `http://localhost:4000`

## 📁 Project Structure

```
jjigit-website/
├── _layouts/          # HTML layouts
│   └── default.html
├── assets/
│   └── css/
│       └── style.css  # Main stylesheet
├── index.md           # Homepage
├── features.md        # Features page
├── community.md       # Community page
├── contact.md         # Contact page
├── _config.yml        # Jekyll configuration
├── Gemfile            # Ruby dependencies
└── README.md          # This file
```

## 🛠️ Customization

### Update Site Information

Edit `_config.yml` to update:
- Site title and description
- GitHub repository URL
- ReadTheDocs documentation URL
- Live application URL
- Social media links

### Modify Colors

Edit the CSS variables in `assets/css/style.css`:

```css
:root {
  --primary: #4F46E5;      /* Primary color */
  --secondary: #06B6D4;    /* Secondary color */
  --accent: #F59E0B;       /* Accent color */
  /* ... */
}
```

### Add New Pages

1. Create a new `.md` file in the root directory
2. Add front matter:
```yaml
---
layout: default
title: Your Page Title
permalink: /your-page/
---
```
3. Add your content
4. Update navigation in `_layouts/default.html`

## 🌐 Deployment

### GitHub Pages

1. Push your code to GitHub
2. Go to Settings > Pages
3. Select the branch you want to deploy
4. Save and wait for deployment

### Custom Domain

1. Add a `CNAME` file with your domain
2. Configure DNS settings with your domain provider
3. Enable HTTPS in GitHub Pages settings

## 📝 Content Updates

### Homepage
Edit `index.md` to update:
- Hero section
- Mission statement
- Feature preview
- Quick links

### Features Page
Edit `features.md` to:
- Add new features
- Update feature descriptions
- Modify visual placeholders

### Community Page
Edit `community.md` to:
- Update communication channels
- Add new community platforms
- Modify contribution guidelines

### Contact Page
Edit `contact.md` to:
- Update contact information
- Modify contact form
- Add social links

## 🎨 Design Guidelines

The website follows a modern, professional design with:
- **Color Scheme**: Indigo (#4F46E5) and Cyan (#06B6D4)
- **Typography**: System fonts for optimal performance
- **Layout**: Responsive grid-based design
- **Components**: Card-based interface elements
- **Icons**: Inline SVG for flexibility

## 📱 Responsive Design

The website is fully responsive and optimized for:
- Desktop (1200px+)
- Tablet (768px - 1199px)
- Mobile (< 768px)

## 🧩 Components

### Buttons
- Primary: White background, primary text
- Secondary: Transparent with border
- Tertiary: Minimal styling

### Cards
- Feature cards: Gradient icons, shadow effects
- Link cards: Left border accent
- Channel cards: Platform-specific styling

### Forms
- Contact form with validation
- Newsletter subscription
- Customizable field types

## 🔧 Advanced Customization

### Adding Analytics

Edit `_layouts/default.html` and add your analytics code in the production block:

```html
{% if jekyll.environment == 'production' %}
  <!-- Your analytics code here -->
{% endif %}
```

### Custom JavaScript

Add custom scripts at the bottom of `_layouts/default.html` before the closing `</body>` tag.

### Email Form Integration

The contact form uses Formspree. To integrate:

1. Sign up at [Formspree](https://formspree.io)
2. Create a new form
3. Replace `YOUR_FORM_ID` in `contact.md` with your Formspree form ID

## 📄 License

This website template is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

For issues and questions:
- GitHub Issues: [Report a bug](https://github.com/yourusername/jjigit-website/issues)
- Email: contact@jjigit.io

## 🙏 Acknowledgments

Built with:
- [Jekyll](https://jekyllrb.com/) - Static site generator
- [GitHub Pages](https://pages.github.com/) - Hosting
- Inspired by [Apache Hadoop](https://hadoop.apache.org/) and [Django](https://www.djangoproject.com/)
