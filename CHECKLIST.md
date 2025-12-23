# Customization Checklist

Use this checklist to ensure you've customized all the placeholder content.

## Personal Information

### Header (`src/components/Header.astro`)
- [ ] Line 5: Replace `YourName` with your name

### Hero Section (`src/components/Hero.astro`)
- [ ] Line 7: Replace `Your Name` with your name
- [ ] Line 10: Replace `Creative Developer & Designer` with your title
- [ ] Lines 12-15: Update the description about yourself
- [ ] Line 22: Update GitHub URL (`https://github.com/yourusername`)
- [ ] Line 28: Update LinkedIn URL (`https://linkedin.com/in/yourusername`)
- [ ] Line 34: Update Twitter/X URL (`https://twitter.com/yourusername`)

### Projects (`src/components/Projects.astro`)
- [ ] Lines 2-25: Replace placeholder projects with your actual projects
  - Update project titles
  - Update descriptions
  - Update technology tags
  - Update project links
  - Update GitHub repository links

### Contact (`src/components/Contact.astro`)
- [ ] Line 20: Update email address (`your.email@example.com`)
- [ ] Line 31: Update location (`San Francisco, CA`)
- [ ] Line 41: Update availability status (`Open to opportunities`)

### Footer (`src/components/Footer.astro`)
- [ ] Line 8: Replace `Your Name` with your name
- [ ] Lines 10-12: Update social media links

### Page Metadata (`src/pages/index.astro`)
- [ ] Line 11: Update page title (`Your Name - Portfolio`)
- [ ] Line 12: Update meta description

### Site Configuration (`astro.config.mjs`)
- [ ] Line 11: Update site URL to your actual domain

## Optional Customizations

### Colors (`src/layouts/Layout.astro`)
- [ ] Lines 30-37: Customize color scheme (optional)

### Favicon
- [ ] Replace `/public/favicon.svg` with your own icon (optional)

## Before Deployment

### GitHub Repository
- [ ] Create a new repository on GitHub
- [ ] Update repository name in GitHub Actions workflow if needed
- [ ] Push your code:
  ```bash
  git remote add origin https://github.com/yourusername/your-repo-name.git
  git push -u origin main
  ```

### For GitHub Pages Only
- [ ] Uncomment and update lines 6-7 in `astro.config.mjs`
- [ ] Set your username and repo name

### For Vercel/Netlify
- [ ] Update `site` URL in `astro.config.mjs` after first deployment

## Testing

- [ ] Run `bun run dev` and test locally
- [ ] Check all links work
- [ ] Test contact form (after deploying to Netlify)
- [ ] Test on mobile devices
- [ ] Run `bun run build` to ensure no errors

## Post-Deployment

- [ ] Verify site is live and accessible
- [ ] Test all navigation links
- [ ] Test social media links
- [ ] Check responsiveness on different devices
- [ ] Test contact form submission (Netlify only)
- [ ] Set up custom domain (optional)
- [ ] Update README with your actual deployment URL

---

Once all items are checked, your site is ready to share with the world!
