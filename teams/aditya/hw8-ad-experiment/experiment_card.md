# Experiment Card: Gable (Meta ad test)

Team Aditya: Michelle Mai, Lookman Mustapha, Sam Hearst
Card owner and ad account owner: [name one teammate]

Sections 1 to 8 are committed before launch and don't change after. Section 9 is filled in for homework 9.

---

## 1. Question

Should we lead with "real sublets near Columbia, checked before you pay" as Gable's promise to students?

## 2. Hypothesis

At least 10% of visitors from Columbia-area students on Meta who see "real sublets near Columbia, checked before you pay" will leave their email for early access on the Gable homepage. Under 3% means the promise or the page isn't working.

## 3. The one variable

- **What we're testing:** the promise: "real sublets, checked before you pay" (the trust angle from our brand position and from what our interviewees told us about fake listings and Zelle).
- **Everything we hold fixed:** one landing page (the Gable homepage, https://www.gable.fit), one audience, one ad, $100 lifetime budget, 7 days, the same email form at the bottom of the page.

## 4. Audience

- **Platform and targeting:** Meta (Facebook and Instagram). New York City plus 15 miles. Ages 18 to 24. Interests: Columbia University, Barnard College, NYU, The New School, Fordham, subletting, StreetEasy. English.
- **Why this audience:** these are the students we interviewed, tested with, and have been posting to on Reddit. Starting narrow on a known audience lets the ad algorithm learn on $100.

## 5. Setup

- **Platform:** Meta
- **The question this platform can answer:** do visitors sign up when they see this promise?
- **Campaign objective:** Traffic (landing page views)
- **Budget:** $100 as a lifetime (total) budget
- **Start date:** ___ **End date:** ___ (7 days)
- **What counts as a signup:** a new row in the Supabase `signups` table with `page = 'home'` and `utm_campaign = aditya_adtest_nov2026`, excluding our own test rows. It also fires the Google Analytics `sign_up` key event on `/thanks`.
- **Where we read signups from:** Supabase `signups`, checked against Google Analytics by UTM.
- **Tracking check:** we clicked through our own ad link and saw the visit and the signup arrive in Google Analytics Realtime. Yes / No (screenshot in `analytics/`)
- **Expected clicks** (the platform's estimate): ___ (we assume about 166 at typical Meta prices; update from the ads dashboard)

**Ad link:**
`https://www.gable.fit/?utm_source=meta&utm_medium=paid&utm_campaign=aditya_adtest_nov2026`

**The ad (must match the homepage):**
- Primary text: "Looking for a sublet near Columbia? Tell Gable what you need and get real places, checked before you pay. Built by Columbia students. Be first in."
- Headline: "Real sublets near Columbia"
- Description: "Checked before you pay"
- Button: Sign Up
- Image: one screenshot of Gable's chat search with a result card showing what we checked.

Note: Gable has few real listings today, so the ad offers early access, not listings you can book now.

## 6. The bar

Set before launch.

- We read the result once, after the end date.
- **PASS** if signups are **10 or more**.
- **FAIL** if signups are **9 or fewer**.
- **UNCLEAR** if between (with about 166 clicks there is no unclear zone; if Meta delivers about 140 clicks, use PASS at 9 or more, FAIL at 7 or fewer, UNCLEAR at 8).
- **Our prediction:** 7 signups (about 4%).

Based on the template table: floor 3% vs. good 10%, 166 clicks.

## 7. What we'll do

- **If PASS:** make "checked before you pay" the headline everywhere (homepage, Reddit posts) and run the same ad again with a second audience to replicate before spending more.
- **If FAIL:** a low click rate means the hook or the audience is off, so test a different promise next, such as skipping the back-and-forth of messaging many people. Clicks but no signups means the homepage is the problem, so fix the page and re-run.
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
