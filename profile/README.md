# AccordBridge Labs

**Clear agreements. Funded milestones.**

AccordBridge Labs builds an experimental freelancer–client workspace on Stellar Testnet. Our first focus is fixed-price website projects for independent developers and designers working with clients they already know.

The implemented workflow connects versioned agreements, participant acceptance, first-milestone test-token escrow, deliverable submissions, client review, release, and mutual refunds. Paid scope changes and human dispute resolution remain planned.

## Project status

**Development/testnet prototype.** The repositories contain a Next.js interface, a NestJS/PostgreSQL API, and Rust/Soroban contracts. ABUSD is a valueless test token, not USDC. No audit or mainnet payment service is available. Production escrow infrastructure is still being evaluated.

Start with the [repository and architecture guide](../docs/REPOSITORY-GUIDE.md). Each repository documents reproducible setup and checks. [Deployment records](https://github.com/accordbridge-labs/accordbridge-contracts/tree/main/deployments) record historical testnet observations; resets and storage expiry can invalidate them. A successful automated or mocked test is not evidence of live Freighter acceptance.

## Repositories

| Repository | Responsibility |
| --- | --- |
| [accordbridge-frontend](https://github.com/accordbridge-labs/accordbridge-frontend) | Client and freelancer experience, wallet interaction, project workspace |
| [accordbridge-backend](https://github.com/accordbridge-labs/accordbridge-backend) | Sessions, participant access, agreement history, work review, transaction preparation and reconciliation |
| [accordbridge-contracts](https://github.com/accordbridge-labs/accordbridge-contracts) | Testnet escrow, participant authorization, a test-token faucet, contract tests and deployment evidence |

All three repositories are public. Read the [contribution guide](../CONTRIBUTING.md) before starting work. The backend, frontend and these organization resources have adopted MIT; contracts adoption remains pending. See the [per-repository licensing status and outstanding contributor permissions](../docs/LICENSING-REVIEW.md). Public visibility alone does not grant an open-source reuse license.

## Design principles

- Show what was agreed, whether it is funded, and who must act next.
- Require agreement and funding for additional work.
- Keep private project files and personal information off the public chain.
- Explain the authority of clients, freelancers, operators, and reviewers.
- Verify financial behaviour before handling real funds.

Stellar Testnet is the experimental network; this project does not imply endorsement by the Stellar Development Foundation or acceptance into a funding program.
