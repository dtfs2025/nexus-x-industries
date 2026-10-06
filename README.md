# Nexus X Industries

Complete standalone corporate website featuring NCI, DTFS and NexCare, the founder’s message and portrait, product logos, responsive layouts and an automatic hero carousel.

## Run locally

Install Node.js 22.13 or newer, then run from this folder:

```sh
npm ci
npm run dev
```

Open the local URL printed by Vite. To build and check the production output:

```sh
npm run build
npm run preview
```

## Deploy

Import this repository into Vercel or Netlify. The included configuration uses `npm run build` and publishes `dist`. For Cloudflare Pages, choose the same build command and output folder, with Node.js 22 or newer. For ordinary web hosting, upload the contents of `dist` to the domain’s web root. No backend, database, API keys or environment variables are required.

This standalone export uses React, TypeScript, Vite and plain CSS. It preserves the site’s current visual design and content while removing the original host-specific runtime. Deployment is intended at a domain root; GitHub Pages project subpaths need asset path configuration first. A private GitHub repository does not automatically make a deployed website private: configure access with the chosen host if required.

## Content and assets

- `src/App.tsx`: all site content, product links and carousel logic.
- `src/styles.css`: responsive design and animations.
- `public/`: Nexus X, DTFS, NexCare and NCI logos, founder portrait, hero background and favicon.
- `index.html`: page title and search description.

Contact links use `info@nexusind.com`. DTFS links to `https://www.dtfsglobal.com`; NexCare links to `https://www.nexcareglobal.com`. Email buttons open the visitor’s email app; this project does not provision an email mailbox or submit forms to a server.

The hero advances every five seconds and has manual navigation and pause/play controls. Reduced-motion preferences disable automatic rotation and animation. Product descriptions express the existing roadmap and do not imply that all capabilities are already available.

## Push to a new private GitHub repository

With Git and GitHub CLI installed, run inside this folder:

```sh
gh auth login
git init -b main
git add .
git commit -m "Initial Nexus X Industries website"
gh repo create nexusx212/nexus-x-industries --private --source=. --remote=origin --push
```

If that name is already taken, choose a new repository name. Never commit `node_modules`, credentials or `.env` files. The included Git ignore rules exclude these.

## Ownership

Company branding, supplied portraits and website content belong to their respective owners. No open-source license is granted for those assets by this export. Dependency licenses remain with their authors.
