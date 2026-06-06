---
title: SZL Anatomy 3D V2
emoji: 🫀
colorFrom: indigo
colorTo: red
sdk: static
pinned: false
license: apache-2.0
---

# SZL Anatomy 3D V2 — Human Substrate · Live Surfaces

A WebGL (Three.js r160) anatomical visualization of the SZL substrate rendered
as a **semi-transparent human body** with the 12 named capability organs placed at
anatomically correct positions inside the shell, plus PURIQ-formula + Lean-theorem +
live-receipt genome labels per organ, plus **6 live capability satellite orbs** wired into the body.

## What's live
- **6 capability surfaces polled every 30s** (command, memory, policy, operator console,
  vessels, drones) via their `/healthz` endpoints. Orb color = real status: green=UP, red=DOWN,
  gray=unknown. The bottom-left HUD shows per-surface dot, last poll time,
  commit SHA (last 8), and Λ where exposed.
- **Honest wires**: shipped/live wires render as glowing colored TubeGeometry with
  animated traveling particles; **not-yet-shipped wires render as gray DASHED lines
  with no flow** (no fake colors).
- **Λ-spine = exactly 13 vertebrae** (Doctrine v11, 2 sacred / 7 structural / 4 introspection).
- Live Λ score + declarations/axioms/sorries pulled from a11oy `/api/a11oy/v1/honest`
  and `/api/a11oy/v1/lambda`; falls back to the 2026-06-01 snapshot with a banner
  when the live endpoint is unreachable.

## Genome labels (ANATOMY UNIFICATION, 2026-06-02)
Each organ info panel declares its **Quechua name**, its **PURIQ formula** (F1–F23)
with PROVED / OPEN(sorry) / CONJECTURE-1 status, the **Lean theorem** it depends on, and
its **live receipt count** (sourced from the `SZLHOLDINGS/uds-spans-receipts` ledger:
50 total + 5 SLSA-chain attestations). The panel is **mobile-first**: on screens ≤720px it
becomes a full-width slide-up sheet with large tap targets.

## Controls
Orbit (drag) · Zoom (scroll) · Explode/Reassemble · Pulse · Reset · Hide body · Hide surfaces · per-wire toggles.

## Honesty
Doctrine v12: 749 declarations, 14 unique axioms, 163 sorries, 13/13 Λ-axes.
Uniqueness remains **Conjecture 1** (NOT a theorem) — see the Λ bounty at
`github.com/szl-holdings/lutar-lean/blob/main/BOUNTY.md`. Surfaces not yet deployed
render red/PENDING by design, never faked. Receipt counts are real ledger snapshots,
not fabricated; surfaces with no deployed presence show 0.

Built via `HfApi.create_commit` (direct), not GitHub Actions.

— Yachay (CTO), SZL Holdings
