# Experiment Card: Gable (Reddit ad test)

Team Aditya: Michelle Mai, Lookman Mustapha, Sam Hearst
Card owner and ad account owner: Michelle Mai

Sections 1 to 8 are committed before launch and don't change after. Section 9 is filled in for homework 9.

Platform note: we planned a Meta test first. Meta treats rental search ads as Housing ads and blocks targeting by age and interests, so we could not reach our audience of students and recent grads aged 18 to 30 on Meta. We switched to Reddit before spending anything.

---

## 1. Question

Should we lead with "real sublets near Columbia, checked before you pay" as Gable's promise to students?

## 2. Hypothesis

At least 10% of clicks from the people Reddit shows the ad to (it uses r/columbia, r/nyc_sublets and r/nycollegestudents as audience suggestions) who see "Find a sublet through the Columbia community" will create a Gable account after searching for a sublet. Under 3% means the promise or the page isn't working.

## 3. The one variable

- **What we're testing:** the message: Gable as a sublet network for the Columbia community, with places posted by other students (the trust angle from our brand position and from what our interviewees told us about not knowing who is on the other end).
- **What the ad shows:** one headline, one image and a Sign Up button. Reddit Max has no body text field, so the ad does not use the longer body text we drafted.
- **Everything we hold fixed:** one landing page (the Gable homepage, https://www.gable.fit), one headline (entered three times so Reddit cannot rotate), one image, one audience setting, $100 total budget, 7 days, and the same flow: type a search, then sign up to see matches.

## 4. Audience

- **Who we want to reach:** students and recent grads, about 18 to 30, looking for a sublet in NYC.
- **Platform and targeting:** Reddit Max campaign with audience suggestions: r/columbia, r/nyc_sublets and r/nycollegestudents. Reddit says suggestions help find the best audience but do not limit who sees the ad, so some people outside these communities may see it. Location: United States. The campaign is declared as a housing special ad category (Gable lists sublets), which means no age, gender or postal code targeting. We have no interest groups or keywords.
- **Why this audience:** the ad speaks to the Columbia community, so we point Reddit at Columbia students and at the two communities where people already look for NYC sublets. We left out r/NYCapartments because most of its readers are not students. Because suggestions do not limit delivery, we read the result as "people Reddit finds similar to these communities", not "members of these subreddits".

## 5. Setup

- **Platform:** Reddit
- **The question this platform can answer:** does this community respond to the promise? (Reddit is not the place to read a precise signup rate; the bar below is set for a small, directional test.)
- **Campaign objective:** Traffic (clicks to the website). Reddit may label this as the Sales objective with a Clicks goal; we do not use the Reddit pixel and measure in Google Analytics instead.
- **Budget:** $100 in total. Reddit sets a daily budget, so we use $14.28 a day for 7 days (about $100).
- **Start date:** Nov 20, 2026 **End date:** Nov 27, 2026 at 12:30 PM ET (7 days)
- **What counts as a signup:** someone creates a Gable account. On gable.fit, a visitor who is not signed in sees "Sign up to see your matches" after they search, and creating an account fires the Google Analytics event `account_created` (marked as a key event). Our own test accounts are excluded. The homepage waitlist email box still works; those emails are reported separately and do not count toward the bar.
- **Where we read signups from:** Google Analytics, event `account_created` for visits with `utm_source = reddit`, checked against new users in Supabase Authentication during the 7 days.
- **Tracking check:** we clicked through our own ad link, searched, created a test account, and saw the visit and the `account_created` event arrive in Google Analytics Realtime. Yes / No (screenshot in `analytics/`)
- **Expected clicks** (the platform's estimate): ___ about 60. Reddit's builder estimated 6 to 11 clicks a day at our $14.28 daily budget, so about 42 to 77 over the 7 days.

**Ad link:**
`https://www.gable.fit/?utm_source=reddit&utm_medium=paid&utm_campaign=aditya_adtest_nov2026`

**The ad (the homepage says "real sublets near Columbia"):**
- Headline: "Find a sublet through the Columbia community" (entered three times, the same each time)
- Button: Sign Up
- Image: `ad_creative_1200x628.png`, a real screenshot of Gable (the search and its reply next to a real student listing), cropped to 1200 by 628. No stock photos.

Note: Gable has few real listings today, so the ad offers a search and early access, not a large catalog. The longer body text we drafted (it also mentions listing your own place) is saved here for the next test: "Sublet hunting is stressful when you don't know who's on the other end. Gable is a sublet network for Columbia students: places posted by other students, so you're dealing with people from your own community. Tell us what you need and we'll show what fits. And if you're subletting your own place, you can list it here and cover your rent while you're away. It's free to join."

## 6. The bar

Set before launch.

- We read the result once, after the end date.
- **PASS** if signups are **5 or more**.
- **FAIL** if signups are **2 or fewer**.
- **UNCLEAR** if **3 or 4**.
- **Our prediction:** 3 signups (about 5%).

How we picked it: with about 60 clicks, a page at the 3% floor would reach 5 or more signups only about 1 time in 30, and a page at the 10% target would land at 2 or fewer about 1 time in 19. This is smaller than the template table's rows, so we worked it out the same way (the chance of a wrong call is about 1 in 20 either way).

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
