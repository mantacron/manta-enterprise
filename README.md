# Manta Enterprise — Landing Page

Marketing site for [Manta Enterprise](https://mantacron.github.io/manta-enterprise/), the
commercial edition of [Manta](https://github.com/mantacron/manta), built by
[Mantacron](https://github.com/mantacron).

## What it covers

- What Manta is, and the enforcement claim: every commit reviewed, every bypass recorded
- **The data boundary**, second on the page rather than in a footer — what the control plane
  receives and what it never receives. It is the objection that decides an enterprise
  evaluation, so it is answered before it is asked
- The pipeline: three agents at commit, up to nine routed at push, evidence after
- Free edition vs Enterprise — 20 agents / 21 commands against 33 / 32, eleven of them served
  from the control plane under an active subscription
- The four capability areas: compliance, risk and governance, security depth, spec and architecture
- An evidence bundle, and what it discloses about its own limits
- Contact form for enterprise enquiries

## House rules for edits

- **The palette is the control plane's, not a second brand.** `#02274a` is the ray in the logo
  art and `#43c0ca` the constellation dots, both sampled from the artwork. Navy carries
  structure and action; teal is reserved for accent and focus, so it keeps its meaning. Do not
  set a headline in teal.
- **The terminal panel is text, not a screenshot** — it stays sharp at any zoom, is selectable,
  and cannot drift out of date the way a PNG of a CLI does.
- **Every number on this page is checkable against the product.** Agent counts come from
  `.claude/agents/` in each edition; the blocking rule (a CRITICAL blocks alone, a warning
  blocks only when a second agent independently raises it) is the enterprise reporter's
  consensus rule. If a claim here cannot be traced to the code, it does not belong on the page.
- Claims about what leaves a customer's machine must match `docs/TELEMETRY.md` in the
  enterprise repo.

## Stack

Static HTML/CSS — no build step, no dependencies. Edit `index.html` directly. `contact.js`
composes a `mailto:` from the form; nothing is submitted to a server.

## Deploying

GitHub Pages, via `.github/workflows/`. Push to `main` and it updates automatically.
