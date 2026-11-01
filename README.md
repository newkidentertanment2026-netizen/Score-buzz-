# ScoreBuzz — Worldwide Cricket Website

A responsive blue-and-white website starter with a Node/Express backend. It is prepared for worldwide cricket coverage: IPL, BBL, PSL, WPL, international and domestic cricket.

## Important status
- The website currently uses clearly labelled **illustrative demo data**.
- No live cricket API is connected yet.
- Scorecards, ball-by-ball commentary, playing XIs, points tables, player statistics, news and notifications are planned next modules, not active data feeds.
- Before publishing commercial cricket data, check the provider's licensing and redistribution terms. An API key alone does not necessarily grant commercial display rights.

## Run locally
1. Install Node.js (LTS).
2. Extract this ZIP.
3. Open a terminal in the extracted folder.
4. Run `npm install`
5. Copy `.env.example` to `.env`.
6. Run `npm start`
7. Open `http://localhost:3000`

## Connect a cricket API
1. Choose a provider and review worldwide coverage, rate limits, update delay and commercial redistribution permission.
2. Put credentials in `.env` only. Never expose API keys in `public/` JavaScript.
3. Implement the provider request inside `fetchLiveMatches()` in `server.js`.
4. Map provider responses into the normalized match object used by the frontend:
   `{ id, status, tournament, teams: [teamA, teamB], scores: [scoreA, scoreB], detail, format }`
5. Test API quota usage and failure handling before launch.

## Project structure
- `server.js` — backend and API route
- `public/index.html` — website layout
- `public/styles.css` — responsive blue/white design
- `public/app.js` — match filtering and rendering
- `.env.example` — safe configuration template

## Next build stages
1. Connect and validate a free API.
2. Add match detail pages: scorecard, commentary and playing XI.
3. Add fixtures, results, series pages and points tables.
4. Add player profiles, statistics and news workflow.
5. Add alerts, SEO, analytics, deployment and later Android app.
