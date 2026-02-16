
# DevProof — GitHub Portfolio Verifier & Score

DevProof is a portfolio-ready web app that lets users link their GitHub account, fetch public repository data, and generate a simple **Portfolio Score** with a shareable public profile page.

## ✨ Features
- 🔐 Sign-in with GitHub (OAuth)
- 🧾 Fetch GitHub profile + public repositories
- 📊 Portfolio Score (stars, forks, recency, languages)
- 🌐 Public share page: `/u/:username`
- ♻️ Manual refresh endpoint to re-calculate score

## 🧠 How It Works (High Level)
1. User signs in using GitHub OAuth.
2. The app stores the user record and OAuth tokens (securely).
3. The app calls GitHub REST API to fetch:
   - user profile
   - public repos
4. The scoring engine aggregates metrics and calculates a score (0–100).
5. The result is shown on dashboard and a public page.

## 🧰 Tech Stack
- Next.js (App Router)
- NextAuth.js (GitHub OAuth)
- Prisma ORM
- PostgreSQL (recommended) / SQLite (local)
- TailwindCSS

## 🚀 Getting Started

### 1) Clone & install
```bash
git clone https://github.com/<your-username>/devproof.git
cd devproof
npm install
