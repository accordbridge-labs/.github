# Contributing

AccordBridge is a development/testnet prototype. Begin with an existing unassigned issue or describe the user problem, proposed behaviour, affected repositories, and acceptance criteria. Check for an existing pull request before starting duplicate work. The three repositories are components of one product, not independent claims of ecosystem impact.

## Changes and review

1. Link the relevant issue and confirm its scope and current assignment.
2. Describe the proposed behaviour and remaining decisions.
3. Make changes on a branch and open a pull request.
4. Obtain review before merging changes to agreed scope or financial rules.

Keep interface changes coordinated across frontend, backend, and contracts. The backend repository holds the canonical product specification and architecture. Repository-specific documents describe how each component fulfils those requirements.

Distinguish proposals, locally checked behaviour, testnet observations, and verified mainnet behaviour. Do not claim guarantees, audits, or deployments without evidence for the exact version.

Do not commit secrets, private keys, real customer evidence, or identifying dispute material. Use synthetic examples.

## Licensing and contribution terms

The backend, frontend, contracts and this organization-resources repository use MIT for their original work. Contributions intentionally submitted for inclusion in these licensed repositories must be offered under their MIT license, and contributors must have the right to submit them. Preserve existing copyright and third-party license notices; identify reused material and its terms in the pull request. No copyright assignment is requested.

Frontend and contracts MIT adoption was explicitly requested by the maintainer; historical contributor permission has not been independently verified. Neither this guide nor adoption establishes retroactive contributor consent. Resolve and record the outstanding permissions listed in the [licensing review](docs/LICENSING-REVIEW.md).

## Verification

- Backend: `npm ci`, configure an isolated PostgreSQL database ending in `_test`, then `npm test` and `npm run docs:api`. Commit generated API changes with their implementation.
- Frontend: `npm ci`, `npm test`, `npm run build`, `npm run typecheck`, then install Chromium and run `npm run test:e2e`. Run `npm run test:workspace` with the sibling backend and its isolated database for connected changes.
- Contracts: use the pinned toolchain, `cargo fmt --all -- --check`, `cargo test --locked --workspace`, and `cargo build --locked --release --target wasm32v1-none --workspace`.

Read each repository's README for complete setup. Include commands, results, and remaining gaps in the pull request. Review authorization, state transitions, failure recovery and tests before merging. Never turn a mocked test into a claim of a live deployment or audit.

## Attribution and program participation

Explain code you submit, including AI-assisted work, and verify it with relevant tests. Credit reused work and respect its license. Do not create artificial commits, issues, reviews, identities or activity to inflate reward metrics. Keep tasks tied to a concrete product need, and do not promise contributor rewards before repository/program approval.

For Wave participation, follow the [current Drips rules](https://docs.drips.network/wave/terms-and-rules/) and [maintainer procedure](https://docs.drips.network/wave/maintainers/participating-in-a-wave/). Rejected repositories require substantive improvements and an in-app appeal; a polished README alone is not evidence of eligibility.
