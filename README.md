# Automated SEO & Performance Audit SaaS

An automated SEO and performance audit tool that generates detailed reports on website quality metrics. Users enter a URL and receive comprehensive analysis on SEO, accessibility, performance, and best practices.


## Tech Stack

### Frontend
- **Framework** - Vite + ReactTS
- **Styling** - Tailwind CSS
- **Charrts** - Recharts
- **Routing** - React Router
- **Hosting** - GitHub Pages

### Backend
- **Serverless Functions** - Vercel/Netlify Functions
- **Primary API** - Google PageSpeed Insights API
- **Secondary API** - Lighthouse CI

### Data & Storage
- **MongoDB/PostgreSQL**  - Atlas/Supabase
- **Caching** - Upstash Redis


## Development ethos

Single codebase with frontend and serverless functions, minimal dependencies and progressive enhancement

### Project Structure
```
├── api/
├── public/
├── src/
│   ├── components/
│   ├── hooks/
│   ├── pages/
│   ├── services/
│   ├── types/
│   └── utils/
├── README.md
├── package.json
└── vite.config.js
```

## Implementation plan

### Phase 1 - Project Setup
1. Initialise Vite React + TypeScript project
2. Install dependencies (React Router, Recharts, Tailwind CSS)
3. Configure GitHub Page deployment in `vite.config.js`
4. Set up basic project structure

### Phase 2 - Frontend
1. Create input form for URL entry
2. Implement results display components
3. Add loading states and error handling
4. Create basic chart components for data visualisation

### Phase 3 - Backend integration
1. Set up serverless functions on Vercel/Netlify
2. Implement API route to call PageSpeed Insights
3. Create data transformation utilities to format API responses
4. Connect frontend to backend API

### Phase 4 - Additional Features
1. Implement result caching with Upstash Redis
2. Add basic history storage with MongoDB/Supabase
3. Create shareable report links
4. Add simple authentication with Next-Auth

### Phase 5 - Polish & Deployment
1. Optimize performance and bundle size
2. Add responsive design improvements
3. Test across different websites
4. Final deployment to GitHub Pages

```javascript
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

export default defineConfig({
    plugins: [react()],
    base: '/seo-audit/',
    build: {
        outDir: 'dist',
    },
})
```