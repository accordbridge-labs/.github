# Licensing review and adoption checklist

Reviewed 18 October 2026. **MIT is the selected project license.** The maintainer
requested implementation of the MIT adoption steps. The backend and organization
resources now include root MIT licenses attributed to Yusuf Abdulhameed. This
review does not grant rights to other repositories or replace third-party licenses.

The frontend and contracts have also adopted MIT at the maintainer's explicit direction, with
attribution to Yusuf Abdulhameed and contributors. Historical contributor
permission has not been independently verified; adoption does not establish that
permission. This is an evidence inventory,
not a warranty of ownership or a complete distribution-license audit.

## Adoption status

| Repository | Status |
| --- | --- |
| [backend](https://github.com/accordbridge-labs/accordbridge-backend) | MIT: root LICENSE, package metadata and README updated. |
| [organization resources](https://github.com/accordbridge-labs/.github) | MIT: root LICENSE and contribution terms updated. This does not license sibling repositories. |
| [frontend](https://github.com/accordbridge-labs/accordbridge-frontend/blob/main/LICENSE) | MIT: root LICENSE, package metadata and README updated at explicit maintainer direction. Permission for PR #12 has not been independently verified. |
| [contracts](https://github.com/accordbridge-labs/accordbridge-contracts/blob/main/LICENSE) | MIT: root LICENSE, npm and Cargo metadata, and README updated at explicit maintainer direction. Permission for PR #7 has not been independently verified. |

## Source provenance

| Repository | Inspected main commit | Finding |
| --- | --- | --- |
| backend | `15d5fe59a240474fc3e22b4ac4b95f5feeab1e7c` | Non-merge authors in the inspected history are maintainer identities. MIT adoption was requested by the maintainer. |
| frontend | `6672699b9a0ccf2f5f37f30c3c87d95fb2cd6d4b` | Includes @Oluwa-Laughter's [PR #12](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12), affecting recovery implementation, tests, documentation and package configuration. No explicit license permission was found in its PR body, comments or reviews. |
| contracts | `6d6cfec` | Includes @Ay-obami's [PR #7](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7): `.github/workflows/contracts.yml` and `docs/CI-WASM-ARTIFACTS.md`. No explicit license permission was found in the inspected PR records. |
| organization resources | `00d31a8` | Inspected non-merge authors are maintainer identities. MIT adoption was requested by the maintainer. |

Author names and GitHub merge permission do not establish copyright ownership or
a license grant. These findings do not assert that private permission records do
not exist. Keep attribution and Git history intact when resolving permissions.

## License choice

The maintainer requested the [MIT](https://choosealicense.com/licenses/mit/)
adoption workflow. MIT provides broad reuse rights with notice retention. Its
selection does not establish funding eligibility or license third-party work that
the maintainer does not control.

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

## Consent request drafts — not sent

The maintainer can send each contributor this request with the exact repository
and PR/commit range filled in:

> We are preparing to license AccordBridge under the MIT License.
> Please confirm whether you own or are authorized to license the original work
> you contributed in [repository and PR/commit range], and whether you grant
> permission to distribute those contributions under that license. Please identify
> any third-party material or employer restrictions and its applicable terms.
> We will preserve your attribution. A lack of response will not be treated as consent.

The affected requests are frontend PR #12 (@Oluwa-Laughter) and contracts PR #7
(@Ay-obami). No request has been posted or sent by this review. Record actual
responses or existing permission records; do not substitute a maintainer checkmark
for a contributor's grant. If permission is unavailable, keep that scope pending
and resolve an independently authored alternative through a separate reviewed change.

## Rights records and remaining adoption checks

Frontend and contracts adoption is recorded above separately from unresolved rights evidence.
The outstanding permissions still require follow-up; no historical contributor
consent is inferred from the maintainer's request.

1. Record the selected license and maintainer confirmation of rights.
2. Establish compatible permission for existing outside contributions, with links
   to the records or an appropriately redacted reference to a private agreement.
3. Add the unmodified official license text to each covered repository's root,
   using accurate copyright attribution. Update package/Cargo metadata to match.
4. Replace stale “license pending” statements only for repositories actually covered.
5. State the selected license for future contributions and preserve third-party
   notices. Do not imply that historical contributors accepted new terms retroactively.
6. Verify GitHub license detection and package metadata, then record the adoption
   commits in the project readiness report. Keep any unresolved exceptions explicit.
