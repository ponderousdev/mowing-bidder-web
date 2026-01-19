Follow the repository’s AGENTS.md instructions (and any inherited ~/.codex/AGENTS.md guidance) as highest priority. If AGENTS.md exists, comply with it. If it does not exist, proceed using the “Working Agreements” below (do NOT create a backend).

# Goal
Build a fast, static, pre-launch landing page for “Mowing Bidder” using Astro. No backend. No database. No form functionality yet (we can add later). The page should be conversion-focused and make it easy to understand the product in <10 seconds.

# Working Agreements (AGENTS.md style)
## Definition of Done
- Astro project runs locally and builds successfully.
- Landing page is responsive, polished, accessible, and loads fast.
- All copy is written (no lorem ipsum, no placeholder sections).
- CTA buttons are present but (for now) do not submit data. They can either:
  (A) open a simple modal that says “Email signup coming soon”, OR
  (B) scroll to a “Get Updates” section with a note that signup is coming soon.
  Choose the simplest option and implement it cleanly.
- `npm run build` succeeds.

## Tech Stack
- Astro + TypeScript
- Tailwind (preferred) OR plain CSS (pick one and implement fully)
- No backend, no external services, no analytics scripts (only optional console-log stub).

## Commands to Run (must run and fix)
- npm install
- npm run build
- npm run dev (smoke test)

# Implementation Instructions
1) Create a new Astro site (or use existing) and add a single landing route at `/`.
2) Use componentized structure:
   - `src/components/` for sections (Hero, HowItWorks, Benefits, DemoMock, FAQ, Footer).
   - `src/layouts/` for a base layout with SEO meta tags.
3) Ensure accessible headings, keyboard focus states, and good contrast.

# Page Content (write the copy, no placeholders)
## Brand
- Product name: Mowing Bidder
- Tagline: “Instant mowing quotes.”

## Sections (in this order)
1) Sticky top nav
   - Left: “Mowing Bidder” text logo
   - Right: CTA button “Get Updates” (scrolls to final CTA section)

2) Hero
   - Headline emphasizing speed + simplicity:
     Example direction: “Quote mowing jobs in a few seconds.”
   - Subheadline:
     “Enter an address. Get a weekly + bi-weekly price based on property square footage and your pricing formula.”
   - Primary CTA: “Get Updates” (scroll)
   - Secondary CTA: “See how it works” (scroll to How it works)

3) Social proof band (light)
   - “Built by lawn care operators”
   - 3 short credibility bullets:
     - “Fewer back-and-forth texts”
     - “Consistent pricing every time”
     - “Faster quotes → more closed jobs”

4) How it works (3 steps)
   - Step 1: “Enter the address”
   - Step 2: “We find the property size”
   - Step 3: “Your formula generates weekly + bi-weekly pricing”

5) Why Mowing Bidder (6 benefit cards)
   - Speed: “Quote in seconds”
   - Consistency: “Formula-based pricing”
   - Convenience: “Send prices on the spot”
   - Less admin: “Reduce back-and-forth”
   - Better win-rate: “Respond before competitors”
   - Simple setup: “Works with how you already price”

6) Who it’s for
   - Owner-operators
   - Office/admin teams
   - Estimators + sales staff
   Include 1–2 sentences describing each.

7) Demo section (interactive mock, front-end only)
   - An address input (does not need real autocomplete)
   - A “property sqft” output that can be:
     - hardcoded after “Generate quote”, OR
     - randomly generated in a believable range (e.g., 2,000–20,000 sqft)
   - Show example weekly + bi-weekly price outputs derived from a simple demo formula.
   - Clear note: “Demo only — real app pulls accurate sq ft + your pricing formula.”
   - Keep the demo logic entirely client-side (no API calls).

8) Pricing teaser
   - “Early access will be affordable.”
   - “Join the updates list to be first in line.” (no form yet)

9) FAQ (6 Qs + concise As)
   - “Where does the square footage come from?”
   - “Can I use my own pricing formula?”
   - “How fast is it?”
   - “Will it integrate with CRMs later?”
   - “When does it launch?”

10) Final CTA section (Get Updates)
   - Headline + short copy
   - Implement the chosen “no-form” behavior:
     Option A (recommended): button opens modal: “Email signup coming soon. Check back soon.”
     Add a secondary link: “Contact us” → `mailto:hello@example.com` placeholder.

11) Footer
   - Copyright
   - Simple links: Privacy (placeholder page optional), Contact (mailto)

# SEO
- Set title: “MowingBidder — Instant mowing quotes”
- Meta description: emphasize address → weekly/bi-weekly pricing in seconds
- Open Graph tags with a simple default image path (can be a placeholder asset you create, e.g. `/og.png`)

# Performance & Polish
- Mobile-first spacing and typography
- Sticky nav, smooth scrolling, subtle hover/focus states
- No heavy animation libraries

# Deliverables
- Full Astro project code
- Clean structure and comments where helpful
- README: how to run dev + build, and “Things to customize” (mailto address, pricing copy, OG image)

Now implement the landing page in Astro accordingly.
