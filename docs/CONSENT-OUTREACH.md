# Contributor consent outreach

Status: **frontend PR #12 is now granted under both MIT and Apache-2.0.**
@Oluwa-Laughter first replied "Yes, permission granted" to the MIT request at
09:34 UTC, then replied "Hi @hameedx01 permission granted good move" at 22:57
UTC, after the Apache-2.0 follow-up was posted at 22:41 UTC — that second reply
is recorded as the Apache-2.0 grant. **Contracts PR #7 remains AWAITING** for
both licenses. The historical MIT drafts below are kept for the record. This
file does not create or imply permission beyond what contributors actually
wrote, and it does not replace the [licensing inventory](LICENSING-REVIEW.md).

Requests sent on 2026-11-27 from the maintainer account `hameedx01`:

| Item | Channel | Comment link | Response |
| --- | --- | --- | --- |
| L1 | Public comment on frontend PR #12 | [comment 7209604233](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7209604233) | GRANTED for MIT, 2026-11-27 09:34 UTC — [reply 7214840379](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7214840379); Apache-2.0 granted later at 22:57 UTC — [reply 7229757636](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7229757636). |
| L2 | Public comment on contracts PR #7 | [comment 7209605792](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7#issuecomment-7209605792) | AWAITING |

Do not convert a row to GRANTED without the contributor's actual answer. A
lack of response is not consent.

Why this matters: the organization and all three application repositories now
use Apache-2.0 for their original work, but frontend PR #12 and contracts PR #7
were outside contributions for which no explicit license grant was found in the
public PR records. The MIT requests sent earlier do not cover Apache-2.0. Drips Wave [terms §6](https://docs.drips.network/wave/terms-and-rules/)
prohibit submissions that infringe third-party IP and require proper
attribution; §13 expects contributions under the applicable open-source
license. Resolve or explicitly disclose these exceptions before appealing.

## Outstanding records

| Item | Repository / PR | Contributor | Contribution | Request sent | Response recorded |
| --- | --- | --- | --- | --- | --- |
| L1 | `accordbridge-frontend` [PR #12](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12) | @Oluwa-Laughter | Cold-start intent recovery implementation, tests, docs, package configuration | YES, 2026-11-27 | YES — MIT [reply](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7214840379) and Apache-2.0 [reply](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7229757636) |
| L2 | `accordbridge-contracts` [PR #7](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7) | @Ay-obami | `.github/workflows/contracts.yml`, `docs/CI-WASM-ARTIFACTS.md` | YES, 2026-11-27 | NO |

## Apache-2.0 confirmations required (not sent)

Because the selected license changed from MIT to Apache-2.0 on 27 November
2026, send a fresh request to each contributor before relying on their work
under the new license. Do not treat the MIT comments linked above as grants
under Apache-2.0.

| Item | Repository / PR | Contributor | Apache-2.0 request | Response |
| --- | --- | --- | --- | --- |
| A1 | `accordbridge-frontend` [PR #12](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12) | @Oluwa-Laughter | YES, 2026-11-27 — [comment 7229541759](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7229541759) | **GRANTED**, 2026-11-27 22:57 UTC — [reply 7229757636](https://github.com/accordbridge-labs/accordbridge-frontend/pull/12#issuecomment-7229757636): "Hi @hameedx01 permission granted good move" |
| A2 | `accordbridge-contracts` [PR #7](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7) | @Ay-obami | YES, 2026-11-27 — [comment 7229543662](https://github.com/accordbridge-labs/accordbridge-contracts/pull/7#issuecomment-7229543662) | NO — AWAITING |

A1 is GRANTED because the contributor replied in direct response to the
Apache-2.0 request. A2 remains AWAITING and must not be marked granted without
an actual reply. Keep the exact wording, timestamp and link for each grant.

> AccordBridge has changed its selected license from MIT to the Apache License,
> Version 2.0. Please confirm whether you own or are authorized to license the
> original work you contributed in [repository and PR], and whether you grant
> permission to distribute those contributions under Apache-2.0. Please identify
> any third-party material or employer restrictions and its applicable terms. We
> will preserve your attribution and the `NOTICE` notices. A lack of response
> will not be treated as consent.

## Historical MIT drafts (already sent on 27 November 2026)

The drafts below were sent when MIT was the selected license. They are retained
as the record of what was actually asked. They are **superseded** by the
Apache-2.0 requests above.

### Generic MIT template (historical)

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

#### L1 — filled MIT draft (sent)

> We are preparing to license AccordBridge under the MIT License.
> Please confirm whether you own or are authorized to license the original work
> you contributed in `accordbridge-frontend` PR #12 (cold-start intent recovery
> implementation, tests, documentation and package configuration), and whether
> you grant permission to distribute those contributions under that license.
> Please identify any third-party material or employer restrictions and its
> applicable terms. We will preserve your attribution. A lack of response will
> not be treated as consent.

#### L2 — filled MIT draft (sent)

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

The two requests above were posted manually as public PR comments under the
maintainer's identity on 27 November 2026. A public PR comment is an external
message: confirm delivery and wording before posting any follow-up. Keep
recording only what the contributor actually says; silence is not consent.
