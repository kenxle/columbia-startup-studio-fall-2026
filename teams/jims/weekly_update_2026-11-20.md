# Weekly Update: SettleWise, November 20, 2026

## Accountability: what we did

**Build:** This week went into making users countable, which was last week's Analyze plan.

- **Signup and activation tracking:** Cleaned up Google Analytics to a single tag and removed an old, unused Firebase Analytics property. Added four events: `signup_started` (which signup button was clicked), `sign_up` (a new account was created), `comparison_viewed` (a user compared their apartments) and `analysis_requested` (a user asked for the AI summary).
- **Public metrics endpoint:** `/api/metrics` now reports signups and active users straight from our database, with team and test accounts excluded. The link is in `api-metrics.md`.
- **Meta Pixel:** Installed for ad reporting only. It mirrors the same events and sends no names, emails or page details.
- **Security update:** Upgraded Next.js to 16.4.6.

**Grow:** Launched our first paid experiment, a $100 Meta ad, on Thu Nov 19. It's in the Housing ad category, targets NYC, runs 7 days and sends people to the homepage with UTM tags. We wrote the pass/fail bar before launch (`hw8-ad-experiment/experiment_card.md`). We also created a SettleWise Facebook Page, linked to our Instagram, with a tracked link to the site. We planned last week to add links to our Reddit posts, but we didn't post any. That's now part of this week's cold start plan.

**Demand strategy:** We started publishing blog posts. Before this, our site had a blog tab but no posts.

**Analyze:**

- We tested tracking end to end. A fresh Google account signed up through a UTM link, and every event showed up in Google Analytics Realtime and in Meta Events Manager.
- Google Analytics for Nov 13–19 shows 61 sessions: 15 Direct, 14 Organic Search, 13 Referral, 17 Paid Social and 1 Organic Social.
- The 17 Paid Social sessions came on the ad's first afternoon. Most lasted 0–1 seconds, which looks like Meta's ad review systems, not people.
- The 3 `sign_up` events that week appear to be our own 2 test accounts.
- `sign_up` isn't marked as a key event in Google Analytics yet, so the "Key events" column still reads 0.

**Research:** We didn't run new research sessions. We wrote our HW9 cold start plan and backlog from the 5 usability sessions (Nov 5–6) and our GA data (see `hw9-ad-result-and-cold-start/`).

## Planning: what we're doing next

**Build:** Backlog #1: a 10–15 second looping video showing the Saving shortcut working on a real StreetEasy listing, plus a "Can't see your bookmarks bar?" tip. All 5 testers struggled to add a listing.

**Grow:** Follow the cold start plan (`hw9-ad-result-and-cold-start/cold-start-strategy.md`):

- 10 helpful comparison replies in r/NYCapartments, r/AskNYC and r/columbia
- 25 personal messages to classmates moving for spring, our testers and friends of our interviewees
- book a room by Wed Nov 25 for a "Shortlist Night" in the week of Dec 7–11

The Meta ad keeps running, untouched, until Thu Nov 26.

**Analyze:** Mark `sign_up` as a key event and switch our team-traffic filter from Testing to Active. On Nov 26, read the ad result once against the bar in the experiment card, and report it with a Google Analytics screenshot.

**Research:** Ask every new signup from outreach where they heard about us and where they got stuck.

## Current User Count

17 signups, 6 active (did the core action), from `/api/metrics` on Nov 20 with team accounts excluded. Last week we reported 0 because we had no way to count accounts. The endpoint now counts them directly. Almost all of these users are people we know, not strangers from a channel we can repeat.

## Issues and Blockers

- The ad is delivering slowly: $0.11 spent and 1 click on day 1. That's common for a new ad account in the Housing category. If it stays slow, we may get far fewer than the ~166 clicks we planned for, and the result could be UNCLEAR. We aren't changing the ad during the test.
- Adding a listing with the Saving shortcut is still the hardest step for new users.
- Thanksgiving week leaves less time for outreach.
