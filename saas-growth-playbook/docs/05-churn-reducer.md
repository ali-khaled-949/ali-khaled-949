# 5. Churn Reducer: keeping users after the first month

## Onboarding that shows value in the FIRST SESSION
Goal: **first proposal generated within 5 minutes** of sign-up (the "aha" moment).
1. **Skip the empty state.** The first screen says "Paste notes from your last client call (or try our sample)."
2. **Generate the proposal live** while they watch, then edit it inline. They leave with something they can use.
3. **Import their rate and a past project** (a 30-second form) so the estimate feels personal.
4. **Plant the habit hook:** "Forward client emails to `you@in.scopeguard.app` and we'll watch for scope creep." This setup step matters most for retention.
5. Checklist (4 items, progress bar): Proposal ✓ → Rate set → Scope Watch connected → Send to a client.

## Feature that makes it part of their routine
**Daily Scope Digest (8 am):** a short email or Slack message such as "3 new client requests: 2 in scope, 1 ⚠ out of scope, with a change order ready ($360)." One tap sends it.
It fits into something they already do every day (reading client messages), and each out-of-scope catch shows money.
Also: a weekly time-vs-estimate check, so every project improves future estimates.

## Early-warning system for users likely to cancel
Health score (0–100), recalculated daily:

| Signal | Weight |
|--------|--------|
| No Scope Watch connected by day 3 | −25 |
| No login in 7 days | −20 |
| 0 proposals sent to clients | −20 |
| No active projects | −15 |
| Visited billing/cancel page | −30 |
| Accepted change order this month | +25 |
| Invited teammate or referred a user | +15 |

Automated plays:
- **Score 50–70:** in-app tip plus an email with a 2-minute Loom showing the feature they haven't used.
- **Score < 50:** a personal email from the founder: "Want me to set up your first project with you?" (15-minute call).
- **Cancel flow:** ask why. Between projects → offer the $5/mo **pause**. Too expensive → downgrade or 50% off for 2 months. Missing feature → log it and offer early access.
- **Failed payments:** dunning with 3 retries, a card-update email on days 1, 3, and 7, and in-app banners. This alone recovers about 30–40% of involuntary churn.

Implementation: product events (PostHog or Segment) → a nightly job computes the score → sends by status (Customer.io or Loops) + a Slack alert to the founder for accounts under 50.

## Realistic 30-day churn reduction estimate
Baseline assumption: early-stage monthly churn of about **10–12%**.
| Change | Expected effect |
|--------|-----------------|
| Onboarding to first value in 5 min | −2 to −3 pts |
| Scope Watch habit + daily digest | −1 to −2 pts |
| Pause/downgrade in the cancel flow | −1 to −2 pts (saves 15–25% of cancel attempts) |
| Dunning fixes | −0.5 to −1 pt |

**Realistic result within 30 days: churn drops from about 11% to about 7–8%** (roughly a 25–35% relative reduction). Getting under 5% usually takes 2–3 months, as the habit features compound and annual plans increase.
