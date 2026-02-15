# StellarFantasyLeague-Backend

Backend infrastructure for Stellar Fantasy League.
Responsible for:
Oracle data submission
Match data processing
API services
Leaderboard caching
User metadata storage
Built to interact securely with Soroban on Stellar.

Architecture
src/
 ├── modules/
 │    ├── league/
 │    ├── scoring/
 │    ├── oracle/
 │    ├── users/
 │    └── leaderboard/
 ├── services/
 ├── config/
 ├── utils/
 └── main.ts



Tech Stack
NestJS
TypeScript
PostgreSQL
Redis
Axios
Soroban RPC SDK
BullMQ (job queues)

Core Responsibilities
1️⃣ Oracle Engine
Fetch match data from sports APIs
Validate results
Sign transactions
Submit scores to Soroban contract
2️⃣ Leaderboard Engine
Cache leaderboard rankings
Serve frontend API quickly
3️⃣ User Profile System
Store off-chain metadata
Referral tracking




Environment Variables
DATABASE_URL=
REDIS_URL=
SPORTS_API_KEY=
SOROBAN_RPC_URL=
ORACLE_PRIVATE_KEY=
LEAGUE_CONTRACT_ID=
SCORING_CONTRACT_ID=
REWARD_CONTRACT_ID=

Installation
git clone repo URL 
cd project folder 
npm install
npm run start:dev

Testing
npm run test
npm run test:e2e

Security
Multi-sig oracle signing (planned)
Rate-limited API endpoints
Encrypted private key storage
Role-based admin access
API Endpoints
GET /leagues
GET /leaderboard/:leagueId
POST /oracle/submit-score
GET /players
POST /referral

Deployment
Recommended:
Docker
AWS / DigitalOcean
Railway / Render
Managed PostgreSQL
