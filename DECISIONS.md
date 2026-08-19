# Concourse — Design Decisions

## 1. Why this product and metaphor?

I designed Concourse as a departures board for campus placement drives because placement opportunities already behave like departures: each has a drive code, a company, a deadline, a status, and a decision to act before the window closes.

Students often receive placement information through emails, PDFs, screenshots, and portal notices. I wanted the home page to communicate three things immediately:

1. What opportunity is this?
2. How urgent is it?
3. What should I do next?

The departures-board metaphor gives urgency a familiar visual language without turning the product into another generic productivity dashboard.

## 2. Product interaction

I did not want the product section to be only a static mockup. I made the placement board interactive so the core idea can be experienced directly.

Users can add a placement drive, click a drive to view its details and next action, mark drives as done, archive or restore them, filter by All/Open/Today/Archived, and sort by deadline, company, or status. The “Next Departure” card also updates to the closest active drive and displays a live countdown.

Drive state is stored in the browser with `localStorage`, allowing added drives and their states to persist after refresh without pretending that a backend or database exists.

## 3. Trade-off

Under the assignment time limit, I chose a single HTML/CSS/JavaScript implementation instead of introducing a framework, authentication system, database, or backend.

This let me spend the available time on visual hierarchy, responsive behavior, interaction quality, and making the product representation genuinely functional. The trade-off is that the current data is local to the browser and is not shared between users or devices.

With a real week, I would build an ingestion layer that converts placement notices into structured drive entries, add persistent student-specific storage, and connect the board to real placement data.

## 4. AI usage and ownership

I used AI tools as a development assistant for implementation ideas, HTML/CSS/JavaScript iteration, debugging, and refinement. I did not treat generated output as a finished submission.

I personally reviewed and changed the product metaphor, copy, visual hierarchy, placement-board content, responsive layout, interaction model, countdown behavior, filtering, sorting, localStorage state, drive-detail flow, theme toggle, and easter egg.

I also tested the main interactions and responsive behavior so I can explain how the implementation works during the follow-up discussion.

The final design intentionally avoids fabricated testimonials, user counts, and company logos. The product claims are represented through the working interface rather than invented social proof.
