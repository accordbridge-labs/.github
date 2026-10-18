# Start contributing to AccordBridge

AccordBridge is a Testnet experiment for known freelancer–client pairs, not a
mainnet payment service. Start with one reproducible problem rather than expanding
the product scope. Never use customer data, valuable assets or real wallet secrets
in test fixtures.

| Area | Start here | Verification |
| --- | --- | --- |
| UI, agreement editing, recovery | [Frontend README](https://github.com/accordbridge-labs/accordbridge-frontend#readme) | Unit tests, build, typecheck, browser suites; use an isolated backend/database for connected tests. |
| Sessions, access, agreement history, transaction reconciliation | [Backend README](https://github.com/accordbridge-labs/accordbridge-backend#readme) | PostgreSQL integration tests, build, formatting and generated OpenAPI drift check. |
| Escrow authorization and settlement | [Contracts README](https://github.com/accordbridge-labs/accordbridge-contracts#readme) | Locked Rust tests, formatting, pinned WASM build and reproducibility check. |

## Terms used across the repositories

- **Soroban:** Stellar's smart-contract platform; our Rust contracts execute there.
- **Freighter:** the browser wallet that holds the participant's keys and asks for signing approval.
- **XDR:** the encoded Stellar transaction passed from the API to the wallet for signing.
- **Intent:** the backend's record of a prepared action and its submission/confirmation lifecycle.
- **Reconciliation:** checking transaction results, contract state and balances before reporting settlement.
- **ABUSD:** our valueless, seven-decimal Testnet faucet token; not USDC or a stablecoin.
- **Terms hash:** the digest committed to escrow to bind wallet approvals to frozen terms.

## Contribution loop

1. Read [contribution and licensing requirements](../CONTRIBUTING.md).
2. Look for an existing issue in the relevant repo. State the affected code, current
   behavior, expected behavior and a concrete acceptance test. Avoid duplicate issues.
3. Reproduce the problem in an isolated local environment. A documentation-only
   change should still have its commands, paths and claims checked against source.
4. Make a focused change. Include a regression test for behavior changes, and update
   API/schema documentation when interfaces change. Link dependent cross-repo PRs.
5. In the PR, report the commands actually run and their results, plus anything not
   tested. CI success is not a security audit or proof of hosted wallet acceptance.

## Existing work to discuss with maintainers

- [Frontend wallet setup guidance](https://github.com/accordbridge-labs/accordbridge-frontend/issues/9).
- [Backend bounded reconciliation](https://github.com/accordbridge-labs/accordbridge-backend/issues/9).
- [Contract storage expiry/restoration](https://github.com/accordbridge-labs/accordbridge-contracts/issues/6).

Check the live issue status and current implementation before starting: this list
is a routing guide, not an assignment or a claim that no progress has been made.
Hosted two-wallet acceptance, historical contributor permissions and production
controls remain separate requirements in the [readiness report](PROGRAM-READINESS.md).
