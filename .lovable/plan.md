

## GitHub Pages Deployment Setup

### Changes

**1. Update `vite.config.ts`**
- Add `base: './'` to the Vite config so all asset paths are relative, working on any hosting path

**2. Create `.github/workflows/deploy.yml`**
- Add a GitHub Actions workflow that builds and deploys to GitHub Pages on every push to `main`
- Uses Node 20, runs `npm ci` and `npm run build`, then deploys the `dist` folder

### After Implementation

1. Connect your project to GitHub via **Settings > GitHub > Connect project** in Lovable
2. Go to your GitHub repo > **Settings > Pages** and set Source to **GitHub Actions**
3. Push to `main` -- your site will be live at `https://your-username.github.io/repo-name/`

