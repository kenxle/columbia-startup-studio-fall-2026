# SettleWise — Demand Strategy (Fall 2026)

**Planning period:** October 22–December 13, 2026 (remaining semester)  
**First execution deadline:** Sunday, October 25, 2026  
**Product:** SettleWise — an apartment-search web app helping renters find and compare apartments more confidently.  
**Primary goal:** Bring relevant apartment hunters to SettleWise's homepage and landing pages, learn from their problems, and convert interested visitors into email signups and, as features become available, active users.

> **Planning assumptions:** This plan covers the remaining Fall 2026 semester, with weekly Sunday checkpoints. The exact course end date and the blog article taxonomy on **class 6, slide 45** should be confirmed against the course materials. Article formats below are practical working categories, **not a verified transcription of slide 45**. All reach and conversion targets are estimates, not actuals. Replace `[TBD]` entries with live links after publishing; do not represent scheduled work as completed.

## 0. This week: Friday Nov 20 to Thursday Nov 26 (updated for HW 9)

**What changed since October 22:**
- **17 signups, 6 active (Nov 20, `/api/metrics`), almost all from people we know and none from a tracked channel.** In GA4, 92% of users came in as Direct and no UTM traffic was recorded before the Meta ad started on Nov 19 (`hw8/growth-strategy.md`). Posting on social and in communities without links hasn't brought in users we can see.
- **Our cold start type is "good product, no distribution"** (`hw9/cold_start_plan.md`). This week we stop broad posting and go one-to-one with **renters mid-search**, using one personal channel and one one-to-many channel, as Class 10 recommends.
- **Measurement now works.** `signup_started`, `sign_up` and `comparison_viewed` are live in GA4 (Nov 16). An **activated** user is one who fired `comparison_viewed` (a comparison of 2+ of their own apartments).
- **Domain:** `settlewise.group`.

### Channel cards

| | **A. Campus DMs** (personal) | **B. Comparison replies on Reddit** (one-to-many) | **C. Meta ad** (paid) |
|---|---|---|---|
| **Owner this week** | Izum (each teammate DMs the people they know) | Izum | See the experiment card (Part 1). We don't touch it until the 7 days are up. |
| **Where, and the rules** | Columbia classmates moving for spring, our 5 usability testers and one friend from each of our 5 interviewees. Personal messages only, never a list or group blast. We ask before posting in any group. | r/NYCapartments, r/AskNYC, r/columbia: posts where someone is choosing between 2–3 apartments. **Before the first reply, read each sidebar and write its self-promotion rule here:** r/NYCapartments: _not yet checked_, r/AskNYC: _not yet checked_, r/columbia: _not yet checked_. No link where links aren't allowed. | Meta, Special Ad Category: Housing |
| **Landing page** | `https://settlewise.group/students-on-a-budget?utm_source=dm&utm_medium=personal&utm_campaign=hw9_coldstart&utm_content=campus` | `https://settlewise.group/compare-apartments?utm_source=reddit&utm_medium=community&utm_campaign=hw9_coldstart&utm_content=comparison_reply` | Per the experiment card |
| **Volume** | 5 DMs a day for 5 days = **25 touches**. One follow-up after 3–5 days, then stop. | **10 replies** over the week, at most 2 a day, with no two replies saying the same thing | Fixed budget |
| **Success bar (set before we start)** | 25 touches → 10 replies → 5 signups → **3 activated** | 10 replies → 15 sessions → 2 signups → **1 activated** | Pass bar on the experiment card |

The **Shortlist Night** invite (`hw9/cold_start_plan.md`) goes out through channel A. RSVPs are tracked in the sign-up sheet, not here.

### First messages

Every message has the four parts from Class 10: something specific about them, who we are, one small ask, and an easy out.

**A. Campus DM (Instagram, WhatsApp or iMessage, to someone we know):**
> Hey [name], you mentioned you're looking for a place for January. I'm building SettleWise with three classmates for our Columbia startup class. It puts the StreetEasy listings you've already found side by side and ranks them by what matters to you. Would you try it on the 2–3 places you're deciding between and tell me where it gets confusing? Takes about 5 minutes. No worries at all if not. [campus link]

**A. Follow-up, once, 3–5 days later:**
> No pressure on this. If you've already picked a place, congrats! And if you're still deciding, the offer stands. [campus link]

**A. Asking an interviewee for a friend:**
> Hi [name], thanks again for talking to us about your apartment search in October. We built a tool from what you and others told us. Do you know one person who's apartment hunting right now and might want help comparing their options? Happy for you to just forward this. [campus link]

**B. Reddit reply (the comparison is written in the comment, so it helps without a click):**
> I put your three side by side:
> - **[Apt 1]:** $[rent], [net effective rent if there's a free month], [what the listing leaves out, e.g. no laundry info]
> - **[Apt 2]:** ...
> - **[Apt 3]:** ...
>
> Based on what you said matters ([their priorities]), [Apt X] comes out ahead, mainly because [reason]. Before signing, I'd ask the broker about [missing detail] and [fee].
>
> *Disclosure: I'm a Columbia student building a free tool that does this comparison (SettleWise). Happy to share it if that's useful, no worries if not.* [link only where the subreddit allows it]

### Results log (fill in every Friday from GA4, by UTM source and campaign)

| Week ending | Channel | Touches | Replies / sessions | Signups | Activated | What we learned |
|---|---|---:|---:|---:|---:|---|
| Nov 19 (Nov 13–19) | All channels | Not logged (outreach starts Nov 20) | 61 sessions | 3* | 1* | Tracking works end to end, but we can't yet see a single stranger sign up. *Likely our own 2 tracking-test signups on Nov 18; these events went live Nov 16.* |
| Nov 26 | A. Campus DMs | | | | | |
| Nov 26 | B. Reddit replies | | | | | |
| Nov 26 | C. Meta ad | See the experiment card | | | | |

We write actuals here, zeros included. We never estimate a number we can't see.

---

*The plan below is the original October 22 semester plan. Section 0 above replaces its channel priorities from Nov 20 onward. Sami's social posts continue as a secondary channel and carry UTM links from now on (`utm_source=instagram`, `tiktok`, `facebook` or `x`; `utm_campaign=hw9_coldstart`).*

## 1. Weekly responsibility for traffic

Sami owns social content and distribution. Izum owns community engagement, the email program, and the first blog post. Both are responsible for bringing qualified visitors to SettleWise, not just creating content. **Sunday is the shared reporting and deliverable deadline each week.**

| Week (Monday–Sunday) | Traffic owner(s) | Sami — social | Izum — communities, email, blog | Sunday checkpoint |
|---|---|---|---|---|
| Oct 19–25 | Sami + Izum | 1 Instagram/TikTok post + 1 Facebook/X post | Join relevant discussions without promotional links; launch automated welcome email; publish first blog about renter complaints | Oct 25 |
| Oct 26–Nov 1 | Sami + Izum | 2 short-form posts + 1 Facebook/X post; test a renter-pain-point hook | Reply helpfully in 3–5 threads; share a resource only where permitted; publish blog #2; send Sunday project update | Nov 1 |
| Nov 2–8 | Sami + Izum | 2 short-form posts + 1 Facebook/X post; test carousel vs. video | Engage in 3–5 discussions; publish blog #3; send Sunday update | Nov 8 |
| Nov 9–15 | Sami + Izum | 2 short-form posts + 1 Facebook/X post; highlight a useful apartment-search checklist | 3–5 discussions; publish blog #4; invite interested renters to give feedback | Nov 15 |
| Nov 16–22 | Sami + Izum | 2 short-form posts + 1 Facebook/X post; share a product demo if ready | 3–5 discussions; publish blog #5; send development update | Nov 22 |
| Nov 23–29 | Sami + Izum | 1–2 short-form posts + 1 Facebook/X post; seasonal moving advice | 2–4 discussions; publish blog #6; Sunday email, adjusted for Thanksgiving week | Nov 29 |
| Nov 30–Dec 6 | Sami + Izum | 2 short-form posts + 1 Facebook/X post; repeat best-performing topic | 3–5 discussions; publish blog #7; request product feedback | Dec 6 |
| Dec 7–13 | Sami + Izum | 2 short-form posts + 1 Facebook/X post; semester recap and next steps | 3–5 discussions; publish blog #8; final newsletter and channel review | Dec 13 |

**Continuity rule:** If one person is unavailable, the other publishes the minimum viable weekly deliverable and logs the change. The remaining teammates can review links, contribute content ideas, and respond to product feedback, but are not listed as accountable traffic owners without agreement.

## 2. Target communities and expected reach

Our priority audience is students, recent graduates, first-time renters, and people currently searching for apartments, especially in NYC. We will first listen and contribute useful answers. We will **not drop unsolicited links** or post the same promotion in multiple communities. Check each community's current self-promotion rules before linking SettleWise.

| Community | URL | Why relevant | Estimated views of an individual relevant contribution* | Initial approach |
|---|---|---|---:|---|
| r/AskNYC | https://www.reddit.com/r/AskNYC/ | NYC neighborhood and renting questions | 100–1,500 | Answer questions with specific, non-promotional guidance |
| r/NYCapartments | https://www.reddit.com/r/NYCapartments/ | Active NYC apartment seekers | 100–1,000 | Join discussions about searching, applications, and scams |
| r/Columbia | https://www.reddit.com/r/columbia/ | Students dealing with housing searches | 50–500 | Help with student-specific apartment-search questions |
| r/Apartmentliving | https://www.reddit.com/r/Apartmentliving/ | Renters discussing frustrations and practical issues | 100–1,000 | Identify recurring complaints; offer useful checklists |
| NYC student housing Facebook groups | [TBD — link to specific approved group] | Students and recent graduates finding roommates/housing | 50–500 | Ask admins about resource-sharing rules; join discussions |
| Columbia student / campus housing channels | [TBD — verify specific forum or group] | Focused student audience | 25–250 | Share tips or request interviews with moderator permission |

*These are **hypothetical per-post impression ranges for planning**, not verified membership counts or guaranteed views. Group access, algorithmic distribution, timing, and moderation may dramatically change results. Record actual impressions wherever the platform reports them. Avoid summing estimates as unique people because audiences overlap.

**Weekly community workflow (Izum):**
1. Monday: find 3–5 active conversations where renters discuss a specific problem.
2. Tuesday–Thursday: add thoughtful replies, questions, or advice. **First week (Oct 19–25): do not include SettleWise links.**
3. Friday: log recurring complaints, exact wording, and useful product insights (without storing personal identifying details).
4. In later weeks: post a blog or landing-page link only when it is directly helpful and explicitly allowed by the community.
5. Sunday: report conversations joined, estimated/actual reach, referrals, signups, and qualitative insights.

## 3. Social media posting strategy

**Channels and owners:** Instagram and TikTok are primary short-form channels; Facebook and X (Twitter) are secondary distribution channels. Sami creates and publishes content, while Izum contributes renter pain points gathered from community discussions.

**Week of October 19–25 — required initial deliverables:**
- **1 Instagram/TikTok concept:** Publish to Instagram, TikTok, or both. Topic: a relatable apartment-hunting frustration (e.g., comparing listings across tabs). Clear CTA: visit the appropriate SettleWise landing page.
- **1 Facebook/X post:** Share a concise renter tip or question and invite responses. Add a link only if the platform or group permits it.

**October 26 onward:** Target 2 short-form concepts and 1 Facebook/X post each week. Repurpose the same concept across channels when appropriate, rather than requiring entirely unique content for each platform. Alternate among renter frustrations, actionable tips, explainers, website/blog updates, and product demonstrations when functional.

| Week ending | Instagram/TikTok concept | Facebook/X concept | Published post URLs |
|---|---|---|---|
| Oct 25 | “What makes apartment hunting frustrating?” | “What is your biggest apartment-search pain point?” | IG: [TBD] · TikTok: [TBD] · FB/X: [TBD] |
| Nov 1 | Apartment search across too many tabs | Checklist: questions before touring | [TBD] |
| Nov 8 | Spotting suspicious listings | Poll: hardest part of NYC apartment search | [TBD] |
| Nov 15 | Hidden costs to check | Share a cost-comparison tip | [TBD] |
| Nov 22 | Demo or workflow preview (only if ready) | Ask for early feedback | [TBD] |
| Nov 29 | Holiday-season housing prep | Moving timeline tip | [TBD] |
| Dec 6 | Compare options with a structured checklist | Most useful renter resource | [TBD] |
| Dec 13 | Semester learnings and next steps | Recap and signup invitation | [TBD] |

**Link requirements:** As soon as a post is published, replace `[TBD]` with its public permalink. When available, add platform-specific UTM links to the website destination, for example:

`https://settlewise.group/[LANDING_PAGE]?utm_source=instagram&utm_medium=social&utm_campaign=fall2026_demand&utm_content=20261025_painpoint`

Use lowercase UTM values consistently. Use `utm_source=tiktok`, `facebook`, `x`, or `reddit` when applicable. Never invent live post URLs.

## 4. Blog strategy and editorial calendar

**Cadence:** **1 post every week**, beginning Sunday, October 25, for **8 planned posts** across the remaining semester. Izum owns the first blog post and the editorial schedule; Sami can turn each blog into short-form social content. Each blog should address a genuine renter problem and link naturally to a relevant SettleWise page.

**Working article formats (verify against class 6, slide 45):** pain-point/problem analysis, how-to guide, checklist/listicle, comparison, FAQ/explainer, case study or user story, product update, and roundup/recap. We will update the format labels if the slide specifies a different taxonomy.

| Publication date | Working title | Format | Reader value / angle | URL |
|---|---|---|---|---|
| Oct 25 | Why Apartment Hunting Feels So Frustrating: Common Complaints from Renters | Pain-point analysis | Summarize recurring issues such as scattered listings, uncertainty, and hard-to-compare options; distinguish user evidence from assumptions | [TBD] |
| Nov 1 | The First-Time Renter’s Apartment Search Checklist | How-to / checklist | Actionable steps from requirements to tours to applications | [TBD] |
| Nov 8 | How to Spot Common Apartment Listing Red Flags | How-to guide | Teach renters to assess suspicious signs without claiming to certify listings | [TBD] |
| Nov 15 | Beyond the Monthly Rent: Costs to Compare Before Signing | Explainer / listicle | Compare deposits, utilities, commute, and other expenses | [TBD] |
| Nov 22 | Spreadsheet vs. Saved Tabs vs. a Search Tool: How to Compare Apartments | Comparison | Present tradeoffs fairly; position SettleWise only for features that exist | [TBD] |
| Nov 29 | 7 Questions to Ask Before an Apartment Tour | FAQ / checklist | Give a practical, shareable set of questions | [TBD] |
| Dec 6 | What We Learned Talking to Apartment Hunters | Research insight / case study | Share aggregated findings, with permission and without identifying participants | [TBD] |
| Dec 13 | What’s Next for SettleWise: Features, Feedback, and Lessons | Product update / recap | Summarize only completed work and transparently identify planned features | [TBD] |

**Blog production routine:** Monday collect questions; Tuesday select an angle; Wednesday draft; Thursday fact-check and review; Friday format/SEO and prepare accompanying social clips; Sunday publish and add URL to this file. Use descriptive headings and a single relevant email-signup CTA. Do not manufacture testimonials or imply features already exist if they do not.

## 5. Email strategy: welcome, updates, lifecycle

**Owner:** Izum. **Initial deadline:** automated welcome email active by Sunday, October 25.

**Email types**

| Trigger / timing | Audience | Message | Action |
|---|---|---|---|
| Immediately after signup | New subscribers | Welcome to SettleWise; explain who the product is for and what updates they will receive | Reply with biggest apartment-search frustration or visit blog |
| Every Sunday, starting Oct 25 | Subscribers who opted into updates | Brief progress newsletter: one useful renter tip, latest blog post, and an honest product-development update | Read blog / share feedback |
| When a feature is genuinely released | Subscribers interested in that feature | Explain the released feature, who benefits, and how to use it | Try feature |
| ~7 days after signup, if practical to automate | Subscribers who have not engaged | Send one helpful tip or quick survey, without pressure | Give feedback / visit site |
| After first meaningful product use, if usage data and consent permit | Active users | Short follow-up asking what worked and what was confusing | Share feedback |

**Lifecycle stages:** (1) visitor → (2) email signup → (3) welcomed subscriber → (4) engaged reader or respondent → (5) early product user when features launch. Initially segment only by signup date and email engagement. Add feature-usage segmentation **only after the app reliably records that behavior, users have received appropriate privacy disclosures, and email permissions support it**.

**Minimum email setup:**
- Store subscribers through the approved signup form/provider and document consent.
- Trigger welcome email once per signup; test with a real test address.
- Send Sunday updates with clear sender identity, a valid unsubscribe method, and no misleading feature claims.
- Avoid collecting sensitive housing or financial information through email unless necessary and properly secured.
- Review delivery, opens (directionally), link clicks, unsubscribes, and replies. Prioritize clicks and responses over open rates because open tracking can be unreliable.

**Suggested welcome email content:**

**Subject:** Welcome to SettleWise — let's make apartment hunting easier  
**Body:** Thanks for joining SettleWise! We're building a simpler way to organize and compare apartment options. We'll share practical renter tips and occasional product updates. For now, we'd love to know: what's the most frustrating part of your apartment search? Just reply to this email. You can unsubscribe from updates at any time.

## 6. Measurement and experimentation

**Primary conversion:** completed email signup. **Primary acquisition measures:** landing-page sessions, community/site referrals, and visitors who sign up. **Qualitative metric:** recurring renter pain points identified through replies, interviews, and feedback.

| Metric | How measured | Initial planning target, not actual |
|---|---|---|
| Social content published | Public post URLs | Oct 25: 2 concepts; later: 3 concepts/week |
| Community interactions | Link to discussion + notes | Initial week: 3+ helpful discussions, no promotional links |
| Blog cadence | Published blog URLs | 1/week, 8 total from Oct 25–Dec 13 |
| Email delivery | Email provider logs | Welcome automation tested by Oct 25; weekly Sunday update |
| Website traffic | GA4 by UTM source/medium | Establish baseline in first 2 weeks, then improve best channels |
| Email conversion | GA4 signup key event ÷ sessions | Track weekly; set target once baseline exists |
| Qualified feedback | Reply form / opt-in interviews | At least 2 actionable renter insights per week |

**Weekly experiment:** Test one variable at a time—topic, post format, CTA, channel, or landing-page headline. Compare results at similar time windows; do not draw strong conclusions from very small samples.

**Sunday reporting template:**

| Week ending | Social post links | Community discussion links | Blog link | Newsletter sent? | Sessions by source | New signups | Top insight | Next experiment |
|---|---|---|---|---|---:|---:|---|---|
| Oct 25 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |

## 7. Immediate to-do list — Sunday, October 25

### Sami — social
- [ ] Draft one short-form renter-pain-point concept.
- [ ] Publish on Instagram and/or TikTok and save the direct public URL(s).
- [ ] Publish one Facebook or X post and save the direct public URL.
- [ ] Use trackable links where applicable; record any available reach and site visits.

### Izum — communities, email, and blog
- [ ] Identify and enter at least three relevant renter discussions; **do not drop SettleWise links yet**.
- [ ] Log community links, recurring complaints, and moderator/self-promotion rules.
- [ ] Activate and test the automated welcome email for new subscribers.
- [ ] Prepare the first Sunday email update, reporting only real progress.
- [ ] Publish blog #1 on common apartment-hunting complaints and add its live URL.

### Joint Sunday review
- [ ] Put every live social, discussion, and blog URL into this file.
- [ ] Verify signup forms and the signup tracking event function on the linked pages.
- [ ] Record available traffic and signup results; mark metrics unavailable rather than guessing.
- [ ] Choose the strongest pain point and one experiment for the next week.

## Reference

- [Course class 6 slides (see slide 45 for required article types)](https://github.com/kenxle/columbia-startup-studio-fall-2026/blob/main/classes/20261016_c6w6_fri_build-kickoff/class-6-slides.pdf)

_Last revised: November 20, 2026 (section 0 added for HW 9). Original plan: October 22, 2026._
