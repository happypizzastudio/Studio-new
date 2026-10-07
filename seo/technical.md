# Technical and site-wide changes

## 1. Organization schema (home page JSON-LD)

Current `@graph[0]` has `"name": "Happy Pizza Studio"` and a `knowsAbout` list. Add:

```json
"alternateName": "Happy Pizza Studio, startup branding agency",
"knowsAbout": [
  "Startup Branding", "Branding Agency", "Brand Identity Design", "Logo Design",
  "Design Systems", "SaaS Branding", "Brand Strategy", "Visual Identity",
  "Typography", "Merch Design", "Dev Tool Branding", "AI Company Branding"
],
"makesOffer": [
  { "@type": "Offer", "itemOffered": { "@type": "Service", "@id": "https://happypizza.studio/startup-branding-agency#service" } },
  { "@type": "Offer", "itemOffered": { "@type": "Service", "@id": "https://happypizza.studio/saas-branding-agency#service" } }
]
```

Keep `addressLocality: Bournemouth`. Don't fake a US address.

## 2. Internal links

The two new pages need links from pages Google already trusts. Minimum set:

| From | Anchor | To |
|---|---|---|
| Home, "What we do" block | `Branding for startups` | `/startup-branding-agency` |
| Footer (site-wide, next to Lab and RFC) | `Startup branding` · `SaaS branding` | both new pages |
| `/services`, intro | `SaaS branding` | `/saas-branding-agency` |
| `/about`, facts block or closing line | `branding agency for startups` | `/startup-branding-agency` |
| 7 SaaS case studies | `SaaS branding` | `/saas-branding-agency` |
| 7 other case studies | `branding for startups` | `/startup-branding-agency` |
| `/teardown`, "This is for you if" | `startup branding` | `/startup-branding-agency` |

Footer is the cheapest: one edit, 24 pages link.

## 3. Sitemap and llms.txt

- `sitemap.xml`: add both new URLs. `/startup-branding-agency` priority 0.9, `/saas-branding-agency` 0.8, changefreq monthly.
- `llms.txt`: under `## Services`, add a line for each new page using the same format as the existing entries.
- `/index.md` exists for the home page. If the site generates `.md` twins per page, let the two new pages have them too.

## 4. Things to leave alone

- Case study titles. They rank for the client name, which is the job.
- The visible home H1 `WE MAKE BRANDS THAT F**K.` It's the brand. The hidden span does the SEO work.
- Robots and canonical tags are correct on every page crawled.
- `Content-Signal: ai-train=no, search=yes, ai-input=yes` in robots.txt is fine as is.

## 5. Measurement

- Search Console: add the eight target queries as a saved filter. Record current position before any change ships.
- Check at 6 and 12 weeks. Don't edit titles between checks; you won't know what moved what.
- Treg: re-run the same export in January and compare.
