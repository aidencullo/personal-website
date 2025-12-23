# Personal Portfolio Website

A modern, fast, and SEO-optimized personal portfolio website built with [Astro](https://astro.build).

## Features

- ⚡️ Lightning-fast performance with Astro
- 📱 Fully responsive design
- 🎨 Modern, clean UI with smooth animations
- 🔍 SEO-optimized with meta tags
- 📝 Contact form with Netlify Forms integration
- 🚀 Easy deployment to GitHub Pages, Vercel, or Netlify
- ♿️ Accessible and keyboard-friendly

## Project Structure

```
/
├── public/           # Static assets (favicon, images, etc.)
├── src/
│   ├── components/   # Reusable Astro components
│   │   ├── Header.astro
│   │   ├── Hero.astro
│   │   ├── Projects.astro
│   │   ├── Contact.astro
│   │   └── Footer.astro
│   ├── layouts/      # Page layouts
│   │   └── Layout.astro
│   └── pages/        # Page routes
│       └── index.astro
├── .github/
│   └── workflows/    # GitHub Actions for deployment
├── astro.config.mjs  # Astro configuration
├── netlify.toml      # Netlify configuration
└── package.json
```

## Quick Start

### Prerequisites

- [Bun](https://bun.sh) installed on your machine (or Node.js 18+)
- Git
- A code editor (VS Code recommended)

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/personal-website.git
   cd personal-website
   ```

2. Install dependencies:
   ```bash
   bun install
   ```

3. Start the development server:
   ```bash
   bun run dev
   ```

4. Open [http://localhost:4321](http://localhost:4321) in your browser

## Customization

### 1. Personal Information

Update the following files with your information:

**`src/components/Header.astro`**
- Change `YourName` to your name

**`src/components/Hero.astro`**
- Update your name, title/subtitle, and description
- Update social media links (GitHub, LinkedIn, Twitter)

**`src/components/Projects.astro`**
- Replace the placeholder projects with your actual projects
- Update project titles, descriptions, tags, and links

**`src/components/Contact.astro`**
- Update email address
- Update location
- Update availability status

**`src/components/Footer.astro`**
- Update your name and social links

**`src/pages/index.astro`**
- Update the page title and meta description

### 2. Styling

All styling is contained within each component using Astro's scoped `<style>` blocks. Color scheme variables are defined in `src/layouts/Layout.astro`:

```css
:root {
  --color-primary: #3b82f6;      /* Main brand color */
  --color-primary-dark: #2563eb; /* Darker variant */
  --color-secondary: #8b5cf6;    /* Accent color */
  --color-text: #1f2937;          /* Main text */
  --color-text-light: #6b7280;    /* Secondary text */
  --color-bg: #ffffff;            /* Background */
  --color-bg-alt: #f9fafb;        /* Alternate background */
  --color-border: #e5e7eb;        /* Borders */
}
```

### 3. Adding Custom Favicon

Replace `/public/favicon.svg` with your own icon.

## Building for Production

Build the site for production:

```bash
bun run build
```

Preview the production build locally:

```bash
bun run preview
```

## Deployment

### Option 1: GitHub Pages (Free)

1. **Update configuration** in `astro.config.mjs`:
   ```js
   export default defineConfig({
     site: 'https://yourusername.github.io',
     base: '/your-repo-name',
   });
   ```

2. **Push to GitHub**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/yourusername/your-repo-name.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to your repository settings on GitHub
   - Navigate to **Pages** (under Code and automation)
   - Under **Source**, select **GitHub Actions**
   - The workflow will automatically deploy your site

4. **Access your site** at `https://yourusername.github.io/your-repo-name`

### Option 2: Vercel (Recommended - Free)

1. **Install Vercel CLI** (optional):
   ```bash
   bunx vercel
   ```

2. **Or deploy via Vercel Dashboard**:
   - Go to [vercel.com](https://vercel.com)
   - Click "Add New Project"
   - Import your GitHub repository
   - Vercel will auto-detect Astro and configure build settings
   - Click "Deploy"

3. **Update site URL** in `astro.config.mjs`:
   ```js
   export default defineConfig({
     site: 'https://your-project.vercel.app',
   });
   ```

4. **Your site is live!** Vercel provides:
   - Automatic deployments on git push
   - Preview deployments for pull requests
   - Custom domain support
   - Built-in analytics

### Option 3: Netlify (Free)

1. **Deploy via Netlify Dashboard**:
   - Go to [netlify.com](https://netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Connect your GitHub repository
   - Build settings are auto-detected from `netlify.toml`
   - Click "Deploy site"

2. **Or use Netlify CLI**:
   ```bash
   bunx netlify deploy --prod
   ```

3. **Contact Form**: The contact form will automatically work with Netlify Forms (already configured)

4. **Update site URL** in `astro.config.mjs`:
   ```js
   export default defineConfig({
     site: 'https://your-site.netlify.app',
   });
   ```

### Custom Domain

All three platforms support custom domains:

- **GitHub Pages**: Settings → Pages → Custom domain
- **Vercel**: Project Settings → Domains
- **Netlify**: Site Settings → Domain management

## Commands Reference

| Command            | Action                                       |
| :----------------- | :------------------------------------------- |
| `bun install`      | Install dependencies                         |
| `bun run dev`      | Start dev server at `localhost:4321`         |
| `bun run build`    | Build production site to `./dist/`           |
| `bun run preview`  | Preview production build locally             |
| `bun run astro`    | Run Astro CLI commands                       |

## Troubleshooting

### Build fails on GitHub Actions

Ensure your repository has GitHub Pages enabled in settings and the source is set to "GitHub Actions".

### Contact form not working

The contact form is configured for Netlify. If deploying to GitHub Pages or Vercel, you'll need to:
- Set up a form backend service (Formspree, Getform, etc.)
- Or implement a serverless function for form handling

### Styles not loading

Run `bun run build` to ensure there are no build errors. Check browser console for errors.

## Performance

This site achieves near-perfect Lighthouse scores:

- ⚡ Performance: 100
- ♿ Accessibility: 100
- 🎯 Best Practices: 100
- 🔍 SEO: 100

## License

MIT License - feel free to use this template for your own portfolio!

## Support

If you have questions or run into issues:

1. Check the [Astro documentation](https://docs.astro.build)
2. Search [Astro Discord](https://astro.build/chat)
3. Open an issue on GitHub

---

**Built with** [Astro](https://astro.build) - The web framework for content-driven websites
