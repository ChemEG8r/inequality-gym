# Inequality Gym

Randomized inequality practice for VJ, modeled on his Inequality Test Review
(Periods 1 & 5). Every quiz is 12 freshly generated problems — new numbers
every time, effectively never the same problem twice:

- One-step inequalities (add/subtract, and multiply/divide including the
  divide-by-a-negative FLIP)
- Two-step inequalities (kx + a and x/k − a forms)
- Distributive form, like −4(x + 2) > −4
- Number-line graphs (pick the right open/closed dot and direction) and
  "possible value" questions
- Word problems: wages ("at least"), rentals ("less than"), savings dropping
  ("below" — flip trap), and pet diets ("at most" — flip trap)

Answers are entered test-style: pick the sign (< ≤ > ≥) and type the number.
Instant grading with step-by-step explanations; every generated problem is
machine-verified against its own inequality. History records exact misses,
synced across devices via `/api/scores` on Cloudflare Pages (Workers KV bound
as `SCORES`), falling back to per-device localStorage elsewhere.

Deploy: `npx wrangler pages deploy . --project-name inequality-gym --branch main`
(needs `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID`).
