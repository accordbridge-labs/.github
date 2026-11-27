# Wave issue backlog — routing and readiness

Status: **routing proposal only**. No issue has been added to a Drips Wave
Program, no complexity has been set in the app, and no contributor is assigned
by this document. Check live issue state before using this list.

The three repositories are components of one product. Issues that change an
API or contract interface must link dependent issues and PRs across repos and
state the integration order. Add issues to the Program only after repository
approval, and set complexity in the Drips dashboard.

| Repository | Issue | Scope | Suggested complexity* | Cross-repo note |
| --- | --- | --- | --- | --- |
| Frontend | [#2](https://github.com/accordbridge-labs/accordbridge-frontend/issues/2) | Specify wallet signing and transaction status behaviour | High | Depends on backend interface and contract authority design; planning only |
| Frontend | [#9](https://github.com/accordbridge-labs/accordbridge-frontend/issues/9) | Freighter Testnet onboarding, error states, manual two-wallet check | Medium | Core wallet reliability; overlaps hosted acceptance runbook H05–H09 |
| Frontend | [#18](https://github.com/accordbridge-labs/accordbridge-frontend/issues/18) | Guard against discarding unsaved agreement edits | Medium | Client-only; include dirty/failed-save browser tests |
| Backend | [#9](https://github.com/accordbridge-labs/accordbridge-backend/issues/9) | Bounded, idempotent reconciliation of unresolved intents | High | Core reliability; depends on existing reconciliation logic, no signer |
| Backend | [#14](https://github.com/accordbridge-labs/accordbridge-backend/issues/14) | Cursor pagination for participant project list | Medium | Requires companion frontend PR; update OpenAPI in same change |
| Contracts | [#1](https://github.com/accordbridge-labs/accordbridge-contracts/issues/1) | Provider deployment and audit evidence decision | High | Evidence/design issue; must not be presented as mainnet approval |
| Contracts | [#2](https://github.com/accordbridge-labs/accordbridge-contracts/issues/2) | Isolated milestone escrows and financial validation matrix | High | Design/test plan; informs frontend #2 and backend rules |
| Contracts | [#5](https://github.com/accordbridge-labs/accordbridge-contracts/issues/5) | Adversarial escrow state-machine and invariant tests | High | Core reliability; no new authority or policy |
| Contracts | [#6](https://github.com/accordbridge-labs/accordbridge-contracts/issues/6) | Storage expiry and restoration procedure | High | Coordinate diagnostic wording with backend #8/readiness work |
| Contracts | [#15](https://github.com/accordbridge-labs/accordbridge-contracts/issues/15) | Dependency-advisory check and triage | Medium | Partially addressed by the prepared `fix/dependency-advisories` work; clarify remaining scope before listing |

\* Drips uses Trivial (100), Medium (150) and High (200) base points. These are
suggestions for review, not assignments or promises of reward.

## Recently closed contributor-facing work

- Frontend #10 and #11 were closed as completed on 9 October 2026, but
  `frontend/docs/HOSTED-ACCEPTANCE.md` still records H01–H26 as **NOT RUN**.
  Closing an issue is not the same as executing a hosted wallet acceptance run.
- Contracts #4 was closed when reproducible WASM CI was added; contracts #5
  remains open for deeper adversarial coverage.
- Backend #7/#8 were closed; bounded reconciliation (#9) remains open.

## Before listing issues

1. Confirm each issue still reproduces on current `main` and that no PR is open.
2. Confirm the scope is small enough for one Wave cycle and states concrete
   acceptance tests.
3. Coordinate interface changes across repos; link dependent PRs and specify
   merge order.
4. Do not claim the application is feature-complete while core reliability
   issues remain open, and do not mark an issue resolved before its PR is
   merged and its evidence recorded.
5. Distinction for contributors: mocked browser tests, isolated PostgreSQL
   tests, real Testnet writes and manual Freighter checks are different kinds
   of evidence. State which one was actually run.
