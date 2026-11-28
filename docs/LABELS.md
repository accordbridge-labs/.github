# Issue labels

The three application repositories use the same label taxonomy. It is adapted
from the [Soroban testkit](https://github.com/soroban-testkit/testkit-backend/issues)
pattern of type + module/area + size. Labels are **routing aids**, not
assignments, promises of reward, or evidence that an issue is in a Wave.

## Taxonomy

| Family | Labels | Rule |
| --- | --- | --- |
| Type | `bug`, `enhancement`, `documentation`, `dependencies`, `question` | Usually one. Use `bug` for incorrect behavior, `enhancement` for new behavior, `documentation` for evidence/decision docs, `dependencies` for advisories and upgrades. |
| Area | `area/agreement`, `area/wallet`, `area/escrow`, `area/review`, `area/testnet`, `area/frontend`, `area/backend`, `area/contracts`, `area/ci`, `area/tooling`, `area/policy`, `area/security`, `area/docs`, `area/licensing` | One or more, only where the work actually lands. Cross-repo issues carry each affected area. |
| Size | `size/s`, `size/m`, `size/l` | Exactly one. `size/l` includes cross-repository or design-heavy work. |
| Contributor signals | `good first issue`, `help wanted` | Optional. `good first issue` means isolated scope with concrete acceptance tests. |
| Program | `Stellar Wave` | **Do not apply until the repository is approved and the issue is added to the program.** A maintainer applying this label can enroll an issue; treat it as an action, not a category. |

Existing GitHub defaults (`duplicate`, `invalid`, `wontfix`, `accessibility`)
keep their standard meaning.

## Current open issues (28 November 2026)

| Repository | Issue | Labels |
| --- | --- | --- |
| Frontend | [#2](https://github.com/accordbridge-labs/accordbridge-frontend/issues/2) Wallet signing spec | `enhancement`, `area/wallet`, `area/testnet`, `size/m` |
| Frontend | [#9](https://github.com/accordbridge-labs/accordbridge-frontend/issues/9) Freighter onboarding | `enhancement`, `area/wallet`, `size/m` |
| Frontend | [#18](https://github.com/accordbridge-labs/accordbridge-frontend/issues/18) Unsaved-edit guard | `bug`, `good first issue`, `area/agreement`, `size/m` |
| Backend | [#9](https://github.com/accordbridge-labs/accordbridge-backend/issues/9) Bounded reconciliation | `enhancement`, `area/testnet`, `area/backend`, `size/l` |
| Backend | [#14](https://github.com/accordbridge-labs/accordbridge-backend/issues/14) Cursor pagination | `enhancement`, `help wanted`, `area/backend`, `size/m` |
| Contracts | [#1](https://github.com/accordbridge-labs/accordbridge-contracts/issues/1) Provider/audit evidence | `documentation`, `area/contracts`, `area/policy`, `area/security`, `size/l` |
| Contracts | [#2](https://github.com/accordbridge-labs/accordbridge-contracts/issues/2) Escrow validation matrix | `documentation`, `area/contracts`, `area/policy`, `size/l` |
| Contracts | [#5](https://github.com/accordbridge-labs/accordbridge-contracts/issues/5) Adversarial invariant tests | `enhancement`, `area/testnet`, `area/contracts`, `area/security`, `size/l` |
| Contracts | [#6](https://github.com/accordbridge-labs/accordbridge-contracts/issues/6) Storage expiry/restoration | `enhancement`, `area/testnet`, `area/contracts`, `size/l` |
| Contracts | [#15](https://github.com/accordbridge-labs/accordbridge-contracts/issues/15) Dependency-advisory check | `enhancement`, `dependencies`, `area/ci`, `area/tooling`, `size/m` |

Check live issue state before relying on this table. Historical closed issues
were not relabeled.

## Adding an issue to the program

Applying `Stellar Wave` is meaningful only when the repository is approved.
Follow the [maintainer procedure](https://docs.drips.network/wave/maintainers/participating-in-a-wave/)
and the [appeal checklist](APPEAL-CHECKLIST.md). Never apply the label to
manufacture activity or imply that a rejected repository is enrolled.
