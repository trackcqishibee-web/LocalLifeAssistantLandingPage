
  # Product Launch Landing Page

  ## Running the code

  Run `npm i` to install the dependencies.

  Run `npm run dev` to start the development server.

  Run `npm run build` to create a production build.

  Run `npm run preview` to preview the production build locally.

  ## Deployment to Cloudflare Pages

  This project is configured for deployment to Cloudflare Pages using Git-based continuous deployment.

  ### Prerequisites

  - A Cloudflare account
  - A GitHub or GitLab repository with your code

  ### Setup Steps

  1. **Push your code to Git**
     - Push your code to a GitHub or GitLab repository
     - Make sure all changes are committed and pushed

  2. **Connect to Cloudflare Pages**
     - Log in to your [Cloudflare Dashboard](https://dash.cloudflare.com/)
     - Navigate to **Pages** → **Create a project**
     - Click **Connect to Git** and authorize Cloudflare to access your repository
     - Select your repository from the list

  3. **Configure Build Settings**
     - **Build command**: `npm run build`
     - **Build output directory**: `dist`
     - **Root directory**: `/` (leave empty or set to `/`)
     - **Node version**: The Node version is specified in `package.json` under `engines.node` (currently set to >=18.0.0). Cloudflare Pages will automatically detect and use this version. You can also manually select Node 18 or 20 in the dashboard if needed.

  4. **Deploy**
     - Click **Save and Deploy**
     - Cloudflare will automatically build and deploy your site
     - Your site will be available at `https://<project-name>.pages.dev`

  ### Automatic Deployments

  - Every push to your main/master branch will trigger a new production deployment
  - Pull requests will automatically create preview deployments
  - All deployments include HTTPS, CDN distribution, and are available globally

  ### Custom Domain

  - After deployment, you can add a custom domain in the Cloudflare Pages dashboard
  - Cloudflare will automatically configure DNS and SSL certificates
  