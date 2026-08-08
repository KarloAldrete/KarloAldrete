# Karlo Aldrete

Product engineer in Tijuana, MX (US Pacific). I build 0-to-1 products with agents in
the loop, then measure whether the architecture actually pays for itself.

## Now

- **[frameshi](https://frameshi.com)** — cinematic product videos filmed from your live
  product, not a rebuilt demo. Our engine takes ownership of Chromium's clock, so the same
  screenplay produces byte-identical frames on every run, and clones any live URL into a
  self-contained pack in 12–26s.
- **[Habitae](https://habitae.mx)** — PropTech for independent real-estate agents in
  Mexico: [agentes.habitae.mx](https://agentes.habitae.mx) for agents,
  [habitae.mx](https://habitae.mx) for buyers, one backend underneath, ~$5/mo to run.
- **Open source contributor** to [PostHog Code](https://github.com/PostHog/code) and
  [posthog-js](https://github.com/PostHog/posthog-js) — performance work, always with a
  reproducible benchmark attached.

## Numbers, not adjectives

- **Streamed markdown rendering** — killed an O(n²) re-parse on every token: 8,000 chars
  from 1,361 ms to 81 ms. Merged as [PostHog/code#2716](https://github.com/PostHog/code/pull/2716).
  [Writeup →](https://karloaldrete.xyz/smooth-cheap-agent-streaming)
- **Session replay main thread** — time-sliced rrweb snapshots: a single 7,789 ms freeze
  became 110 slices, 93 ms worst case, wire output identical across 152,036 nodes.
  [posthog-js#4233](https://github.com/PostHog/posthog-js/pull/4233); the hardening PR that
  carries it forward builds on that branch with 15 of my commits.
  [Writeup →](https://karloaldrete.xyz/a-recorder-is-a-guest)
- **Renderer memory + open time** — 1.1 s freeze → 198 ms, 713 MB → 61 MB across four big
  sessions. Shipped via [PostHog/code#3063](https://github.com/PostHog/code/pull/3063).
  [Writeup →](https://karloaldrete.xyz/paint-the-tail-first)
- **Habitae's maps layer** — $680/mo vendor bill → $0, map-first discovery intact.
- **frameshi cloud renders** — 47.5 s of 1080p60 in 81 s for $0.028, down from ~29 min.
  [Writeup →](https://karloaldrete.xyz/clone-the-web-then-film-it)

## Rust, when the problem needs it

**[universal-proxy](https://github.com/KarloAldrete/universal-proxy)** — a `no_std`,
zero-heap Solana program (Pinocchio, ~18 KB SBF) that runs N arbitrary swaps atomically
with an on-chain profit guard. I security-audited it myself and shipped the findings with
it: a `MaybeUninit` undefined-behaviour bug, an arbitrary-CPI hole, and missing owner
checks.

## Writing

I document what I build, with the evidence, at
**[karloaldrete.xyz](https://karloaldrete.xyz)** — ten writeups, every claim linked to the
benchmark behind it.

---

karloaldretedev@gmail.com · [LinkedIn](https://www.linkedin.com/in/karloaldretedev/)
