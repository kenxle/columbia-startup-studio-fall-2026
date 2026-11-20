# SettleWise: Backlog (HW 9, Part 3)

**Ranked:** Friday, November 20, 2026
**Inputs:** where our 5 usability testers got stuck (`hw8/user_testing_summary.md`), what we said we'd change in that write-up (section 5), the GA4 gaps in `hw8/growth-strategy.md`, our earlier leftovers list (`docs/MVP_Handoff_Leftover.md` in the product repo), and what's on `main` as of Nov 19.

**What "impact" means for us right now:** a new renter **reaches the comparison with 2+ of their own apartments, without help**. Only 2 of 5 testers reached the aha moment, only 6 of our 17 signups are active, and the class only counts a user who has done the core action. Anything that doesn't move that number, or help us see it, scores low on impact.

## Top 7, ranked by RICE

**Score = Reach × Impact × Confidence ÷ Effort.**

| Factor | Scale |
|---|---|
| Reach | 1, 2, 3, 5, 8, 13 (13 = every new user) |
| Impact | 3 massive, 2 high, 1 low |
| Confidence | 100% data, 80% reasoning, 50% guess |
| Effort | 1, 2, 3, 5, 8, 13, 21 |

🤖 = AI could help build or run it.

| Rank | Item | Type | Evidence | R | I | C | E | **Score** |
|---|---|---|---|---:|---:|---:|---:|---:|
| **1 ★** | **Show the Saving shortcut working on a real StreetEasy listing.** Add a 10–15 second looping video in the empty-group guide and the Saving shortcut modal: drag to the bookmarks bar, click on a listing, and the apartment appears. Add one line for "Can't see your bookmarks bar?" (⌘⇧B / Ctrl+Shift+B). | Activation | 5/5 struggled to add a listing. The tutorial didn't fix it (P3). P3 asked for a video several times. P1 and P4 didn't know where the bookmarks bar was. | 13 | 2 | 80% | 2 | **10.4** |
| 2 | **Make signups and activation countable.** Mark `sign_up` as a key event in GA4 admin, filter out team traffic, and check that `comparison_viewed` shows up from a real stranger's session. | Measurement | GA4 showed 0 key events. Chrome and Dashboard numbers are probably inflated by our own testing. We can't tell whether the cold start plan worked without this. | 13 | 1 | 80% | 1 | **10.4** |
| 3 | 🤖 **Turn Analyze on in production.** The AI trade-off summary is built and merged (Nov 13). It's off until the backend's `ANTHROPIC_API_KEY` and `NEXT_PUBLIC_COMPARISON_ANALYSIS=1` are set on Railway. *Needs team approval because it changes deployment settings.* | Feature | P4 saw "no difference apart from price" in a plain table. Our own write-up listed an AI recommendation under "Exploring." No user has tried it yet, hence 50%. | 8 | 2 | 50% | 1 | **8.0** |
| 4 | **Personal callouts at the top of results.** For example, "Over your $2,400 budget" on the apartments that are, and the net effective rent when there's a free month. | Activation | Both aha moments came from these: P1 when an apartment was flagged over her limit, P2 when he saw net effective rent. This was listed as "Next" in HW8. | 8 | 3 | 80% | 3 | **6.4** |
| 5 | **Diagnose the Safari and iPhone drop-off.** Run the full flow on iPhone Safari and on a Mac in Safari. Fix it or write down why it can't work. | Bug (suspected) | Safari users were engaged for 9s versus 5m 30s on Chrome, and about a third of users are on Safari. P1 usually searches on her phone. It could be team traffic skewing Chrome, hence 50%. | 8 | 3 | 50% | 3 | **4.0** |
| 6 | **Send signed-in visitors to their dashboard.** On the marketing pages, change "Get started" to "Go to my apartments" for anyone already signed in. | Onboarding | After signing up, P5 went back to the homepage and had to hit "Get started" again with no home base. | 3 | 1 | 80% | 1 | **2.4** |
| 7 | **Retest with strangers, unaided.** Use the realistic scenario from HW8 section 6, with no host help, and time how long the first listing takes to add. Run it with the Shortlist Night attendees. | Learning | Hosts helped mid-session in P1 and P5, so 2 of 5 is likely generous. Without a retest we can't tell whether #1–#4 worked. | 5 | 2 | 80% | 3 | **2.7** |

Item 7 scores slightly above item 6, but it's ranked after it on purpose. It only means something once #1–#4 have shipped.

## Next up (scored, not this sprint)

| Item | Type | Evidence | R | I | C | E | Score |
|---|---|---|---:|---:|---:|---:|---:|
| 🤖 Browser extension instead of the bookmarklet | Big bet | P4 suggested it. The bookmark step blocked all 5 testers. It doesn't help Safari or iPhone users. | 13 | 3 | 50% | 13 | 1.5 |
| Profile or home page after signup | Onboarding | P5 got lost after signup. #6 covers most of this for much less work. | 5 | 1 | 50% | 3 | 0.8 |
| Phone layout of the comparison (only 2 columns are visible) | UX | Leftovers list. P1 searches on her phone. Worth doing once #5 tells us how much phone traffic is real. | 5 | 1 | 50% | 3 | 0.8 |
| 🤖 Richer listing data: past-tenant reviews, building complaints from public records (HPD, 311) | Big bet | P4 asked for "a Google review but for each of the properties." The Reddit research shows experienced renters already check HPD and 311 by hand. *A new data source, so it needs team approval.* | 8 | 2 | 50% | 13 | 0.6 |

## Already done since the usability tests (on `main`)

| Change from the HW8 list | Shipped |
|---|---|
| URL paste removed; the Saving shortcut is the single add path | By Nov 6 (HW8) |
| "Add apartment" on the comparison screen | Nov 6 |
| Default comparison on rent shown immediately | Nov 6 |
| Homepage headline says "compare": *"Find apartments anywhere. Compare them here."* | Nov 12 |
| Comparison setup split into 3 steps (Priorities → Ranking → Non-negotiables) | Nov 13 |
| Ranking upgrade (budget anchors, diminishing returns) and the AI trade-off summary (behind a flag, see #3) | Nov 13 |
| Google sign-in replaces email and password | Nov 9 |
| Signup and activation events in GA4 and the Meta Pixel | Nov 16–18 |
| Onboarding tutorial **turned off** (testers skipped it); #1 replaces it with a short video in context | Nov 12 |

We should confirm in the next round of tests that the "3 of 3" label confusion went away with the setup redesign.

## What we're not building, and why

- **A browser extension (for now).** It would be a big build (13), it does nothing for Safari or iPhone users, and we haven't tried the cheap fix (#1) yet. We'll revisit it if fewer than half of the unaided testers can add a listing after #1.
- **Listing data of our own (scraping, reviews, building records).** It's a new data source that needs approval, it's slow, and we'd risk implying a listing is "verified." P4's request is real, but it's one person.
- **Shared groups or roommate invites.** Nobody in testing asked for this. It would create a Group/Invite cold start on top of the one we have.
- **Bringing back URL paste.** It silently failed for P5, and a broken path is worse than none.
- **More priority or requirement types** (lease length, broker fee, guarantor rules). Personas asked for these, but real users haven't, and they add steps to the setup we just shortened.
- **Animation and visual polish on the marketing pages.** P2 said the page had "so much going on." The next homepage change should be less, not more.
