# SonicJS Deploy Now

A ready-to-deploy SonicJS headless CMS application for Cloudflare Workers.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/lane711/sonicjs-deploy-now)

## What is SonicJS?

SonicJS is a modern, TypeScript-first headless CMS built for Cloudflare's edge platform. It's **6x faster** than traditional Node/Express applications and deploys globally in seconds.

**[Learn more at sonicjs.com](https://sonicjs.com)**

## Quick Start

### One-Click Deploy

Click the "Deploy to Cloudflare" button above to deploy this starter in seconds. Cloudflare will:

1. Clone this repo to your GitHub account
2. Provision a D1 database and R2 bucket
3. Deploy your CMS to Cloudflare Workers
4. Set up CI/CD for future deployments

### Manual Setup

```bash
# Clone this repository
git clone https://github.com/lane711/sonicjs-deploy-now.git
cd sonicjs-deploy-now

# Install dependencies
npm install

# Start the development server
npm run dev

# Visit http://localhost:8787
```

## Project Structure

```
sonicjs-deploy-now/
├── src/
│   ├── index.ts              # Application entry point
│   └── collections/          # Your content collections
│       └── blog-posts.collection.ts
├── wrangler.toml             # Cloudflare configuration
├── package.json
└── tsconfig.json
```

## Creating Collections

Add new collections in `src/collections/` and register them in `src/index.ts`:

```typescript
import myCollection from './collections/my-collection'

registerCollections([
  blogPostsCollection,
  myCollection,  // Add your collection here
])
```

## Deployment

```bash
# Deploy to Cloudflare Workers
npm run deploy

# Apply database migrations to production
npm run db:migrate:prod
```

## Resources

- [Documentation](https://sonicjs.com/quickstart)
- [API Reference](https://sonicjs.com/api)
- [GitHub](https://github.com/lane711/sonicjs)
- [Discord Community](https://discord.gg/8bMy6bv3sZ)

## License

MIT License - see the main [SonicJS repository](https://github.com/lane711/sonicjs) for details.
