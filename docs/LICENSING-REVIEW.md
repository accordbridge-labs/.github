# Licensing review and adoption checklist

Reviewed 18 October 2026. **No project license has been adopted by this document.**
The maintainer's choice and permission for pre-existing outside contributions remain
unresolved. This review is an evidence inventory, not a warranty of ownership or a
complete distribution-license audit.

## Source provenance

| Repository | Inspected main commit | Finding |
| --- | --- | --- |
| backend | `15d5fe59a240474fc3e22b4ac4b95f5feeab1e7c` | Non-merge authors in the inspected history are maintainer identities. Maintainer must confirm rights to the original work and choose the license. |
| frontend | `6672699b9a0ccf2f5f37f30c3c87d95fb2cd6d4b` | Includes @Oluwa-Laughter's [PR #12](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12), affecting recovery implementation, tests, documentation and package configuration. No explicit license permission was found in its PR body, comments or reviews. |
| contracts | `6d6cfec` | Includes @Ay-obami's [PR #7](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7): `.github/workflows/contracts.yml` and `docs/CI-WASM-ARTIFACTS.md`. No explicit license permission was found in the inspected PR records. |
| organization resources | `00d31a8` | Inspected non-merge authors are maintainer identities. Confirm rights to the original documentation. |

Author names and GitHub merge permission do not establish copyright ownership or
a license grant. These findings do not assert that private permission records do
not exist. Keep attribution and Git history intact when resolving permissions.

## License choice

The maintainer has been asked to choose between [MIT](https://choosealicense.com/licenses/mit/)
and [Apache-2.0](https://choosealicense.com/licenses/apache-2.0/). MIT provides broad
reuse rights with notice retention. Apache-2.0 includes an explicit patent grant
and additional notice/change requirements. Neither choice establishes funding
eligibility or licenses third-party work that the maintainer does not control.

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

After selecting one license, the maintainer can send each contributor this request
with the exact repository, PR, commit range and license filled in:

> We are preparing to license AccordBridge under [MIT / Apache-2.0, choose one].
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

## Apply only after the prerequisites are resolved

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
