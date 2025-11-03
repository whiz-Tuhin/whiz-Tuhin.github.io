# Deployment Instructions

This site is built with SvelteKit and deployed to GitHub Pages.

## Local Development

1. Install dependencies:
   ```bash
   npm install
   ```

2. Run the development server:
   ```bash
   npm run dev
   ```

3. The site will be available at `http://localhost:5173/`

## Building for Production

Build the static site:
```bash
npm run build
```

The built files will be in the `build/` directory.

## Deployment to GitHub Pages

The site automatically deploys to GitHub Pages when you push to the `master` branch.

The GitHub Actions workflow (`.github/workflows/ci.yml`) will:
1. Install dependencies
2. Run type checking
3. Run linting
4. Build the site
5. Deploy to the `gh-pages` branch

## Manual Deployment

If you need to deploy manually:

1. Build the site: `npm run build`
2. Push the `build/` directory to the `gh-pages` branch

## Repository Settings

Make sure GitHub Pages is configured to serve from the `gh-pages` branch in your repository settings:
- Go to Settings → Pages
- Set Source to "Deploy from a branch"
- Select the `gh-pages` branch and `/ (root)` folder
- Save

Your site will be available at: `https://whiz-tuhin.github.io/`
