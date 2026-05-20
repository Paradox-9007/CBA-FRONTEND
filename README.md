# Customer Behaviour Analysis Frontend

This repository contains the Vite + React frontend for the Customer Behaviour Analysis platform.

The frontend is responsible for:

- rendering the landing page and About sections
- showing sample replay videos and uploaded video views
- drawing shelf zones, interaction overlays, and heatmaps
- displaying the Product Overlay Board and rolling analytics state
- connecting to the private backend API for live analysis data

## Stack

- React 18
- Vite 5

## Local Development

Install dependencies:

```bash
npm install
```

Create a local `.env` file if you want to override the backend URL. The tracked template is:

```bash
.envexample
```

Example value:

```env
VITE_API_BASE_URL=http://127.0.0.1:8000
```

Start the development server:

```bash
npm run dev
```

Build for production:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## Deployment Notes

- The frontend is designed to be deployed from source.
- `node_modules/` should not be committed because hosting platforms install dependencies during build.
- `dist/` should not be committed because it is generated output from `npm run build`.
- The backend API is private and must be provided through `VITE_API_BASE_URL`.

## Repository Hygiene

Tracked source should include:

- `src/`
- `public/`
- `package.json`
- `package-lock.json`
- config files such as `vite.config.js` and `vercel.json`
- documentation and license files

Generated or machine-specific files should stay out of Git:

- `node_modules/`
- `dist/`
- local `.env`

## Backend Relationship

This frontend depends on a separate private backend repository that owns:

- model inference
- upload processing
- interaction analysis
- analytics APIs
- model assets and proprietary logic
