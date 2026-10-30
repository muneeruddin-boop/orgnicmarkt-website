# Context

Read this first in every new chat or Claude Code session.

## What we're building
A website for Orgnicmarkt: an online marketplace for organic spices and textiles, bought directly from the producers who make them.

- **What we do:** customers order organic spices and textiles straight from manufacturers and producers. These are the only two categories for now; don't show or mention other product types on the site. Every order invests in the communities behind those products and earns the customer Respect Points, which they can redeem when they visit the countries and communities their products come from.
- **Who it's for:** households who want their everyday shopping to do some good. They are health-conscious and environment-conscious, care about workers' rights and not harming the environment, and want to make a positive impact. Launching in Germany first, built to grow worldwide.
- **What makes us different:**
  - One third of the profits (not revenue) goes back to producer communities as investment in energy infrastructure. The rest is reinvested in growing the platform and supply chain, so the impact grows with it. Always say "profits" on the site, never "sales" or "revenue".
  - Direct connection with producers, no anonymous supply chain.
  - Respect Points: a reward that brings customers to the places their products come from.

## Our Git
- Design system: github.com/muneeruddin-boop/orgnicmarkt-design
  Tokens (`assets/tokens.css`), components (`assets/components.css`), the storybook (`storybook.html`), the design skill (`SKILL.md`), and page designs in `prototypes/`.
- Website: github.com/muneeruddin-boop/orgnicmarkt-website
  The pages Claude Code builds. `main` is the live site, `staging` is the rehearsal, every change goes through a pull request.
- The design system repository is the source of truth. The website only uses what is in it.

## Stack
Plain HTML, CSS and a little JavaScript. No build step. Hosted on Netlify, connected to the website repository. The contact form uses Netlify Forms.

## Pages
`index.html` (home) · `pricing.html` · `about.html` · `contact.html` · `thanks.html` (after the form)

## How we work: the loop
1. Design in Claude chat: prototype the page, try versions, check phone and desktop.
2. Update the design system: anything reused or a rule goes into tokens, components, storybook and SKILL.md. The page goes into `prototypes/`.
3. Push the design system repository to GitHub.
4. Claude Code, in the website repository: get the latest design system, update tokens and components to match, build the page from its prototype, on a new branch.
5. Test on localhost: phone and desktop, every link, Lighthouse. Not OK? The report goes back to Claude chat.
6. Pull request, check the Netlify preview link, merge. The site goes live.

## Rules for Claude Code
- Never make a design decision. Colours, fonts, spacing, layout, copy, motion and imagery are decided in Claude chat and live in the design system or the prototype.
- If something isn't defined there, stop and ask. Offer two or three options with a short reason for each. Don't pick one yourself.
- Use only tokens from `assets/tokens.css` and components from `assets/components.css`. Never hard-code a value.
- Work on a branch, never directly on `main`.
- After building, run the site locally, test phone and desktop, and report what you built, what you tested and every open question, before opening a pull request.

## Current state
- Done: design system and website repositories set up from the starter kit. CLAUDE.md filled in.
- Next: design the home page in Claude chat (references, three directions, prototype).
- Later: the kit's pages (pricing, about, contact) are placeholders. A marketplace will likely need shop, producers and Respect Points pages; decide these in Claude chat before building.
