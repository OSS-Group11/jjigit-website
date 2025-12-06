# Jjigit Website

Official website for Jjigit - An AI-powered voting and discussion platform.

🌐 **Live Site:** [https://oss-group11.github.io/jjigit-website/](https://oss-group11.github.io/jjigit-website/)

## 📌 About Jjigit

Jjigit is an AI-powered voting and discussion platform that empowers communities to engage in democratic discourse. This repository hosts the official project website built with Jekyll and GitHub Pages.

### Key Features

- 🗳️ **User-Generated Voting Topics** - Create and participate in polls on topics that matter
- 🤖 **AI Topic Suggestions** - Get intelligent topic recommendations powered by AI
- ⏰ **Automated Content Generation** - AI automatically generates fresh topics every hour
- 💬 **Real-Time Discussions** - Engage in live debates with users worldwide
- 🔐 **Secure Authentication** - Personalized experience with user profiles and voting history

## 🔗 Project Links

### Main Applications
- **Live App:** [https://jjigit-fe.vercel.app/](https://jjigit-fe.vercel.app/)
- **API Documentation:** [https://jjigit-be.readthedocs.io/](https://jjigit-be.readthedocs.io/)

### Repositories
- **GitHub Organization:** [https://github.com/OSS-Group11](https://github.com/OSS-Group11)
- **Frontend Repository:** [https://github.com/OSS-Group11/jjigit-fe](https://github.com/OSS-Group11/jjigit-fe)
- **Backend Repository:** [https://github.com/OSS-Group11/jjigit-be](https://github.com/OSS-Group11/jjigit-be)
- **AI/ML Repository:** [https://github.com/OSS-Group11/jjigit-ai](https://github.com/OSS-Group11/jjigit-ai)

### Community
- **Discord Server:** [Join our community](#)
- **GitHub Discussions:** [https://github.com/OSS-Group11/jjigit/discussions](https://github.com/OSS-Group11/jjigit/discussions)

## 🚀 Local Development

### Prerequisites

- Ruby 2.7 or higher
- Bundler

### Installation

1. Clone the repository:
```bash
git clone https://github.com/OSS-Group11/jjigit-website.git
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

4. Open your browser and visit:
```
http://localhost:4000/jjigit-website/
```

## 📁 Project Structure
```
jjigit-website/
├── _layouts/              # HTML layouts
│   └── default.html
├── assets/
│   └── css/
│       └── style.css      # Main stylesheet
├── index.md               # Homepage
├── features.md            # Features page
├── community.md           # Community page
├── contact.md             # Contact page
├── _config.yml            # Jekyll configuration
├── Gemfile                # Ruby dependencies
└── README.md              # This file
```

## 🎨 Website Pages

- **Homepage** (`/`) - Project introduction and mission statement
- **Features** (`/features.html`) - Detailed feature descriptions
- **Community** (`/community.html`) - Community channels and resources
- **Contact** (`/contact.html`) - Contact information and inquiry form

## 🛠️ Customization

### Changing Colors

Edit CSS variables in `assets/css/style.css`:
```css
:root {
  --primary: #4F46E5;      /* Primary color (Indigo) */
  --secondary: #06B6D4;    /* Secondary color (Cyan) */
  --accent: #F59E0B;       /* Accent color (Amber) */
}
```

### Editing Content

Modify the `.md` files directly:
- `index.md` - Homepage content
- `features.md` - Feature descriptions
- `community.md` - Community information
- `contact.md` - Contact details

### Updating Configuration

Edit site settings in `_config.yml`:
- Site title and description
- Social media links
- Project URLs

## 🌐 Deployment

This site is automatically deployed via GitHub Actions.

1. Push to the `main` branch
2. GitHub Actions builds and deploys automatically
3. Changes appear live in 1-2 minutes at [https://oss-group11.github.io/jjigit-website/](https://oss-group11.github.io/jjigit-website/)

## 🤝 Contributing to Jjigit

**Note:** This repository is for the project website only. To contribute to the Jjigit platform itself, please see the appropriate repository:

### For Code Contributions

- **Frontend Development** → [jjigit-fe](https://github.com/OSS-Group11/jjigit-fe)
  - React/Next.js development
  - UI/UX improvements
  - Frontend features

- **Backend Development** → [jjigit-be](https://github.com/OSS-Group11/jjigit-be)
  - API development
  - Database management
  - Server-side logic

- **AI/ML Development** → [jjigit-ai](https://github.com/OSS-Group11/jjigit-ai)
  - Topic generation models
  - Recommendation algorithms
  - NLP improvements

### For Website Contributions

Contributions to improve this website are welcome! 

**How to contribute:**

1. Fork this repository
2. Create a new branch (`git checkout -b feature/improve-documentation`)
3. Make your changes
4. Commit your changes (`git commit -m 'Improve documentation clarity'`)
5. Push to your branch (`git push origin feature/improve-documentation`)
6. Open a Pull Request

**What to contribute:**
- Documentation improvements
- Design enhancements
- Content corrections
- Accessibility improvements

## 👥 Team

**OSS-Group11** - [GitHub Organization](https://github.com/OSS-Group11)

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

- **Email:** contact@jjigit.io
- **GitHub Issues:** [Create an issue](https://github.com/OSS-Group11/jjigit-website/issues)
- **Discord:** [Join our community](https://oss-group11.github.io/jjigit-website/community.html)
- **Discussions:** [GitHub Discussions](https://github.com/OSS-Group11/jjigit/discussions)

## 🙏 Acknowledgments

- [Jekyll](https://jekyllrb.com/) - Static site generator
- [GitHub Pages](https://pages.github.com/) - Hosting platform
- [Apache Hadoop](https://hadoop.apache.org/) - Design inspiration
- [Django](https://www.djangoproject.com/) - Community structure inspiration

---

**Built with ❤️ by OSS-Group11**

*Empowering democratic discourse through AI-powered voting and discussion*
