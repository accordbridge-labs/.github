![AccordBridge — Clear agreements. Funded milestones. Original bridge illustration.](https://raw.githubusercontent.com/accordbridge-labs/.github/main/profile/assets/accordbridge-banner.png)

# AccordBridge Labs

**Clear agreements. Funded milestones.**

AccordBridge Labs builds an experimental freelancer–client workspace on Stellar Testnet. Our first focus is fixed-price website projects for independent developers and designers working with clients they already know.

The implemented workflow connects versioned agreements, participant acceptance, first-milestone test-token escrow, deliverable submissions, client review, release, and mutual refunds. Paid scope changes and human dispute resolution remain planned.

[Explore the Testnet workspace](https://accordbridge-frontend.vercel.app) · [Start contributing](https://github.com/accordbridge-labs/.github/blob/main/CONTRIBUTING.md) · [Architecture](https://github.com/accordbridge-labs/.github/blob/main/docs/REPOSITORY-GUIDE.md) · [Verification evidence](https://github.com/accordbridge-labs/.github/blob/main/docs/PROGRAM-READINESS.md)

## Who it is for

- **Clients:** agree on scope and acceptance criteria, review delivered work, and explicitly authorize test-token release.
- **Freelancers:** preserve the agreed version, check funding state, and submit versioned delivery notes and links.
- **Contributors:** improve one part of the shared workflow with tests and documented interface changes.

## One workflow, three repositories

```text
Agree & accept → Prepare escrow → Both wallets approve → Fund with ABUSD
                                                            ↓
Release to freelancer ← Client approves work ← Freelancer submits
          or: both participants approve a refund to the client
```

Application acceptance and work approval do not transfer tokens. Freighter signs
wallet actions; the backend submits and reconciles transactions; the contract
enforces its on-chain rules. App review gates are not contract-level dispute protection.

## Project status

**Development/testnet prototype.** The repositories contain a Next.js interface, a NestJS/PostgreSQL API, and Rust/Soroban contracts. ABUSD is a valueless test token, not USDC. No audit or mainnet payment service is available. Production escrow infrastructure is still being evaluated.

Start with the [repository and architecture guide](https://github.com/accordbridge-labs/.github/blob/main/docs/REPOSITORY-GUIDE.md). Each repository documents reproducible setup and checks. [Deployment records](https://github.com/accordbridge-labs/accordbridge-contracts/tree/main/deployments) record historical testnet observations; resets and storage expiry can invalidate them. A successful automated or mocked test is not evidence of live Freighter acceptance.

## Repositories

| Repository | Responsibility |
| --- | --- |
| [accordbridge-frontend](https://github.com/accordbridge-labs/accordbridge-frontend) | Client and freelancer experience, wallet interaction, project workspace |
| [accordbridge-backend](https://github.com/accordbridge-labs/accordbridge-backend) | Sessions, participant access, agreement history, work review, transaction preparation and reconciliation |
| [accordbridge-contracts](https://github.com/accordbridge-labs/accordbridge-contracts) | Testnet escrow, participant authorization, a test-token faucet, contract tests and deployment evidence |

All three repositories are public. Read the [contribution guide](https://github.com/accordbridge-labs/.github/blob/main/CONTRIBUTING.md) before starting work. The backend, frontend, contracts and these organization resources have adopted MIT. See the [per-repository licensing status and outstanding contributor permissions](https://github.com/accordbridge-labs/.github/blob/main/docs/LICENSING-REVIEW.md).

## Start with a verified change

Read the component README, reproduce the issue, agree on scope in its issue thread,
then open a focused PR with test results. Coordinate API or contract changes across
the affected repositories. The [contributor starting guide](https://github.com/accordbridge-labs/.github/blob/main/docs/START-HERE.md)
maps each area to its setup, checks and remaining work. Report security issues
through the [private reporting guidance](https://github.com/accordbridge-labs/.github/blob/main/SECURITY.md), not public issues.

## Design principles

- Show what was agreed, whether it is funded, and who must act next.
- Require agreement and funding for additional work.
- Keep private project files and personal information off the public chain.
- Explain the authority of clients, freelancers, operators, and reviewers.
- Verify financial behaviour before handling real funds.

Stellar Testnet is the experimental network; this project does not imply endorsement by the Stellar Development Foundation or acceptance into a funding program.
