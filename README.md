<div align="center">



### \# 🔥 ROAST FACTORY



\### \*Where Your Mouth Writes Checks Your Wallet Can Cash\*



\[!\[Live Demo](https://img.shields.io/badge/🎮\_Play\_Now-Live\_Demo-FF4500?style=for-the-badge)](https://roastfactory.vercel.app)

\[!\[Backend](https://img.shields.io/badge/⚙️\_Backend-Repository-339933?style=for-the-badge)](https://github.com/ElZech/roastfactory-backend)

\[!\[Frontend](https://img.shields.io/badge/🎨\_Frontend-Repository-0070F3?style=for-the-badge)](https://github.com/ElZech/roastfactory-frontend)



<br />



<img src="https://img.shields.io/badge/Next.js-14-black?style=flat-square\&logo=next.js" />

<img src="https://img.shields.io/badge/Node.js-18+-339933?style=flat-square\&logo=node.js\&logoColor=white" />

<img src="https://img.shields.io/badge/Socket.io-4.6-010101?style=flat-square\&logo=socket.io" />

<img src="https://img.shields.io/badge/OpenAI-GPT--4o-412991?style=flat-square\&logo=openai\&logoColor=white" />

<img src="https://img.shields.io/badge/Solana-Web3-9945FF?style=flat-square\&logo=solana\&logoColor=white" />

<img src="https://img.shields.io/badge/PostgreSQL-Supabase-4169E1?style=flat-square\&logo=postgresql\&logoColor=white" />



</div>



---



\## 🎯 What is RoastFactory?



\*\*RoastFactory\*\* is a real-time multiplayer roast battle game where players compete head-to-head in 3-round verbal combat. An AI judge (GPT-4o-mini) scores each roast on savagery, creativity, delivery, and relevance. Winners take the prize pool. Losers take the L.



> Think rap battles meets Web3 meets viral content.



---



\## 🎮 How It Works

```

1️⃣  Connect your Solana wallet

2️⃣  Choose your tier (Bronze → Diamond)

3️⃣  Get matched with an opponent

4️⃣  Battle for 3 rounds (30 seconds each)

5️⃣  AI judges your roasts in real-time

6️⃣  Winner takes 95% of the prize pool

```



---



\## 💰 Battle Tiers



| Tier | Entry | Winner Takes | Platform Fee |

|:----:|:-----:|:------------:|:------------:|

| 🥉 \*\*Bronze\*\* | 2,000 $ROAST | 3,800 $ROAST | 200 |

| 🥈 \*\*Silver\*\* | 6,000 $ROAST | 11,400 $ROAST | 600 |

| 🥇 \*\*Gold\*\* | 8,000 $ROAST | 15,200 $ROAST | 800 |

| 💎 \*\*Diamond\*\* | 10,000 $ROAST | 19,000 $ROAST | 1,000 |



---



\## 🏗️ Architecture

```

┌────────────────────────────────────────────────────────────────┐

│                        ROAST FACTORY                           │

├────────────────────────────────────────────────────────────────┤

│                                                                │

│   ┌─────────────┐         WebSocket         ┌─────────────┐   │

│   │             │ ◄───────────────────────► │             │   │

│   │   Next.js   │                           │   Node.js   │   │

│   │  Frontend   │                           │   Backend   │   │

│   │             │                           │             │   │

│   └─────────────┘                           └──────┬──────┘   │

│         │                                          │          │

│         │                    ┌─────────────────────┼─────┐    │

│         │                    │                     │     │    │

│         ▼              ┌─────▼─────┐    ┌────▼────┐│┌────▼───┐│

│   ┌──────────┐         │           │    │         │││        ││

│   │  Solana  │         │ Supabase  │    │ Upstash │││ OpenAI ││

│   │  Wallet  │         │ Postgres  │    │  Redis  │││GPT-4o  ││

│   └──────────┘         └───────────┘    └─────────┘│└────────┘│

│                                                    │          │

└────────────────────────────────────────────────────┴──────────┘

```



---



\## 📂 Repositories



| Repository | Description | Stack |

|------------|-------------|-------|

| \[\*\*roastfactory-backend\*\*](https://github.com/ElZech/roastfactory-backend) | WebSocket server, AI judging, database | Node.js, Socket.io, OpenAI |

| \[\*\*roastfactory-frontend\*\*](https://github.com/ElZech/roastfactory-frontend) | Battle UI, wallet integration, real-time client | Next.js 14, TypeScript, Tailwind |



---



\## 🤖 AI Judging System



Every roast is scored by GPT-4o-mini on four criteria:



| Criteria | What It Measures |

|----------|------------------|

| 🔥 \*\*Savagery\*\* | How brutal and cutting |

| 💡 \*\*Creativity\*\* | Originality and cleverness |

| 🎤 \*\*Delivery\*\* | Word choice, flow, impact |

| 🎯 \*\*Relevance\*\* | Staying on topic |



\*\*Total Score:\*\* 0-100 per roast



---



\## ✨ Features



\- ⚡ \*\*Real-time multiplayer\*\* - WebSocket battles with instant feedback

\- 🤖 \*\*AI-powered judging\*\* - Fair, consistent, and savage

\- 💰 \*\*Skill-based rewards\*\* - Better roasts = more $ROAST

\- 🎭 \*\*Tiered competition\*\* - Bronze to Diamond leagues

\- 📊 \*\*Stats tracking\*\* - Win/loss records, leaderboards

\- 🔐 \*\*Web3 native\*\* - Solana wallet authentication

\- 📱 \*\*Mobile responsive\*\* - Battle anywhere



---



\## 🚀 Roadmap



\- \[x] Real-time multiplayer battles

\- \[x] AI judging with GPT-4o-mini

\- \[x] Tiered prize pools

\- \[x] User stats tracking

\- \[ ] Voice mode battles

\- \[ ] Viral clip generation

\- \[ ] Tournament brackets

\- \[ ] Real $ROAST token rewards

\- \[ ] Mobile app (iOS/Android)



---



\## 🛠️ Tech Stack



\*\*Frontend:\*\* Next.js 14 • TypeScript • Tailwind CSS • Socket.io Client • Solana Wallet Adapter



\*\*Backend:\*\* Node.js • Express • Socket.io • OpenAI GPT-4o-mini



\*\*Database:\*\* Supabase (PostgreSQL) • Upstash (Redis)



\*\*Blockchain:\*\* Solana • $ROAST Token



---



\## 👨‍💻 Author



\*\*ElZech\*\* - Builder \& Creator



\[!\[GitHub](https://img.shields.io/badge/GitHub-ElZech-181717?style=flat-square\&logo=github)](https://github.com/ElZech)

\[!\[Twitter](https://img.shields.io/badge/Twitter-@YourHandle-1DA1F2?style=flat-square\&logo=twitter\&logoColor=white)](https://twitter.com/YourHandle)



---



<div align="center">



\### 🔥 Ready to Roast?



\*\*\[Play Now]( https://https://factoryapp.dev/app/builds/9881de3d-0b1b-46f0-be35-9c6a1e6cd7b3 ) \*\* • OR •\*\*(https://roastfactory.vercel.app)\*\* •



\*\*\[View Backend](https://github.com/ElZech/roastfactory-backend)\*\* •



\*\*\[View Frontend](https://github.com/ElZech/roastfactory-frontend)\*\*



<br />



\*Built with mass shipping energy\* ⚡



</div>

