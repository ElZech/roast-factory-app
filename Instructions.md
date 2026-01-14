---

## Quick Start (Frontend Only)

### 1. Install Dependencies

```bash
npm install
```

### 2. Create Environment File

```bash
cp .env.example .env.local
```

### 3. Run Development Server

```bash
npm run dev
```

Open http://localhost:3000

---

## What Works Out of the Box

- Homepage with UI
- Wallet connection (Phantom, Solflare)
- ROAST token balance display (if connected wallet holds ROAST)
- Leaderboard page (mock data)
- Clips page (mock data)
- Profile page
- Battle UI flow (simulated - no real matchmaking)

---

## What Needs Backend Setup

The following features require additional backend infrastructure:

### 1. Real-Time Battles
**Requires**: WebSocket server (Socket.io)

The battle matchmaking and real-time communication needs a Socket.io server. Current flow uses simulated timeouts.

**To implement**:
- Set up Node.js server with Socket.io
- Handle events: `battle:matched`, `battle:round_start`, `battle:roast_submitted`, etc.
- Update `NEXT_PUBLIC_WS_URL` in `.env.local`

### 2. AI Judging
**Requires**: OpenAI API key

The roast scoring uses AI to judge savagery, creativity, delivery, and relevance.

**To implement**:
- Get API key from https://platform.openai.com
- Add to backend server (NOT in frontend .env - keep server-side only)
- Create API endpoint that calls OpenAI and returns scores

### 3. User Data & Leaderboards
**Requires**: PostgreSQL database

Store user profiles, battle history, and leaderboard rankings.

**To implement**:
- Set up PostgreSQL (Supabase, Neon, or Railway recommended)
- Create tables for users, battles, rounds, clips
- Add `DATABASE_URL` to backend environment

### 4. Matchmaking Queue
**Requires**: Redis

Fast matchmaking queue for pairing players by tier.

**To implement**:
- Set up Redis (Upstash recommended for serverless)
- Implement queue logic in backend
- Add `REDIS_URL` to backend environment

### 5. Voice Recording & Clips
**Requires**: Object storage (Cloudflare R2, AWS S3)

Store voice recordings and generated video clips.

**To implement**:
- Set up Cloudflare R2 or S3 bucket
- Configure CORS for your domain
- Add storage credentials to backend environment

---

## Environment Variables Explained

### Frontend (in `.env.local`)

```env
# Solana RPC - can use public or get a dedicated one from Helius/QuickNode
NEXT_PUBLIC_SOLANA_RPC_URL=https://api.mainnet-beta.solana.com

# Network - mainnet-beta for production, devnet for testing
NEXT_PUBLIC_SOLANA_NETWORK=mainnet-beta

# ROAST token address - already set
NEXT_PUBLIC_ROAST_TOKEN_MINT=GRv23yBYo1fMqDY8Ws2LqjwHoLx4TGUqYi7KfCDkBAGS

# Your API server URL (when you build one)
NEXT_PUBLIC_API_URL=https://api.yourdomain.com

# Your WebSocket server URL (when you build one)
NEXT_PUBLIC_WS_URL=wss://ws.yourdomain.com
```

### Backend (keep these server-side only, NEVER in frontend)

```env
DATABASE_URL=postgresql://...
REDIS_URL=redis://...
OPENAI_API_KEY=sk-...
CLOUDFLARE_R2_ACCESS_KEY=...
CLOUDFLARE_R2_SECRET_KEY=...
```

---

## Deploying the Frontend

### Vercel (Recommended)

1. Push code to GitHub
2. Import project in Vercel
3. Add environment variables in Vercel dashboard
4. Deploy

```bash
npm run build  # Test build locally first
vercel deploy --prod
```

### Other Platforms

Works on Netlify, Railway, or any platform that supports Next.js.

---

## File Structure

```
roastpush/
├── src/
│   ├── app/                 # Next.js pages
│   │   ├── page.tsx         # Homepage
│   │   ├── battle/          # Battle page
│   │   ├── leaderboard/     # Leaderboard page
│   │   ├── clips/           # Clips page
│   │   └── profile/         # Profile page
│   ├── components/
│   │   ├── battle/          # Battle-specific components
│   │   ├── wallet/          # Wallet integration
│   │   ├── shared/          # Shared components
│   │   └── ui/              # Base UI components
│   ├── hooks/               # React hooks
│   ├── config/constants.ts  # Token address, fee config
│   ├── lib/utils.ts         # Utility functions
│   └── types/               # TypeScript types
├── public/                  # Static assets
├── .env.example             # Environment template
├── package.json
└── README.md
```

---

## Key Files to Know

| File | Purpose |
|------|---------|
| `src/config/constants.ts` | Token address, battle tiers, fee percentages |
| `src/app/providers.tsx` | Wallet adapter setup |
| `src/hooks/useTokenBalance.ts` | Fetches ROAST balance |
| `src/components/battle/BattleArena.tsx` | Main battle UI |

---

## Customization

### Change Token
Edit `src/config/constants.ts`:
```ts
export const ROAST_TOKEN_MINT = new PublicKey("YOUR_TOKEN_MINT");
```

### Change Battle Tiers
Edit `src/config/constants.ts`:
```ts
export const BATTLE_TIERS = {
  Bronze: { entry: 10, color: "#CD7F32" },
  Silver: { entry: 50, color: "#C0C0C0" },
  // ...
};
```

### Change Platform Fees
Edit `src/config/constants.ts`:
```ts
export const PLATFORM_FEE_PERCENTAGE = 5;  // 5% of prize pools
export const TIP_FEE_PERCENTAGE = 2;       // 2% of tips
```

---

## Questions?

This frontend is ready to use. The mock data lets you demo the full UI flow. To make it fully functional, you'll need to build or connect a backend for real-time battles, AI judging, and data persistence.
