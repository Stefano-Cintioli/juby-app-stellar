Markdown

# 🏦 Juby: The Invisible Pension Protocol

![Juby Banner](https://img.shields.io/badge/Status-Hackathon%20MVP-blueviolet) ![Stellar](https://img.shields.io/badge/Built%20On-Stellar%20%7C%20Soroban-white?logo=stellar) ![World App](https://img.shields.io/badge/Mini%20App-World%20ID-black?logo=worldcoin)

**Juby** is a self-custody retirement Mini App designed for the **Stellar Genesis Track**. We bridge the gap between **World App's liquidity** and **Stellar's financial infrastructure** to create a frictionless, cross-chain savings experience for Latin American freelancers.

🔗 **Live Demo:** [Launch Juby App](https://juby-app-eth.vercel.app)

---

## 🚀 The Problem
Latin American professionals face a "Discipline Crisis". While they hold funds in crypto wallets like World App, these tools are built for spending, not saving.
* **Fragmentation:** 20M+ users uses the World App but lack access to Stellar's efficient DeFi ecosystem.
* **UX Friction:** Bridging funds and managing seed phrases prevents mass adoption of self-custody savings.

## 💡 The Solution: Invisible Cross-Chain Savings
Juby abstracts the blockchain entirely. We built a "Smart Pension Protocol" that allows users to:
1.  **Login with World ID** (Proof of Human).
2.  **Instantly generate a Stellar Wallet** (via Crossmint Account Abstraction).
3.  **Deposit USDC from Base** via "Intents" (via Rozo).
4.  **Auto-Invest** in DeFi Index Vaults on Stellar.

---

## 🛠️ Tech Stack & Architecture

This project leverages cutting-edge interoperability and abstraction tools:

### 1. 🆔 Identity & Onboarding: **World ID + Crossmint**
Instead of forcing users to manage keys, we use **World ID** for authentication.
* We extract the user's verified email from World ID.
* We pass this email to **Crossmint's API** to spin up a custodial/embedded **Stellar Wallet** instantly.
* *Result:* Invisible onboarding. The user gets a Stellar address (`G...`) without creating a seed phrase.

### 2. 🌉 Cross-Chain Liquidity: **Rozo (Intents)**
We solve the lack of CCTP on Stellar by using an Intent-based architecture.
* Users sign an "Intent" to deposit USDC on **Base** (World App Wallet).
* **Rozo's Relayer** detects this signal and releases the equivalent liquidity into the user's **Stellar Wallet**.

### 3. 💸 Yield Strategy: **DeFi Index**
Once funds land on Stellar, the Juby interface allows users to commit them to a Vault strategy (DeFi Index simulation for MVP) to generate long-term yield.

### 4. 🎨 Frontend
* **Framework:** Next.js 14 (App Router).
* **Styling:** Tailwind CSS (Mobile-first for World App integration).
* **Integration:** MiniKit (World ID SDK).

---

## 📸 Key Features (Hackathon Scope)

- [x] **Sybil-Resistant Login:** Verify unique humanity via World ID.
- [x] **Smart Wallet Generation:** Automatic Stellar account creation via Crossmint.
- [x] **Cross-Chain Bridge:** Base -> Stellar liquidity injection.
- [x] **Asset Dashboard:** View locked savings and projected growth.

---

## 💻 Getting Started

To run the development server locally:

* 1. **Clone the repository:**

   ```bash
   git clone [https://github.com/Stefano-Cintioli/juby-app-stellar.git](https://github.com/Stefano-Cintioli/juby-app-stellar.git)
   cd juby-app-stellar
   
* 2. **Install dependencies:**

```bash
npm install
# or
```bash
yarn install

* 3. **Environment Variables:**
Create a .env.local file in the root directory and add your keys (World ID App ID, Crossmint API Keys, etc.):

```bash
NEXT_PUBLIC_WLD_APP_ID=your_app_id
NEXT_PUBLIC_CROSSMINT_API_KEY=your_key


* 4. **Run the server:**

```bash
npm run dev

Open http://localhost:3000 with your browser to see the result.

**🏆 Team**

Stefano Cintioli - Product & Project Manager

Renzo Banegas - Smart Contracts & Backend (Soroban/Rozo)

Joaquín Cortez - Frontend & UX

Built with ❤️ for the Stellar Hackathon: Genesis Track.
