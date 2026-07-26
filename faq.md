# FAQ

---

## General

### What is Meme Arena?

Meme Arena is a real-time prediction platform on Solana where meme tokens fight each other in live, 5-minute head-to-head battles. Users predict which token will outperform and earn Points from the Accuracy Pool when correct.

### Is this gambling?

Predictions in Meme Arena are based on live on-chain market data — not random numbers or house-set odds. The outcome is determined by real trading activity during each 5-minute round. Whether this constitutes gambling depends on your jurisdiction. Check your local laws.

### Does Meme Arena have a token?

Not yet. The **ARENA token** is in development. See [The ARENA Token](token/arena-token.md). Accumulating Points now may benefit you at launch.

### Is Meme Arena audited?

Security and audit information will be published on official channels. Smart contract components (when deployed) will be open source and audited before launch.

---

## Fights & Predictions

### Can I predict on multiple matches at once?

Yes. Each match is independent. You can have open predictions across multiple fights and leagues simultaneously.

### Can I cancel a prediction after placing it?

No. Once confirmed and the betting window closes, predictions are locked. There are no cancellations.

### What happens if there are no predictors on one side?

If there are zero predictors on the losing side, the winning side retains their stakes (no pool to win from). The Accuracy Pool requires both sides to have predictors to generate a meaningful payout.

### How quickly are payouts credited?

Accuracy Pool payouts settle within seconds of a round ending. Points appear in your balance automatically — no manual claim needed.

### What is the 78% refund?

If a fight is flagged for a data integrity issue (missing price snapshots, failed data fetch), the fight cannot be scored fairly. All predictors receive **78% of their original stake** back. The 15 pt entry fee is not refunded.

---

## Tokens & Fighters

### How are tokens admitted to the Arena?

Automatically, via a continuous discovery pipeline from DexScreener, PumpPortal, and PumpFun. Every token must pass security checks (revoked mint/freeze authority, minimum liquidity and volume, pair age, meme signal heuristic). See [Fighters](arena/fighters.md) for full criteria.

### Can I submit a token to be added?

Token admission is fully automated during the current phase. Manual submissions are not available.

### Why did a token disappear from the Arena?

Tokens are deactivated if their 24h volume or liquidity falls below the retention thresholds ($500 each). Fight history is preserved; the token can return if metrics recover.

### Can the same two tokens fight each other repeatedly?

Not within 4 hours. Each specific pair has a 4-hour cooldown after a fight, and each token individually has a 1-hour cooldown.

---

## Points & Account

### My Points balance seems wrong. What happened?

Check your prediction history on the Profile page. Points spent on stakes and entry fees are itemized there. Contact support with your wallet address if you believe there is an error.

### Can I buy Points?

Currently, Points can only be earned through predictions, daily bonuses, and referrals. Purchasing Points is not available.

### What happens to my Points when the ARENA Token launches?

Active users' Points balances will be considered for token allocation at launch. Full details (snapshot timing, conversion rate, eligibility) will be announced in advance. See [The ARENA Token](token/arena-token.md).

### Can I have multiple accounts?

One wallet = one account. You can connect a different wallet to create a separate account, but Points and history are not transferable between accounts.

---

## Wallet & Security

### What wallets are supported?

Any Solana wallet supporting message signing: Phantom, Solflare, and WalletConnect-compatible wallets.

### Does connecting my wallet cost SOL?

No. Connecting your wallet only requires signing a message — not a transaction. No SOL is spent.

### Is my private key ever exposed?

Never. The authentication flow only uses your wallet to sign a message. Your private key stays in your wallet at all times.

### What should I do if I think my account was compromised?

Immediately disconnect your wallet from Meme Arena via the Profile page. If your wallet itself is compromised, move assets to a new wallet. Contact support with your original wallet address.
