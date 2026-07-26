---
icon: arrow-right-arrow-left
---

# Matchmaking

The matchmaker is the engine that keeps the Arena running. It operates continuously, pairing eligible fighters and scheduling fights so there's always action in the arena.

***

## How Pairs Are Selected

The matchmaker runs every **30 seconds**, scanning all active fighters for eligible pairs. To be considered for a fight, a token must:

1. Be in **Active** status (not deactivated)
2. Have a **24h volume above $50,000** — ensures the token has real price action
3. Have a **recent price snapshot** — data must be fresh
4. **Not be in cooldown** — no fight in the last **1 hour**
5. **Not have fought its proposed opponent** in the last **4 hours**

***

## Pairing Criteria

Once a pool of eligible candidates is assembled, the matchmaker pairs tokens within the same league using these constraints:

| Constraint                | Limit    | Reason                                                             |
| ------------------------- | -------- | ------------------------------------------------------------------ |
| Market Cap difference     | ≤ 20%    | Fair fight — prevents a $500k cap token from fighting a $50k token |
| 24h Volume difference     | ≤ 60%    | Comparable trading activity                                        |
| Same league               | Required | Bronze fights Bronze, Diamond fights Diamond                       |
| Different deployer wallet | Required | Anti-collusion — see below                                         |

Candidates are sorted by market cap, and the matchmaker walks the list looking for the closest valid pair.

***

## Anti-Collusion

Every admitted token has its **on-chain deployer wallet** recorded. The matchmaker checks this before creating any pair.

**If two tokens share the same deployer address, they cannot be matched.**

This prevents a bad actor from:

* Deploying two tokens
* Coordinating one token to dump its volume into the other during a fight
* Profiting from a rigged outcome at the expense of predictors

***

## Scheduling & Staggering

Once a pair is confirmed, the fight is **scheduled** (not immediate). The matchmaker staggers fight starts across the arena:

* Minimum **3.5 minutes** between consecutive fight starts
* **±45 seconds** of random jitter applied to each scheduled time

This ensures that at any given moment, there are multiple open betting windows across different fights and leagues — users are never stuck waiting for the next window to open.

***

## Fight Lifecycle States

```
scheduled  →  active  →  completed
     ↑              (scored at end of each match)
     └── cooldown (1 hour before token re-enters matchmaking)
```

| State       | Description                                                 |
| ----------- | ----------------------------------------------------------- |
| `scheduled` | Fight is confirmed, betting window opens 2 min before start |
| `active`    | Round is live, no new predictions accepted                  |
| `completed` | All 3 matches finished, Accuracy Pools settled              |
