# sales-copy

An agent skill that writes buyer-facing conversion assets: long-form sales pages, landing pages,
launch and abandoned-cart email sequences, Facebook, Google and LinkedIn ad variations, product
descriptions, VSL and webinar scripts, upsell flows and testimonial frameworks. Each asset comes
with a headline set, subheadline, body in section order and one call to action, built from the
product, the buyer, their awareness level and the conversion goal. It writes the questions to ask a
real customer instead of inventing a quote, and it replaces conversion-rate promises with a metric
and a first test worth running.

Install: `npx skills add arm-pz/sales-copy --skill sales-copy`

Ask it things like:

- "Write a sales page for my course. It is $290, buyers are freelance designers, they know
  solutions like this exist."
- "I need a launch email sequence for a physical product dropping on the 14th."
- "Give me six Facebook ad variations for a booking tool aimed at dentists."
- "This landing page gets clicks and no signups. What is the one thing to change first?"

## What you get

| Mode | Output |
|---|---|
| Sales page | Page in section order (lead, problem, mechanism, offer, proof, guarantee, close, FAQ) plus a headline set to test |
| Launch email sequence | Beat-by-beat emails: subject, preview text, body, one CTA each |
| Ad variations | Angle-by-length grid for Meta, Google and LinkedIn, with limits and creative notes per variant |
| Landing page | Rewritten page plus a named friction section and the first change to test |
| Product description | Short, long and store-field versions, specs kept exactly as supplied |
| VSL script | Time-coded script with `[on-screen: ...]` cues |
| Webinar presentation | Sectioned run sheet with timings, transition and close |
| Upsell flow | Thank-you page, upsell, fallback and confirmation copy |
| Abandoned-cart emails | Sequence per drop-off point, with timing slots for the user to set |
| Testimonial framework | Interview questions and a blank structure with `[customer name]` and `[result]` slots |

Every asset ends with `Gaps` (the figures only you can supply) and a `Test note` (the metric and the
first hypothesis).

## Not for

Copy that builds an audience rather than taking a payment: posts, threads, LinkedIn content,
YouTube or TikTok scripts, newsletters, calendars and repurposing chains go to `platform-content`.
Text you already wrote that needs shortening, polishing or your own voice back goes to `wordsmith`.
Pricing, offer structure and go-to-market decisions go to `strategy-memo`; SEO clusters across
competing pages go to `keyword-guard`; the numbers from a finished test go to `data-readout`.

## Honest by design

No invented testimonials, names, results, benchmarks, revenue figures or competitor facts. Where a
deliverable needs a number you have not supplied, you get `[metric — supply this]` and a line in
Gaps. Health, earnings and income claims are flagged for substantiation instead of softened. Ad
platform limits and review rules are written as things to check against current docs, not as
durable facts.

## Install

```
npx skills add arm-pz/sales-copy --skill sales-copy
```

Or copy `skills/sales-copy/` into your agent's skills directory (`.claude/skills/`,
`.agents/skills/`, `.cursor/skills/` or `.qoder/skills/`). With Claude Code plugins,
`.claude-plugin/plugin.json` makes the repo installable as a plugin; add it to your marketplace
repo as an entry pointing at `arm-pz/sales-copy`.

## Structure

```
sales-copy/
├── README.md
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   └── sales-copy/
│       ├── SKILL.md                 # intake, modes, output format, quality bar, handoffs
│       └── references/
│           ├── assets.md            # page sections, email beats, ad grid, VSL and webinar skeletons,
│           │                        # upsell and cart flows, testimonial framework, what to measure
│           └── awareness.md         # awareness level to message, headline angle, proof and CTA map
└── tests/
    └── test-prompts.md
```

## Tests

`tests/test-prompts.md` lists triggering and honesty cases, including the near-misses that belong
to `platform-content` and `wordsmith`. They are written down to be run against the suite by hand;
no automated trigger run has been executed.
