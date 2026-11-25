# SettleWise: Cold Start Plan (HW 9, Part 2)

**Week of:** Friday, November 20 to Thursday, November 26, 2026 (Thanksgiving week)
**Inputs:** Class 10 cold start framework, HW8 usability tests (5 sessions, Nov 5–6), GA4 snapshot in `growth-strategy.md`, 17 signups and 6 active users as of Nov 20 (`/api/metrics`, team excluded), almost all people we know.

## 1. Cold start type: none (single-player), with a distribution and timing problem

We ran the slide 73 diagnostic:

| Question | Our answer |
|---|---|
| Two distinct user groups? | **No.** Renters are the only users. The apartments come from StreetEasy and other listing sites, which renters save into SettleWise with the Saving shortcut. We don't need landlords or brokers to join. |
| Empty without content? | **No.** A new renter fills their own workspace in minutes with listings they've already found. A comparison of 3 apartments is useful to one person with no one else on the product. |
| Needs a whole group at once? | **No.** Search groups are one renter's folders. Roommates can't share a group yet. |
| Needs our users' data to work? | **No.** Ranking is rule-based. Analyze uses an LLM on the renter's own comparison, not data from other users. |

Slide 75 lists us as **Marketplace**, with **renters mid-search** as the hard side. We agree on the hard side, but not on the type. Our supply already exists (it's borrowed from StreetEasy), and the product works for user #1 alone. That makes us a single-player tool. Our cold start isn't an empty product. It's that:

- **Our users only need us for a few weeks.** A renter is "mid-search" for roughly 2–4 weeks, then signs a lease and leaves. We have to reach them inside that window.
- **We have no distribution.** In GA4, 92% of users came in as Direct, and no UTM traffic was recorded before the Meta ad started on Nov 19. Our 17 signups came almost entirely from people we know, not from a channel we can repeat.

So in the decision table (slide 103) we're on the row **"Good product, no distribution"**.

*If we ever let roommates compare inside one shared group, a Group/Invite cold start appears. That isn't on the backlog this month.*

## 2. Hard side: renters mid-search, named

Our hard side is people actively choosing between 2+ NYC apartments **this month**. Everyone else follows them: friends, roommates, the parents who co-sign. These are the people we can name and message today.

| Who | Why them | Who reaches out |
|---|---|---|
| **Columbia classmates moving for the spring semester** (January leases and sublets). Each teammate (Izum, Jorim, Maria, Sami) adds 3+ classmates they know to the team doc by **Mon Nov 23**, first name and last initial only, because this repo is public. | Same campus, same deadline, and they talk to each other. That's an atomic network we can reach in person. | Whoever knows them |
| **Our 5 usability testers (P1–P5).** P1 said she'd use it "if apartment hunting." P4 called it "a very good idea as a product." | They already know the product. If any are searching now, they're our fastest activations. | Original host (Maria P1, Izum P2–P3, Sami P4–P5) |
| **Our 5 interviewees** (Jude, Zaynah, Jackson, Yung Yi, Sean) | They've already moved, so we ask each for **one friend who is searching right now**. | Original interviewer |
| **People who posted this week in r/NYCapartments, r/AskNYC and r/columbia** asking which of 2–3 apartments to pick | They're mid-search and have literally written out a comparison by hand. We find them by searching "which apartment," "help me choose" and "deciding between." | Izum |

We are **not** targeting "students" or "NYC renters" in general this week.

## 3. Two strategies (from the decision table)

| | Strategy | Why it fits us |
|---|---|---|
| **Primary** | **Piggyback on existing networks** (Strategy 6) | Renters mid-search are already on StreetEasy, in Reddit apartment threads and in Columbia housing chats. Our Saving shortcut already lives on top of StreetEasy. We go where they're deciding and give value before linking. |
| **Secondary** | **Event-driven launch** (Strategy 7) | Spring-semester housing is a real, time-bounded crunch for Columbia students before winter break. A single "Shortlist Night" packs 15–30 mid-search renters into one room, and we help each one add their listings with no bookmark confusion. It also fixes our activation killer: 5 of 5 testers struggled with the Saving shortcut alone. |

Anti-patterns we're avoiding (slides 97–101):

- **No big-bang launch.** We do one campus and three communities, not "post everywhere."
- **No discounts.** The product is free, so there's nothing to discount.
- **No hard-side neglect.** The renter is the only side, so every backlog item serves them (see `backlog.md`).

## 4. This week: one concrete action per strategy

### Piggyback: "Comparison replies" in apartment threads (owner: Izum)

- **Action:** Between Fri Nov 20 and Thu Nov 26, find **10 posts** where someone is choosing between 2–3 specific NYC apartments. For each, put their listings into SettleWise and reply with a genuinely useful comparison **written in the comment itself**: net effective rent, what each listing leaves out, and questions to ask before signing. The value has to stand on its own without a click.
- **Rules first:** read each subreddit's sidebar and self-promotion rules before the first reply, and write them in `demand_strategy.md`. Where links are banned, there's no link, just a one-line disclosure ("I'm a Columbia student building a comparison tool") and an offer to send theirs if they want it.
- **Done when:** 10 replies posted, links logged in `demand_strategy.md`, with every link carrying `utm_source=reddit`.

### Event-driven: book and announce "Shortlist Night" (owner: picked by the team by **Mon Nov 23**; whole team at the event)

- **Action:** By Wed Nov 25, **book a room on campus** for one evening in the week of **Dec 7–11** (the exact date is set when the room is booked). Then post one invite in the Columbia channels each teammate is a member of, after checking whether each channel allows it. Personally invite the classmates named in section 2.
- **The pitch:** "Moving for spring? Bring the 3 apartments you can't decide between. In 30 minutes you'll have them side by side, ranked by what matters to you."
- **At the event:** we set up the Saving shortcut on each person's own laptop, which tests the setup fix live, and watch who reaches the comparison.
- **Done when:** room booked, invite posted, **10 RSVPs** collected in a sign-up sheet.

## 5. How we'll know it worked

| Measure | This week's bar (set before we start) | Source |
|---|---|---|
| Comparison replies posted | 10 | Links in `demand_strategy.md` |
| Sessions from Reddit | 15 | GA4, `utm_source=reddit` |
| New accounts | 5 | GA4 `sign_up` |
| **Activated**: compared 2+ apartments | **3** | GA4 `comparison_viewed` |
| Shortlist Night RSVPs | 10 | Sign-up sheet |

These are our own targets to learn from, not benchmarks. We report actuals in next Friday's weekly update, including zeros.
