# 1. AI Tool Builder: something people use every day and pay for every month

## The problem
Freelance devs lose about 20–30% of their billable time to unpaid scope creep, such as "can you just add…". Scoping is also slow: a proposal takes 2–4 hours to write. Both problems cost money directly, so the tool is easy to justify paying for.

## The AI capability that makes it useful
1. **Notes → Proposal (in 90 seconds).** Paste call notes, a transcript, or an email thread. The tool extracts deliverables, assumptions, exclusions, milestones, and an estimate range, and writes a clean proposal in your own template and voice.
2. **Scope Watch (the daily habit).** Forward client emails or connect Gmail and Slack. Each new request is classified against the signed scope as *in scope*, *ambiguous*, or *out of scope*. The tool cites the clause it used.
3. **One-click Change Order.** For out-of-scope requests, it drafts a polite change order with a price and timeline impact, based on your hourly rate and past estimates.
4. **Estimate calibration.** It compares estimates with actual tracked time (Toggl/Harvest import), so each new estimate is more accurate than the last. This is a moat that grows with each user's history.

Why this is more than a novelty: it saves time you can measure, and it recovers revenue you can measure. Every Scope Watch catch shows a dollar figure.

## An interface that justifies paying for it
- **Dashboard hero number:** "$X recovered this month" (the total value of accepted change orders).
- **Project view:** signed scope on the left, request feed on the right, colour-coded by status.
- **Proposal editor:** Notion-like blocks, a branded PDF/web link, e-signature, and a deposit link through Stripe.
- **Keyboard-first and fast:** under 200 ms interactions, with dark and light themes. It should look like something a professional would send to a client.

## Pricing model for recurring revenue
| Plan | Price | For | Limits |
|------|-------|-----|--------|
| Free | $0 | Try it | 2 proposals/mo, no Scope Watch |
| Solo | $29/mo ($290/yr) | Freelancers | Unlimited proposals, 5 active projects in Scope Watch |
| Pro | $59/mo ($590/yr) | Busy freelancers | Unlimited projects, Gmail/Slack auto-ingest, calibration, custom branding |
| Studio | $149/mo ($1,490/yr) | Agencies ≤10 seats | Team seats, shared templates, client portal, API |

- Charge per active project in Scope Watch, not per AI call. This is the metric that grows with the user's business.
- Annual plan gives 2 months free. Push it after the first recovered change order.

## First 10 paying customers in week 1
1. **Days −14 to 0:** DM 50 freelancers you already know, from past gigs, GitHub, and Upwork contacts. Ask for a 15-minute call about scope creep, not a sales pitch.
2. **Concierge offer:** "Send me your messiest client thread and I'll return a proposal plus change order in 24h, free." Do it with the tool yourself, then hand them the login.
3. **Founding member deal:** $19/mo locked in for life for the first 25 users (the Pro features). Payment is required to get in.
4. Post a real before/after (notes → proposal) in r/freelance, r/webdev, Indie Hackers, and freelance Slack/Discord communities.
5. Math: 50 DMs → about 20 calls → about 10 paid. Personal outreach usually converts 15–25% of calls, so 10 is a reachable target.
