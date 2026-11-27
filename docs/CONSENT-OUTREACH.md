# Contributor consent outreach — drafts, not sent

Status: **no request has been sent and no grant has been recorded**. This file
contains ready-to-copy drafts and a record template. It does not create or
imply permission, and it does not replace the
[licensing inventory](LICENSING-REVIEW.md).

Why this matters: the organization and all three application repositories use
MIT for their original work, but frontend PR #12 and contracts PR #7 were
outside contributions for which no explicit license grant was found in the
public PR records. Drips Wave [terms §6](https://docs.drips.network/wave/terms-and-rules/)
prohibit submissions that infringe third-party IP and require proper
attribution; §13 expects contributions under the applicable open-source
license. Resolve or explicitly disclose these exceptions before appealing.

## Outstanding records

| Item | Repository / PR | Contributor | Contribution | Request sent | Response recorded |
| --- | --- | --- | --- | --- | --- |
| L1 | `accordbridge-frontend` [PR #12](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12) | @Oluwa-Laughter | Cold-start intent recovery implementation, tests, docs, package configuration | NO | NO |
| L2 | `accordbridge-contracts` [PR #7](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7) | @Ay-obami | `.github/workflows/contracts.yml`, `docs/CI-WASM-ARTIFACTS.md` | NO | NO |

## Draft requests (copy verbatim; fill the bracketed fields)

> We are preparing to license AccordBridge under the MIT License.
> Please confirm whether you own or are authorized to license the original work
> you contributed in [repository and PR/commit range], and whether you grant
> permission to distribute those contributions under that license. Please
> identify any third-party material or employer restrictions and its applicable
> terms. We will preserve your attribution. A lack of response will not be
> treated as consent.

Suggested subject and delivery: a direct GitHub message or a comment on the
specific PR, from the maintainer account, with the exact PR link. Keep a
redacted reference to the message and the contributor's actual reply.

### L1 — filled draft

> We are preparing to license AccordBridge under the MIT License.
> Please confirm whether you own or are authorized to license the original work
> you contributed in `accordbridge-frontend` PR #12 (cold-start intent recovery
> implementation, tests, documentation and package configuration), and whether
> you grant permission to distribute those contributions under that license.
> Please identify any third-party material or employer restrictions and its
> applicable terms. We will preserve your attribution. A lack of response will
> not be treated as consent.

### L2 — filled draft

> We are preparing to license AccordBridge under the MIT License.
> Please confirm whether you own or are authorized to license the original work
> you contributed in `accordbridge-contracts` PR #7
> (`.github/workflows/contracts.yml` and `docs/CI-WASM-ARTIFACTS.md`), and whether
> you grant permission to distribute those contributions under that license.
> Please identify any third-party material or employer restrictions and its
> applicable terms. We will preserve your attribution. A lack of response will
> not be treated as consent.

## Recording a response

For each item, record in the issue or a private, appropriately redacted note:

- channel, date and sender account used for the request;
- the contributor's exact answer and its date, or "no response" after a stated
  follow-up period;
- whether the answer covers the whole PR/commit range;
- any third-party material or employer restriction named;
- the commit or PR where the record was added to public documentation.

A maintainer checkmark, merge permission or author name is **not** a license
grant. If permission cannot be obtained, keep the scope explicitly pending and
use a separate reviewed change authored independently to replace that scope;
preserve attribution and Git history.

## Reviewer note

Do not post these requests automatically. A public PR comment creates an
external message under the maintainer's identity; confirm delivery and wording
before sending.
