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
expanded those suites. Immediately before the 27 November changes, the last CI
runs on `main` were
[frontend, 26 October](https://github.com/accordbridge-labs/accordbridge-frontend/actions/runs/40297788284),
[backend, 30 October](https://github.com/accordbridge-labs/accordbridge-backend/actions/runs/41108083705),
and [contracts, 24 October](https://github.com/accordbridge-labs/accordbridge-contracts/actions/runs/40082567711),
all successful. The 27 November results above were first produced locally; the
post-merge workflow runs linked below now provide the corresponding CI
evidence for the merged commits. Keep the two categories distinct when citing
them.

**Dependency advisories found in this pass:** the pinned frontend `next@16.4.0`
had a critical advisory, the backend had high advisories in
`@nestjs/platform-express` and `zod`, and the contracts JavaScript tree had a
high `follow-redirects` advisory. Compatible patched versions were merged with
a separate least-privilege advisory workflow and triage documentation in
`docs/DEPENDENCY-ADVISORIES.md`:
[frontend PR #27](https://github.com/accordbridge-labs/accordbridge-frontend/pull/27),
[backend PR #24](https://github.com/accordbridge-labs/accordbridge-backend/pull/24),
and [contracts PR #18](https://github.com/accordbridge-labs/accordbridge-contracts/pull/18).
After those updates, `npm audit` reports zero advisories in all three
repositories. `cargo audit` reports one transitive advisory (`RUSTSEC-2026-0387`,
crypto-bigint via pinned soroban-sdk) recorded as a reviewed exception expiring
27 December 2026 in `accordbridge-contracts/.cargo/audit.toml`.

**Post-merge CI evidence (27 November 2026, all successful):**

| Repository | Application CI | Advisory CI | Merged commit |
| --- | --- | --- | --- |
| Frontend | [run 45937179372](https://github.com/accordbridge-labs/accordbridge-frontend/actions/runs/45937179372) | [run 45937179402](https://github.com/accordbridge-labs/accordbridge-frontend/actions/runs/45937179402) | `3b4d13acc3f7` |
| Backend | [run 45937180309](https://github.com/accordbridge-labs/accordbridge-backend/actions/runs/45937180309) | [run 45937180246](https://github.com/accordbridge-labs/accordbridge-backend/actions/runs/45937180246) | `6877e09f8bd0` |
| Contracts | [run 45937179606](https://github.com/accordbridge-labs/accordbridge-contracts/actions/runs/45937179606) | [run 45937179592](https://github.com/accordbridge-labs/accordbridge-contracts/actions/runs/45937179592) | `ca37993c2afe` |

The preparation documents and the evidence addendum were merged in
[organization PR #8](https://github.com/accordbridge-labs/.github/pull/8),
commit `e00bcdaf9905`. These runs establish current repository checks only.
They do not prove hosted wallet acceptance, user adoption, an audit, or
continued availability of the public deployment.

**License change:** on 27 November 2026 the maintainer replaced MIT with the
Apache License 2.0 across all four repositories, added root `NOTICE` files,
updated package/Cargo metadata and documentation, and sent new Apache-2.0
consent questions to the two outside contributors (recorded in
[CONSENT-OUTREACH.md](CONSENT-OUTREACH.md)). @Oluwa-Laughter replied "Yes, permission granted" to the **MIT** request at
09:34 UTC, before the Apache-2.0 follow-up at 22:41 UTC, and then replied
"Hi @hameedx01 permission granted good move" at 22:57 UTC in direct response to
the Apache-2.0 request ([reply](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7229757636)).
Frontend PR #12 is therefore granted under both licenses; contracts PR #7
remains AWAITING. See
[LICENSING-REVIEW.md](LICENSING-REVIEW.md) and
[CONSENT-OUTREACH.md](CONSENT-OUTREACH.md). The earlier MIT requests must not be
cited as Apache-2.0 grants.

License adoption was merged as
[frontend #28](https://github.com/accordbridge-labs/accordbridge-frontend/pull/28)
(`fd3704f7ffbb`),
[backend #25](https://github.com/accordbridge-labs/accordbridge-backend/pull/25)
(`32a2bc093810`),
[contracts #19](https://github.com/accordbridge-labs/accordbridge-contracts/pull/19)
(`a0f53875ac4c`) and
[organization #12](https://github.com/accordbridge-labs/.github/pull/12)
(`55129a51cd70`). Post-merge checks succeeded:
[frontend app](https://github.com/accordbridge-labs/accordbridge-frontend/actions/runs/46078221845) and
[advisory](https://github.com/accordbridge-labs/accordbridge-frontend/actions/runs/46078221691),
[backend app](https://github.com/accordbridge-labs/accordbridge-backend/actions/runs/46078221210) and
[advisory](https://github.com/accordbridge-labs/accordbridge-backend/actions/runs/46078221202),
[contracts app](https://github.com/accordbridge-labs/accordbridge-contracts/actions/runs/46078221051) and
[advisory](https://github.com/accordbridge-labs/accordbridge-contracts/actions/runs/46078220997).
The frontend connected-workspace job failed once on a 5-second mobile selector
timeout and passed on re-run; no code change was made between those runs.

**Activity gap partly closed:** the newest merged commits at the earlier review
were 30 October (backend), 26 October (frontend) and 24 October (contracts).
The 27 November merges above add substantive, tested changes on all three
application repositories. A Drips appeal should still cite the rejection date
from the app and confirm that these changes fall inside the appeal window.

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

1. Resolve outstanding rights records. At the 18 October review the backend,
   frontend, contracts and organization resources had adopted MIT with matching
   contribution terms, and [the inventory](LICENSING-REVIEW.md) identified
   frontend PR #12 and contracts PR #7 as outside contributions without an
   explicit grant; no messages had been sent at that time. **Update:** on
   27 November 2026 the maintainer switched all four repositories to Apache
   License 2.0 and sent consent requests to both contributors, recorded in
   [CONSENT-OUTREACH.md](CONSENT-OUTREACH.md). No replies have been recorded.
   The earlier MIT requests do not grant rights under Apache-2.0.
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
