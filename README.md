## Live URLs

- **Client:** https://platescout-rizon6.vercel.app
- **Server:** https://platescout-rizon6.onrender.com
- **Server health check:** https://platescout-rizon6.onrender.com/api/health


## Local setup

1. Clone the repo
2. Copy `server/.env.example` to `server/.env` and fill in `MONGO_URI` + `JWT_SECRET`
3. From the root: `npm install` (client) and `cd server && npm install` (server)
4. Two terminals: `npm run dev` (root, client) + `npm run dev` (server)
5. Open http://localhost:5173


## What I learned during deployment

What surprised me the most was how differently production behaves compared to local development, especially with environment variables and routing. The part that took the longest to debug was getting the frontend and backend to communicate properly after deployment. Small issues like using relative /api routes caused failures that were not obvious to fix at first. I also had to spend time reading Render and browser network logs to figure out if I was experiencing frontend issues or backend crashing. I also needed to create a new public repo outside the CS342 organization because Vercel would not let me access the repo without organization owner permissions. This created confusion about configurations and environment variables while trying to get back to the deploying on Vercel step. Next time, I would set up an API helper and verify and store environment variables more strategically, because most of the debugging was spent finding configuration errors instead of actual code bugs. I would also create a personal repo outside of an organization from the start to avoid permissions issues during deployment.