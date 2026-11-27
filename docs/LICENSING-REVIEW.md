# Licensing review and adoption checklist

Reviewed 18 October 2026. Updated 27 November 2026. **The selected project
license is now the Apache License, Version 2.0**, replacing the earlier MIT
selection. This review does not grant rights to other repositories or replace
third-party licenses, and it is an evidence inventory, not a warranty of
ownership or a complete distribution-license audit.

At the 18 October review the project had adopted MIT at the maintainer's
direction, with attribution to Yusuf Abdulhameed and contributors, and the
backend/organization roots carried MIT licenses attributed to Yusuf Abdulhameed.
On 27 November 2026 the maintainer decided to use Apache-2.0 instead. The
unmodified official Apache-2.0 text, root `NOTICE` files and matching metadata
are now in all four repositories.

## Current adoption status

| Repository | Status |
| --- | --- |
| [backend](https://github.com/accordbridge-labs/accordbridge-backend) | Apache-2.0: root LICENSE and NOTICE, `package.json` and README updated. |
| [organization resources](https://github.com/accordbridge-labs/.github) | Apache-2.0: root LICENSE and NOTICE, README, contribution terms and docs updated. This does not license sibling repositories. |
| [frontend](https://github.com/accordbridge-labs/accordbridge-frontend/blob/main/LICENSE) | Apache-2.0: root LICENSE and NOTICE, package metadata and README updated. Permission for PR #12 has not been independently verified. |
| [contracts](https://github.com/accordbridge-labs/accordbridge-contracts/blob/main/LICENSE) | Apache-2.0: root LICENSE and NOTICE, npm and Cargo metadata and README updated. Permission for PR #7 has not been independently verified. |

Switching the license label does **not** grant rights over existing outside
contributions. The two unresolved contributions remain exactly that until a
rights holder confirms in writing.

## Source provenance

| Repository | Inspected main commit | Finding |
| --- | --- | --- |
| backend | `15d5fe59a240474fc3e22b4ac4b95f5feeab1e7c` | Non-merge authors in the inspected history are maintainer identities. MIT adoption was requested by the maintainer at that time. |
| frontend | `6672699b9a0ccf2f5f37f30c3c87d95fb2cd6d4b` | Includes @Oluwa-Laughter's [PR #12](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12), affecting recovery implementation, tests, documentation and package configuration. No explicit license permission was found in its PR body, comments or reviews. |
| contracts | `6d6cfec` | Includes @Ay-obami's [PR #7](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7): `.github/workflows/contracts.yml` and `docs/CI-WASM-ARTIFACTS.md`. No explicit license permission was found in the inspected PR records. |
| organization resources | `00d31a8` | Inspected non-merge authors are maintainer identities. MIT adoption was requested by the maintainer at that time. |

Author names and GitHub merge permission do not establish copyright ownership or
a license grant. These findings do not assert that private permission records do
not exist. Keep attribution, `NOTICE` content and Git history intact when
resolving permissions.

## License choice

The maintainer selected the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
on 27 November 2026. It provides broad reuse rights with notice retention and
an express patent grant, and it requires a root `NOTICE` file in covered
distributions. Selection does not establish funding eligibility, ownership of
outside contributions, or a license over third-party work the maintainer does
not control. The earlier MIT adoption is recorded above as history and must not
be cited as an Apache-2.0 grant.

Public visibility is not an open-source license. GitHub's [no-license guidance](https://choosealicense.com/no-permission/)
explains the distinction and the importance of existing contributor rights.

## Dependency metadata findings

- Direct installed backend dependencies declare MIT or Apache-2.0 licenses.
- Direct installed frontend dependencies declare MIT, Apache-2.0 or ISC licenses.
- The contracts JavaScript lockfile lists MIT, Apache-2.0 and BSD-3-Clause.
- Locked Cargo metadata declares licenses for every external package. Expressions
  include MIT, Apache-2.0, BSD alternatives, Unlicense alternatives, Zlib alternatives,
  Unicode-3.0 and the LLVM exception. Preserve the applicable upstream terms.
- Many backend/frontend lockfile entries omit license metadata; their absence is
  not proof that the installed package is unlicensed. Direct installed package
  manifests were inspected to resolve those direct-dependency omissions.

This is metadata inspection, not a finding that every transitive license file,
bundled asset or compiled distribution notice has been checked. Dependencies keep
their own licenses; a root project LICENSE does not replace them. Before publishing
packages, containers, browser bundles or WASM distributions as a licensed release,
inventory the shipped dependencies/assets and retain their required notices.

## Consent requests

On 27 November 2026 the maintainer sent MIT-specific consent requests as public
PR comments: [frontend PR #12 comment](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7209604233)
and [contracts PR #7 comment](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7#issuecomment-7209605792).
Both are recorded in [CONSENT-OUTREACH.md](CONSENT-OUTREACH.md) and remain
AWAITING. Because the project has since moved to Apache-2.0, those requests do
**not** cover the new license. Fresh Apache-2.0 confirmations were sent on the
same day as follow-up comments: [frontend PR #12](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7229541759)
and [contracts PR #7](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7#issuecomment-7229543662).
Both remain AWAITING with no grant recorded. If no answer arrives, the affected
scope must be replaced by an independently authored, reviewed change with
attribution preserved, or the exception must be disclosed explicitly.

Do not substitute a maintainer checkmark, a merge, an author name or silence for
a contributor's grant. Record actual responses with their date, channel and
exact scope.

## Rights records and remaining adoption checks

1. Record the selected license (Apache-2.0) and maintainer confirmation of rights.
2. Establish compatible written permission for existing outside contributions,
   with links to the records or an appropriately redacted reference to a private
   agreement. The MIT requests do not satisfy this for Apache-2.0.
3. Keep the unmodified official Apache-2.0 text at each repository root, with
   matching `NOTICE`, package/Cargo metadata and README statements.
4. State Apache-2.0 for future contributions and preserve third-party notices.
   Do not imply that historical contributors accepted new terms retroactively.
5. Verify GitHub license detection and package metadata, then record adoption
   commits in the [readiness report](PROGRAM-READINESS.md). Keep unresolved
   exceptions explicit in the appeal evidence.
6. If permission is unavailable, keep that scope pending and resolve it through
   a separate reviewed change. Never invent consent, attribution or history.
