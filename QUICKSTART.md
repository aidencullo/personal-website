# Quick Start Guide

This guide will help you customize and deploy your personal portfolio website in under 10 minutes.

## Step 1: Customize Your Content (5 minutes)

### Basic Information

Open these files and search for the following placeholders to replace:

1. **Header** (`src/components/Header.astro`)
   - Replace `YourName` with your actual name

2. **Hero Section** (`src/components/Hero.astro`)
   - Replace `Your Name` with your name (appears twice)
   - Replace `Creative Developer & Designer` with your title/profession
   - Update the description paragraph
   - Update social media links:
     - `https://github.com/yourusername` → your GitHub
     - `https://linkedin.com/in/yourusername` → your LinkedIn
     - `https://twitter.com/yourusername` → your Twitter/X

3. **Projects** (`src/components/Projects.astro`)
   - Edit the `projects` array at the top of the file
   - Add your real projects with descriptions, tags, and links

4. **Contact** (`src/components/Contact.astro`)
   - Replace `your.email@example.com` with your email
   - Replace `San Francisco, CA` with your location
   - Update `Open to opportunities` if desired

5. **Footer** (`src/components/Footer.astro`)
   - Replace `Your Name` with your name
   - Update social links

### Optional: Change Colors

Edit `src/layouts/Layout.astro` and modify the CSS variables:

```css
--color-primary: #3b82f6;      /* Change to your brand color */
--color-secondary: #8b5cf6;     /* Change to your accent color */
```

## Step 2: Test Locally (2 minutes)

```bash
bun run dev
```

Open http://localhost:4321 and verify everything looks good.

## Step 3: Deploy to the Web (3 minutes)

### Option A: Vercel (Easiest, Recommended)

1. Go to https://vercel.com and sign in with GitHub
2. Click "Add New Project"
3. Select this repository
4. Click "Deploy"
5. Done! Your site is live at `https://yourproject.vercel.app`

### Option B: Netlify

1. Go to https://netlify.com and sign in with GitHub
2. Click "Add new site" → "Import an existing project"
3. Select this repository
4. Click "Deploy site"
5. Done! Your site is live at `https://yoursite.netlify.app`

### Option C: GitHub Pages

1. Update `astro.config.mjs`:
   ```js
   site: 'https://yourusername.github.io',
   base: '/personal-website',
   ```

2. Push to GitHub:
   ```bash
   git remote add origin https://github.com/yourusername/personal-website.git
   git push -u origin main
   ```

3. Go to repository Settings → Pages
4. Under "Source", select "GitHub Actions"
5. Wait 2-3 minutes for deployment
6. Done! Your site is live at `https://yourusername.github.io/personal-website`

## Step 4: Add a Custom Domain (Optional)

All three platforms support custom domains:

- **Vercel**: Project Settings → Domains → Add
- **Netlify**: Site Settings → Domain management → Add custom domain
- **GitHub Pages**: Settings → Pages → Custom domain

You'll need to update DNS records with your domain registrar. Each platform provides instructions.

## Common Customizations

### Change the Gradient Colors

In `src/components/Hero.astro`, find `.gradient-text` and update:

```css
background: linear-gradient(135deg, #your-color-1, #your-color-2);
```

### Add More Projects

In `src/components/Projects.astro`, add objects to the `projects` array:

```js
{
  title: "New Project",
  description: "Description here",
  tags: ["Tag1", "Tag2"],
  link: "https://project-link.com",
  github: "https://github.com/you/project"
}
```

### Modify the Hero Background

In `src/components/Hero.astro`, find `.hero` and change:

```css
background: linear-gradient(135deg, #f9fafb 0%, #e0e7ff 100%);
```

## Need Help?

- Full documentation: See `README.md`
- Astro docs: https://docs.astro.build
- Issues: Open an issue on GitHub

---

That's it! Your personal portfolio is now live on the web.
