# Project quality and Wave readiness

Reviewed 18 October 2026. This is an engineering assessment, not a finding from
Drips or a guarantee of program acceptance. The rejection notice names broad
criteria and does not establish a repository-specific cause.

## Update — 27 November 2026

This addendum records a later verification pass. It does not change the
18 October findings above; it supersedes only the stale counts and the status
of the remaining prerequisites. It is an engineering assessment, not a Drips
decision.

**Local verification against current `main` (27 November 2026):**

| Suite | Result | Command |
| --- | --- | --- |
| Frontend unit | 16 passed | `npm test` |
| Frontend browser | 48 passed (desktop + mobile) | `npm run test:e2e` |
| Frontend build / typecheck | passed | `npm run build`, `npm run typecheck` |
| Backend, with isolated PostgreSQL | 28 passed | `npm test` |
| Backend API contract | no drift | `npm run docs:api`, `git diff --exit-code docs/openapi.json` |
| Contracts JS tooling | 14 passed | `npm test` |
| Contracts Rust (8 escrow + 5 token) | 13 passed | `cargo test --locked --workspace` |
| Contracts formatting | passed | `cargo fmt --all -- --check` |

The 18 October counts (18 backend, 9 frontend unit, 16 browser, 10 contract)
were correct at that commit but are **no longer current**: later merged PRs
expanded those suites. The last CI runs visible on `main` at this review were
[frontend, 26 October](https://github.com/accordbridge-labs/accordbridge-frontend/actions/runs/40297788284),
[backend, 30 October](https://github.com/accordbridge-labs/accordbridge-backend/actions/runs/41108083705),
and [contracts, 24 October](https://github.com/accordbridge-labs/accordbridge-contracts/actions/runs/40082567711),
all successful. The 27 November results above were produced locally, not in
GitHub Actions, and must not be described as CI evidence until a change is
merged and its workflow run is linked.

**Dependency advisories found in this pass:** the pinned frontend `next@16.4.0`
had a critical advisory, the backend had high advisories in
`@nestjs/platform-express` and `zod`, and the contracts JavaScript tree had a
high `follow-redirects` advisory. Compatible patched versions were prepared on
the `fix/dependency-advisories` branches in all three repositories, together
with a separate least-privilege advisory workflow and triage documentation in
`docs/DEPENDENCY-ADVISORIES.md`. After those updates, `npm audit` reports zero
advisories in all three repositories. `cargo audit` reports one transitive
advisory (`RUSTSEC-2026-0387`, crypto-bigint via pinned soroban-sdk) recorded as
a reviewed exception expiring 27 December 2026 in
`accordbridge-contracts/.cargo/audit.toml`. These changes were **prepared but not
merged** at the time of this addendum; no CI links or hosted evidence exist for
them yet.

**Activity gap:** the newest merged commits at this review were 30 October
(backend), 26 October (frontend) and 24 October (contracts). A Drips appeal
should rely on substantive change since the rejection, so any prepared work
must be reviewed, merged and linked with its actual CI run before submission.

See [APPEAL-CHECKLIST.md](APPEAL-CHECKLIST.md),
[CONSENT-OUTREACH.md](CONSENT-OUTREACH.md) and [WAVE-BACKLOG.md](WAVE-BACKLOG.md)
for the remaining process work. None of these documents records a submitted
appeal, a hosted wallet run, or a contributor's license grant.

## Findings from the source

The three repositories already implement one connected Stellar Testnet product:
agreements and participant sessions, signed transaction preparation, reconciliation,
deliverable review, and first-milestone Soroban escrow. Historical deployment and
transaction records are public. The backend history begins on 8 October 2026;
short history is an observation, not proof of why the application was rejected.

At review time, the organization profile, contribution policy and security policy
still described planning-only or private repositories despite the implementation.
Backend and frontend lacked CI workflows. All three READMEs said license selection
was pending and GitHub detected no license. Private vulnerability reporting was
disabled on all three application repositories; it was enabled during this review.

The implementation checks uncovered stale release eligibility after work approval:
the frontend refreshed its escrow data only when the project ID changed. Connected
browser tests reproduce that defect and exercise the correction. Recovery browser
tests also needed selectors that distinguish application errors from Next.js's
route announcement.

## Merged improvements and verification

The companion changes were merged: [backend #10](https://github.com/accordbridge-labs/accordbridge-backend/pull/10),
[frontend #13](https://github.com/accordbridge-labs/accordbridge-frontend/pull/13),
[contracts #8](https://github.com/accordbridge-labs/accordbridge-contracts/pull/8), and
[organization #2](https://github.com/accordbridge-labs/.github/pull/2).

Post-merge CI passed for [backend](https://github.com/accordbridge-labs/accordbridge-backend/actions/runs/39124552087),
[frontend](https://github.com/accordbridge-labs/accordbridge-frontend/actions/runs/39124732213), and
[contracts](https://github.com/accordbridge-labs/accordbridge-contracts/actions/runs/39124556117).
The suites contain 18 backend tests, 9 frontend unit tests, 16 browser tests and
10 contract tests; builds and the contract reproducibility check also passed.

- Backend: authenticated, throttled, cached read-only deployment readiness; explicit
  network/configuration/code/availability results; tests and generated API schema;
  PostgreSQL integration CI and API drift checking.
- Frontend: refresh server-owned release eligibility after project changes; repair
  ambiguous recovery selectors; build, unit, browser and connected PostgreSQL CI.
- Contracts: additional adversarial tests for funded-state authorization, outsider
  acceptance, duplicate refund votes, both refund orders and terminal-state replay.
  Contract runtime behavior and historical deployment records are unchanged.
- Organization: accurate scope, contribution/testing instructions, bug reporting,
  private vulnerability reporting, and evidence requirements.

A read-only RPC check of the public deployment configuration returned `ready` at
2026-10-18T11:40:55.494Z. This proves only that the checked Testnet network, token
instance and pinned code were readable and matched then. It does not prove hosted
wallet flows, customer adoption, security audit status or continued availability.

## Reference organization

[Lumeeena](https://github.com/Lumeeena) provides useful examples of repository
boundaries, setup documentation, CI, contributor instructions and traceable fixes.
Its [frontend CI](https://github.com/Lumeeena/lumina-frontend/blob/main/.github/workflows/ci.yml)
includes browser and backend integration checks; its
[contract history](https://github.com/Lumeeena/lumina-contracts/commits/main/)
records concrete registry improvements. These practices informed this work.
No Lumeeena product code, contributors, history or branding was imported.
Its acceptance status and the reasons for that decision were not independently verified.

## Remaining prerequisites

1. Resolve outstanding rights records. The backend, frontend, contracts and
   organization resources have adopted MIT with matching contribution terms;
   frontend and contracts adoption followed explicit maintainer direction. The
   [licensing inventory and consent drafts](LICENSING-REVIEW.md) identify
   frontend PR #12 and contracts PR #7 as outside contributions without an explicit
   license grant in the inspected public records. Permission for those contributions
   has not been independently verified; no contributor messages were sent.
2. Keep evidence tied to actual commits and distinguish local, mocked, hosted and
   live-chain checks. A limited hosted preflight passed on 18 October 2026, checking
   public rendering, authentication boundaries, secure cookies, separate sessions,
   persisted agreement acceptance and authenticated readiness. It used no wallets
   or tokens. Two synthetic accounts and one unfunded project remain as test data.
3. Complete the frontend's hosted two-participant Freighter acceptance runbook,
   recording genuine test transactions. Automated browser tests use synthetic chain
   snapshots; they do not drive the wallet extension.
4. Continue real maintenance and user validation. Storage restoration, bounded
   background reconciliation, operational security and financial/dispute policy
   remain existing roadmap work. Testnet readiness is not production readiness.
5. Prepare an appeal using actual merged improvements, CI links, deployment evidence
   and remaining limitations. Never invent activity, users, audits or hackathon history.

## Program procedure

The [Drips terms](https://docs.drips.network/wave/terms-and-rules/) give organizers
selection discretion and prohibit reward manipulation and low-quality, untested
AI-generated submissions. Assistance does not remove the maintainer's obligation
to understand and review contributions.

The [maintainer procedure](https://docs.drips.network/wave/maintainers/participating-in-a-wave/)
requires rejected repositories to appeal through Maintainers → Orgs and Repos,
after substantive changes. The first appeal opens two weeks after rejection;
subsequent declined appeals have a one-month cooldown and a repository has at most
three appeals. Rejected repositories cannot simply re-apply. Confirm the current
rules and rejection date in the app before using an appeal. No appeal was submitted
as part of this engineering work.
