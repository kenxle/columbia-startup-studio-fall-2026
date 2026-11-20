# Weekly Update: Aditya (Gable), November 20, 2026

## Accountability: what we did

- **Build:** Shipped to gable.fit this week: a "Sign up to see your matches" step on search (so accounts are our signup), hearts on real listings with a Favorites map that pins each place at its street address, a photo gallery with arrows and zoom, and a Messages page with group chats and private direct messages between a renter and a lister (listers' emails are no longer shown). Added tracking so each new account records which link brought it (Supabase), and turned off email confirmation, which was capping sign-ups at 2 an hour.
- **Grow:** Launched our first paid ad on Reddit today ($100 over 7 days, Nov 20 to Nov 27) with the experiment card committed first. It runs a "sublet network for the Columbia community" message in r/columbia, r/nyc_sublets and r/nycollegestudents. We planned Meta first, but Meta treats rental search ads as Housing ads and blocks the targeting we needed, so we switched before spending anything. No ad results yet (the ad was just published). Signups from posts so far: none.
- **Analyze:** Wrote the usability synthesis from our 3 sessions (sign-in vs sign-up confusion showed up in 3 of 3, "not enough listings" in 3 of 3) and used it to decide the first-page and sign-up changes. Set up a Supabase query that counts accounts per campaign, which is how we will read the ad result.
- **Research:** Ran 3 usability sessions on the staging MVP (Nov 6, Nov 10, Nov 11). We have not run new sessions since.

## Planning: what we're doing next

- **Build:** Make "Sign up" the primary button and simplify the first page so the search box comes first (from the usability sessions). Then the "we'll look for it" request form for searches with no match, so an empty search becomes an email we can follow up on.
- **Grow:** Watch the Reddit ad for its 7 days without changing it, and keep outreach to students who can post their own sublet, since supply is still our biggest gap.
- **Analyze:** Read the ad result from Supabase (accounts tagged `aditya_adtest_nov2026`) and Reddit's dashboard (clicks, spend), and compare with the pass/fail bar we set before launch: pass at 5 or more account signups, fail at 2 or fewer.
- **Research:** Run 3 to 5 more usability sessions after the sign-up change, with at least one stranger, to see whether people now find the chat search and sign up without help.

## Issues

- **Google Analytics access:** Gable's property is under a different Google account, so we can't see it yet. Sam has been asked to add Michelle as an Editor. Until then we read results from Supabase.
- **Small audience:** Reddit estimates only 7 to 12 clicks a day, so the ad result will be directional, not precise.
- **Supply:** still very few real listings.
