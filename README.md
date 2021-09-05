# IMPORTANT: do NOT run `npm install`! This repo contains the node_modules that has patched next-server.js to induce latency to the /about page JS chunk so the bug is reproducible.

```bash
# WARNING: DO NOT RUN npm install
npm run build
npm start
```

Now visit http://localhost:3000 with Dev Tools open, and wait for the `/_next/static/chunks/pages/about-75b535cafcce005cf591.js` preloading to finish (it should take at least 5 seconds.) Once it's done, click on the link and notice how it does not work.
