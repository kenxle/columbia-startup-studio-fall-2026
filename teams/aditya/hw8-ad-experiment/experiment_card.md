# Experiment Card: Gable (Reddit ad test)

Team Aditya: Michelle Mai, Lookman Mustapha, Sam Hearst
Card owner and ad account owner: Michelle Mai

Sections 1 to 8 are committed before launch and don't change after. Section 9 is filled in for homework 9.

Platform note: we planned a Meta test first. Meta treats rental search ads as Housing ads and blocks targeting by age and interests, so we could not reach our audience of students and recent grads aged 18 to 30 on Meta. We switched to Reddit before spending anything.

---

## 1. Question

Should we lead with "real sublets near Columbia, checked before you pay" as Gable's promise to students?

## 2. Hypothesis

At least 10% of clicks from members of NYC student subreddits who see "real sublets near Columbia, checked before you pay" will create a Gable account after searching for a sublet. Under 3% means the promise or the page isn't working.

## 3. The one variable

- **What we're testing:** the promise: "real sublets, checked before you pay" (the trust angle from our brand position and from what our interviewees told us about fake listings and Zelle).
- **Also in the ad, not tested separately:** one sentence telling students they can list their own place. The promise being tested, "real sublets, checked before you pay", stays in the body of the ad.
- **Everything we hold fixed:** one landing page (the Gable homepage, https://www.gable.fit), one audience, one ad, $100 lifetime budget, 7 days, and the same flow: type a search, then sign up to see matches.

## 4. Audience

- **Who we want to reach:** students and recent grads, about 18 to 30, looking for a sublet in NYC.
- **Platform and targeting:** Reddit, community targeting: r/columbia, r/barnard, r/nyu, r/nycollegestudents and r/NYCapartments (the same communities we have been posting in). Reddit does not offer age targeting, so the communities are how we reach that age range. United States, feed and conversation placements.
- **Why this audience:** these are the places where students looking for an NYC sublet already ask for help, and we have posted there for several weeks, so we know what these communities respond to.

## 5. Setup

- **Platform:** Reddit
- **The question this platform can answer:** does this community respond to the promise? (Reddit is not the place to read a precise signup rate; the bar below is set for a small, directional test.)
- **Campaign objective:** Traffic (clicks to the website)
- **Budget:** $100 as a lifetime (total) budget
- **Start date:** Nov 21, 2026 **End date:** Nov 28, 2026 (7 days)
- **What counts as a signup:** someone creates a Gable account. On gable.fit, a visitor who is not signed in sees "Sign up to see your matches" after they search, and creating an account fires the Google Analytics event `account_created` (marked as a key event). Our own test accounts are excluded. The homepage waitlist email box still works; those emails are reported separately and do not count toward the bar.
- **Where we read signups from:** Google Analytics, event `account_created` for visits with `utm_source = reddit`, checked against new users in Supabase Authentication during the 7 days.
- **Tracking check:** we clicked through our own ad link, searched, created a test account, and saw the visit and the `account_created` event arrive in Google Analytics Realtime. Yes / No (screenshot in `analytics/`)
- **Expected clicks** (the platform's estimate): ___ (we assume about 100 for $100; update from Reddit's estimate in the ad builder before launch)

**Ad link:**
`https://www.gable.fit/?utm_source=reddit&utm_medium=paid&utm_campaign=aditya_adtest_nov2026`

**The ad (written in a student's own voice; the homepage says "real sublets near Columbia" and "checked"):**
- Headline: "Looking for a sublet in NYC? Or subletting your place?"
- Body: "We're three Columbia students who got tired of messaging twenty people to find out which sublet was real. So we built Gable: tell it what you need and see real places from other students, checked before you pay. Away this summer? List your own place and cover your rent. Free to join."
- Button: Sign Up
- Image: one screenshot of Gable's chat search with a result card showing what we checked.

Note: Gable has few real listings today, so the ad offers a search and early access, not a large catalog. Listing your own place (List your room) is real and works, but a person has to create an account first, so it counts as a signup the same way.

## 6. The bar

Set before launch.

- We read the result once, after the end date.
- **PASS** if signups are **7 or more**.
- **FAIL** if signups are **4 or fewer**.
- **UNCLEAR** if **5 or 6**.
- **Our prediction:** 4 signups (about 4%).

Based on the template table: floor 3% vs. good 10%, 100 clicks. If Reddit's estimate is about 140 clicks, use PASS at 9 or more, FAIL at 7 or fewer, UNCLEAR at 8; if about 166, PASS at 10 or more and FAIL at 9 or fewer.

## 7. What we'll do

- **If PASS:** make "checked before you pay" the headline everywhere (homepage, Reddit posts) and run the same ad again in a second set of subreddits to replicate before spending more.
- **If FAIL:** a low click rate means the hook or the community is off, so test a different promise next, such as skipping the back-and-forth of messaging many people. Clicks but no signups means the homepage or sign-up step is the problem, so fix it and re-run.
- **If UNCLEAR:** don't spend more. Decide from interviews and usability tests.

## 8. Stop rules

The only reasons to touch the ads mid-test: tracking is broken, the ad is disapproved, or spend is running over budget. Nothing else.

---

## 9. Result

Filled in for homework 9, after the end date.

- **Impressions:** ___ **Clicks:** ___ **Click rate:** ___%
- **Signups:** ___ **Signup rate:** ___%
- **Spend:** $___ **Cost per signup:** $___
- **Call:** PASS / FAIL / UNCLEAR
- **Did we do what section 7 said?**
