# My Personal Website

A modern, responsive personal website built with [Hugo](https://gohugo.io/) static site generator and the [Blowfish](https://blowfish.page/) theme.

## Features

- **Fast & Lightweight**: Built with Hugo for blazing-fast performance
- **Responsive Design**: Optimized for all devices and screen sizes
- **Dark/Light Mode**: Automatic theme switching with user preference support
- **SEO Optimized**: Built-in meta tags and structured data
- **Modern UI**: Clean, minimalist design powered by Tailwind CSS
- **GitHub Pages Ready**: Configured for seamless deployment

## Tech Stack

- **Static Site Generator**: [Hugo](https://gohugo.io/)
- **Theme**: [Blowfish](https://blowfish.page/)
- **CSS Framework**: [Tailwind CSS](https://tailwindcss.com/)
- **Hosting**: [GitHub Pages](https://pages.github.com/)

## Project Structure

```
├── archetypes/          # Content templates
├── assets/              # Asset files (images, CSS, JS)
├── config/              # Configuration files
├── content/             # Markdown content files
├── data/                # Data files
├── layouts/             # Custom layout templates
├── public/              # Generated static files (auto-generated)
├── static/              # Static files (copied as-is)
├── themes/blowfish/     # Blowfish theme
├── hugo.toml            # Main Hugo configuration
└── README.md            # This file
```

## Quick Start

### Prerequisites

- [Hugo Extended](https://gohugo.io/getting-started/installing/) (v0.110.0 or later)
- [Git](https://git-scm.com/)

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/phyrexxxxx/phyrexxxxx.github.io.git
   cd phyrexxxxx.github.io
   ```

2. **Start the development server**
   ```bash
   hugo server -D
   ```

3. **Open your browser**
   Visit `http://localhost:1313` to see your site

### Creating Content

1. **Create a new post**
   ```bash
   hugo new posts/my-first-post.md
   ```

2. **Create a new page**
   ```bash
   hugo new about.md
   ```

3. **Edit content**
   - Content files are located in the `content/` directory
   - Use Markdown syntax for writing
   - Configure front matter for metadata

## Customization

### Site Configuration

Edit `hugo.toml` to customize:
- Site title and description
- Base URL
- Language settings
- Theme parameters

### Theme Customization

The Blowfish theme offers extensive customization options:
- Color schemes
- Layout options
- Navigation menus
- Social links
- Analytics integration

Refer to the [Blowfish documentation](https://blowfish.page/docs/) for detailed configuration options.

### Custom Styling

- Add custom CSS in `assets/css/`
- Override theme templates in `layouts/`
- Add custom JavaScript in `assets/js/`

## Deployment

### GitHub Pages (Recommended)

This site is configured for automatic deployment to GitHub Pages:

1. **Push changes to main branch**
   ```bash
   git add .
   git commit -m "Update content"
   git push origin main
   ```

2. **GitHub Actions will automatically build and deploy**
   - The site will be available at `https://phyrexxxxx.github.io`
   - Deployment typically takes 2-5 minutes

### Manual Deployment

1. **Build the site**
   ```bash
   hugo --minify
   ```

2. **Deploy the `public/` folder**
   Upload the contents of the `public/` directory to your web server

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Support

If you have any questions or need help with the site:

- Check the [Hugo documentation](https://gohugo.io/documentation/)
- Review the [Blowfish theme docs](https://blowfish.page/docs/)
- Open an issue in this repository

## License

This project is licensed under the MIT License - see the theme's [LICENSE](themes/blowfish/LICENSE) file for details.
