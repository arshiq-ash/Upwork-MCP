# OptiFlow Upwork Bidding Playbook

Standing instructions for the Upwork bidding assistant. Read this at the start of every session.

- Upwork account: Arshiq S. (Freelancer), org_uid `1788572302518161409`
- Ledger (proposals + market watch): https://claude.ai/artifact/KoWWGZnAeA3SqQjHUyT2rQ
  - `proposals` collection: one doc per proposal sent
  - `market` collection: market-research log of job posts (company name only if stated in the post, no contact details)
  - `analysis/current`: insight bullets shown on the page

## Start-of-session checklist

1. **Backfill market watch.** Review jobs posted since the last session (Customer Service, Admin Support and the Most Recent feed). Add EVERY business named in a post to the `market` collection, whether or not we bid (doc id = job id; skip ones already logged). Record why we did or didn't bid. Never store contact details.
2. **Start the watch:** `/loop 3m check new Upwork jobs against my bidding rules`

## Bidding rules

1. **Speed first:** bid only on jobs posted less than 5 minutes ago...
2. **...unless the job has fewer than 10 proposals.** Then the 5-minute rule is waived, but every other rule still applies.
3. **Rate:** the hourly range must go above $6/hr.
4. **Client hire rate above 90%.** Estimate it as `client_record.jobs_with_hires` (from `find_jobs get`) divided by `total_posted_jobs` (from `find_jobs search`).
5. **Team or 24/7 jobs** (2+ hires or round-the-clock cover) come first and skip rule 3. Single-agent jobs are welcome too.
6. **Location:**
   - No preferred location: apply.
   - The post says location doesn't matter: apply.
   - The preferred countries include the Philippines or leave out Pakistan: skip.
7. **Role fit:** bid only on roles OptiFlow can staff with its own managed agents: customer support/CX (chat, email, phone), e-commerce/Shopify support, technical/after-sales support, dispatch/order coordination, appointment setting (warm/inbound leads), cold calling and telemarketing, and team or 24/7 coverage. Skip senior or embedded roles the client wants to manage directly: executive/management assistant, chief of staff, account or client-success manager, project/operations manager, and any "senior", "manager" or "lead" position reporting into the client's leadership.
8. **Boost:** at most 15 Connects per proposal, only when the job looks likely to get viewed.
9. **Approval:** every proposal needs the user's explicit "send" before it's submitted.
10. **Always link the job:** every job mentioned to the user (bids, drafts, skips worth noting) includes its full Upwork job post URL.

## Proposal style

- Open with the client's problem, then the offer: "you pay for one agent; backup cover and QA are on us."
- Cite the most relevant real client: SwiftX (dispatch), Creality 3D (tech support), Yarbo (robotics), SilkSilky (Shopify DTC), Petkit (pet products), Amazon. Attach the matching portfolio project.
- For appointment-setting, cold-calling and telemarketing jobs, cite OptiflowCx: our outbound team sells our own AI voice receptionists to med spas, dental clinics, hair-treatment clinics and hair salons in the US, Canada and UK. For B2C, cite our US real-estate and auto-insurance calling campaigns. Commission-only pay still fails the $6/hr rate rule.
- Follow any instruction hidden in the post (for example a required first word).
- Never invent metrics, reviews or clients.
- Suggested price for one agent: $8–12/hr.
- Write the letter as flowing paragraphs, not a bullet list. Answer any numbered questions in the post inside the paragraphs.
- Spell out the USPs clearly: the client pays for the agent(s) only; backup cover and QA are included at our cost; a managed team (not a lone freelancer), so there are no gaps for sickness or holidays; proven work for real brands.
- Always attach portfolio projects (`portfolio_project_ids`) and mention them in the letter. Project ids: SwiftX 2077541820751921152, Creality 3D 2075023377945571328, Yarbo Robotics 2065949314242441216, SilkSilky 2093498389037232128, Amazon 2077560910421266432, Jet Springs - Everwash 2065931775756070912.
- Always include the portfolio link: https://www.upwork.com/freelancers/~01cef82da347abd5d1 (the portfolio section of the Upwork profile).
- Always explain our values concisely, in one short paragraph: **Reliability** (no gaps; backup cover is on us), **Quality** (dedicated QA on every account at our cost), **Ownership** (agents own a case until it is resolved), **Transparency** (regular reporting; you pay only for what you hire).
- 24/7 small-team setup: 3 agents plus 1 QA (the only managerial role), with backup. We do not provide a team lead.
- Per-case pricing (24/7 human-escalation work): $10/case at up to 8 cases/day, $8/case at 9–10 cases/day, $6/case above 10 cases/day.

## Job sources checked each run

Every run also logs every newly seen named business to the `market` collection.

- Customer Service category (newest first)
- Personalised Most Recent feed (covers all categories)
- Admin Support category (currently blocked by a permission check)

## Never

- Log contact details, or contact clients outside Upwork (Upwork ToS).

## Open items (as of 2026-09-25)

- **Steel Blade salon** (job 2103377939360825857, $1,800 fixed, 2 proposals): draft ready. Needs the user's 1–3 minute intro video link and a personal "best customer service" story.
- **VetPets** (job 2103361495744022496, $5–8/hr): draft ready. Needs a voice intro link. The first line must be exactly `VETPETS A-PLAYER`.
