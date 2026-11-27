# Stellar Wave appeal checklist

Status: **prepared, not submitted**. This is an operator checklist, not evidence
that any repository was accepted, appealed or approved. Complete it in the
Drips Wave app; do not send appeals by email or other channels.

## Procedure from the current Drips docs

- Rejected repositories **cannot be re-applied**. Reconsideration happens only
  through **Maintainers → Orgs and Repos → Appeal** in the
  [Drips Wave app](https://www.drips.network/wave).
- First appeal opens **two weeks after rejection**. A declined appeal has a
  **one-month cooldown**. A repository may be appealed at most **three times**.
- Appeals ask what development work and improvements were made since rejection.
  "Substantive change" means meaningful code, project quality, activity, or a
  direct response to the review concerns. Polished documentation alone is not
  enough.
- Program rules and organizer discretion can change. Re-read the
  [terms](https://docs.drips.network/wave/terms-and-rules/) and
  [maintainer procedure](https://docs.drips.network/wave/maintainers/participating-in-a-wave/)
  in the app before acting.

At 27 November 2026 the Stellar Wave page showed **no active or upcoming Wave**
(Wave 11 ran 18–25 November). Confirm the next cycle in the app.

## Fields to fill from the app (not from public GitHub)

| Field | Value | Source |
| --- | --- | --- |
| Rejection date (UTC) | NOT RECORDED | Drips dashboard email/in-app notice |
| First appeal eligible from | NOT RECORDED | rejection date + 2 weeks |
| Appeals already used per repo | NOT RECORDED | Drips dashboard |
| Cooldown end (if previously declined) | NOT RECORDED | Drips dashboard |
| Org approval status | NOT RECORDED | Maintainers → Orgs and Repos |
| Next Wave dates | NOT RECORDED | Stellar Wave Program page |
| Repo application limits this cycle | NOT RECORDED | Application limits step |

## Per-repository appeal matrix

| Repository | Repo status in app | Appeal window | Substantive change to cite | CI evidence link | Result |
| --- | --- | --- | --- | --- | --- |
| `accordbridge-frontend` | NOT RECORDED | NOT RECORDED | [PR #27](https://github.com/accordbridge-labs/accordbridge-frontend/pull/27): critical Next.js patch + advisory CI | [app](https://github.com/accordbridge-labs/accordbridge-frontend/actions/runs/45937179372), [advisory](https://github.com/accordbridge-labs/accordbridge-frontend/actions/runs/45937179402) | NOT SUBMITTED |
| `accordbridge-backend` | NOT RECORDED | NOT RECORDED | [PR #24](https://github.com/accordbridge-labs/accordbridge-backend/pull/24): NestJS/zod patch + advisory CI | [app](https://github.com/accordbridge-labs/accordbridge-backend/actions/runs/45937180309), [advisory](https://github.com/accordbridge-labs/accordbridge-backend/actions/runs/45937180246) | NOT SUBMITTED |
| `accordbridge-contracts` | NOT RECORDED | NOT RECORDED | [PR #18](https://github.com/accordbridge-labs/accordbridge-contracts/pull/18): JS patch, reviewed Rust exception + advisory CI | [app](https://github.com/accordbridge-labs/accordbridge-contracts/actions/runs/45937179606), [advisory](https://github.com/accordbridge-labs/accordbridge-contracts/actions/runs/45937179592) | NOT SUBMITTED |

Do not convert a row to "submitted" until the app records it. Do not cite an
unmerged branch, a local test run, or a documentation-only change as the sole
substantive improvement.

## Evidence bundle to attach or reference

1. Merged PR URLs and **post-merge CI run URLs** for each repository.
2. Current `PROGRAM-READINESS.md` addendum with the actual commit SHAs tested.
3. Dependency advisory results: `docs/DEPENDENCY-ADVISORIES.md` in each repo,
   including the reviewed, expiring Rust exception — not a claim of an audit.
4. Deployment records in `accordbridge-contracts/deployments/` and the 18 October
   read-only readiness observation, with their timestamps and limits.
5. Hosted two-profile Freighter results **only if actually executed**; otherwise
   state clearly that H01–H26 remain NOT RUN and link `HOSTED-ACCEPTANCE.md`.
6. Licensing status from [CONSENT-OUTREACH.md](CONSENT-OUTREACH.md). Both
   outside contributions now have explicit Apache-2.0 grants with links and
   timestamps; cite those records. If a future grant remains unresolved, say so
   rather than implying retroactive consent.

## Claim boundaries

Use "experimental Stellar Testnet prototype", "valueless ABUSD", "unaudited",
and "no mainnet payment service". Never claim users, audits, hackathon history,
mainnet readiness, or hosted wallet acceptance that was not observed. The
Drips terms prohibit reward manipulation, multiple identities, and low-quality
or unreviewed LLM-generated submissions.
