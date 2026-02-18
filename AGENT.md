# agent.md

## Working Style

- Prioritize **precision and correctness** over speed. I prefer **high precision over high recall** in code and decisions.
- Work in small, verifiable steps. Avoid big jumps.
- Keep me in the loop: after each meaningful change, summarize:
  - what you changed
  - why you changed it
  - what you plan to do next

## Decision-Making Rules (Hard Constraints)

- **Do not make architectural decisions without my approval.**
- **Do not make major implementation decisions without my approval.**
  - Examples: database choice, schema design, service boundaries, message formats, queue vs cron, caching strategy, auth approach, deployment strategy, data model, API shape.
- If you’re unsure whether something counts as “major,” assume it does and ask.

## Questions Policy

- Ask questions early and often. **Err on the side of asking too many questions.**
- When you ask, present:
  - 2–3 options
  - trade-offs (cost/complexity/performance/maintainability)
  - your recommendation (if you have one)

## Quality Bar

- Prefer simple, readable, maintainable solutions.
- No “random” implementation choices: every non-trivial choice should be justified or approved.
- If something is ambiguous or under-specified, pause and ask before coding further.

## Progress Tracking

- Maintain a root-level `progress.md` file as the single source of truth for execution status.
- Update `progress.md` after each meaningful step with:
  - current milestone status
  - completed tests
  - pending tests
  - next planned step
