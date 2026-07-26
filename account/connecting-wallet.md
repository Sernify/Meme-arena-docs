---
icon: wallet
---

# Connecting Your Wallet

Meme Arena uses **Solana wallet authentication** — no email, no password, no KYC. Your wallet address is your identity.

***

## Supported Wallets

Any Solana wallet that supports message signing works with Meme Arena:

* **Phantom** — [phantom.app](https://phantom.app) _(most popular)_
* **Solflare** — [solflare.com](https://solflare.com)
* Any **WalletConnect-compatible** Solana wallet

{% hint style="success" %}
You do not need to send any SOL to connect. Connecting your wallet is free — it only requires signing a message to prove ownership.
{% endhint %}

***

## How to Connect

1. Click **"Enter Arena"** in the top-right corner (or **"Login"** on mobile)
2. Select your wallet from the modal
3. Your wallet app will prompt you to **sign a message** — this is not a transaction. No SOL is spent
4. Once signed, your account is created or restored automatically
5. Your truncated wallet address and Points balance appear in the nav bar

***

## What Happens Behind the Scenes

Authentication uses a **cryptographic signature flow**:

```
1. Server generates a unique, time-limited nonce for your wallet address
2. Your wallet signs the nonce using your private key
3. Server verifies the signature using your public key (wallet address)
4. If valid → session created, you are logged in
```

Your private key **never leaves your wallet**. The platform only ever sees your public wallet address and the signature.

***

## Disconnecting

Go to your **Profile** page and click **Disconnect**. This clears your server session and local state.

Your Points balance, history, and referral code are all preserved and tied to your wallet address — reconnect at any time.

***

## Security Notes

{% hint style="danger" %}
* Always verify you are on the correct domain before signing any message
* Meme Arena will **never** ask you to sign a **transaction** that spends SOL or tokens just to log in
* If a "connect" prompt asks you to approve a spending transaction, do **not** approve — that is not the login flow
{% endhint %}
