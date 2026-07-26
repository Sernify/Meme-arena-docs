---
icon: user
---

# Profile & Stats

Your Profile page is your personal command center — it shows your identity, performance stats, and full prediction history.

***

## Identity

* **Wallet Address** — displayed in truncated form (first 6 and last 4 characters). Click to copy the full address.
* **Referral Code** — your unique invite code. Share it to earn referral bonuses (see [Referrals](referrals.md)).

***

## Balance & Streaks

| Field              | Description                                                             |
| ------------------ | ----------------------------------------------------------------------- |
| **Points Balance** | Your current spendable Points                                           |
| **Daily Streak**   | Consecutive days you've claimed the daily bonus                         |
| **Next Claim**     | Countdown to when your next daily bonus is available (20-hour cooldown) |

***

## Performance Stats

| Stat              | What It Means                                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------------------------- |
| **Accuracy Paid** | Number of matches where your prediction won and you received an Accuracy Pool payout                           |
| **Refunded**      | Number of predictions that received the 78% integrity refund                                                   |
| **Win Rate**      | `(Accuracy Paid) / (Total Settled Predictions)` — your overall prediction accuracy                             |
| **Net PnL**       | `Total Points Received − Total Points Staked − Total Entry Fees Paid` — your all-time profit or loss in Points |

A **positive Net PnL** means you've earned more from the Accuracy Pool than you've spent on stakes and entry fees. A **negative PnL** means you've spent more than you've earned — this is normal for new predictors still calibrating their strategy.

***

## Prediction History

The prediction history table shows every prediction you've placed, sorted newest first:

| Column      | Description                                       |
| ----------- | ------------------------------------------------- |
| **Fight**   | The fight ID — click to open the fight detail     |
| **Match**   | Which of the 3 rounds within that fight           |
| **Stake**   | How many Points you committed                     |
| **Fighter** | Which token you backed                            |
| **Status**  | `Pending` / `Pool Paid` / `78% Refunded` / `Loss` |
| **Payout**  | Points received (for winning predictions)         |

### Status Meanings

* **Pending** — the match hasn't concluded yet
* **Pool Paid** — your prediction won; payout has been credited to your balance
* **Loss** — your prediction lost; your stake went to the winning predictors
* **78% Refunded** — the fight had an integrity issue; 78% of your stake was returned
