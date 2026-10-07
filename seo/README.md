# SEO plan: happypizza.studio

Built from the Treg keyword export (US volumes, 7 Oct 2026) and a crawl of all 24 live URLs.

## The one finding that matters

The phrase **"branding agency"** appears zero times on the live site. "Startup branding agency", "branding agency for startups", "SaaS branding", "branding studio": all zero. The site says "brand identity" everywhere. Google ranks pages for the words on them. Every item below is downstream of fixing that.

## Keyword to page map

| Target cluster | Vol/mo | Diff | Page | Action |
|---|---|---|---|---|
| startup branding agency / branding agency for startups / branding for startups | 1,440 | 0–20 | **NEW** `/startup-branding-agency` | Build. Full copy in `pages/05`. Priority 1. |
| saas branding / saas branding agency | 190 | 0–46 | **NEW** `/saas-branding-agency` | Build. Full copy in `pages/06`. Priority 2. |
| branding studio / design studio branding | 1,140 | 22–36 | `/about` + `/` | Rewrite title, hidden H1, intro line. `pages/01`, `pages/03`. |
| brand identity design | 1,900 | 52 | `/services` | Title and H1 already close. Tighten. `pages/02`. |
| branding agency (head) | 9,900 | 68 | `/` | Not winnable yet. Put the phrase in the home title and schema so the site is at least eligible. |
| branding agency for small business | 590 | 0 | NEW article, optional | Intent mismatch with $10k packages. Outline in `pages/07`; routes to the $1,200 teardown. Your call. |
| branding agency houston / austin | 310 | 10–15 | Skip for now | Reasoning in `pages/08`. |
| best branding agency / agencies | 1,300–1,600 | 18–24 | Skip | Listicle intent. You don't rank an agency site for this; you get on the lists. |
| saas marketing agency | 1,300 | 14 | Skip | Not a service you sell. |

## Order of work

1. Build `/startup-branding-agency` (`pages/05`). Add it to the nav or footer, sitemap, and llms.txt.
2. Apply the title / meta / hidden-H1 edits to home, services, about, work (`pages/01` to `04`). Thirty minutes of work.
3. Schema and internal-link changes in `technical.md`.
4. Build `/saas-branding-agency` (`pages/06`).
5. Decide on the small-business article (`pages/07`).
6. Re-check Search Console positions for the target terms after 6 to 8 weeks. Don't touch titles again before then.

## Conventions used in the specs

- Titles stay under 60 characters where possible. Brand suffix ` | Happy Pizza Studio` stays.
- The site already uses an `sr-only` span inside the display H1 (see `/work`). Hidden H1 text below goes into that span. The visible headline doesn't change.
- "Colour" vs "color": the site mixes both. Google treats them as the same for ranking, but US buyers searching are typing "color". Body copy on the two new pages uses US spelling on purpose.
- Nothing in the copy is invented. Every client, number, price and quote comes from the live site. If a fact is wrong on the live site, it is wrong here too.

## What I could not do

The Next.js source for happypizza.studio is not in this repository (the branch has one empty commit). These specs are written to be pasted into the source by whoever has it.
