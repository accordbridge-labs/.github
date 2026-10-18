# StellarTickets reference review

Reviewed 18 October 2026 using GitHub repository contents and recent PR history.
This is a presentation/workflow comparison, not an audit of StellarTickets or
evidence of its funding eligibility. No product code, branding or activity was copied.

| Reference | Useful pattern | AccordBridge adaptation |
| --- | --- | --- |
| [Frontend README](https://github.com/StellarTickets/frontend#readme) | Explains users, routes, wallet flow, setup and focused documentation links. | Profile audience/workflow, frontend reader navigation and clear simulator vs persistent-workspace boundaries. |
| [Backend README](https://github.com/StellarTickets/backend#readme) | Separates API responsibilities from chain authority and documents setup/testing. | Correct stale hosted-status claims, distinguish implemented responsibilities from planned features, link API and recovery docs. |
| [Blockchain README](https://github.com/StellarTickets/blockchain#readme) | Documents contract authorization, data, tests and deployment procedure. | Escrow authorization/state reference and separate local checks from Testnet-broadcast scripts. |
| [Frontend issue #242](https://github.com/StellarTickets/frontend/issues/242) and [PR #347](https://github.com/StellarTickets/frontend/pull/347) | A specific component need and acceptance condition followed by regression tests. | Contributor loop: reproduce, scope, test, link evidence. No manufactured issue or commit volume. |
| [Backend PR #448](https://github.com/StellarTickets/backend/pull/448) | A focused change addressing event access and payload exposure. | Emphasize participant boundaries and regression evidence in contribution guidance. |
| [Contracts PR #389](https://github.com/StellarTickets/blockchain/pull/389) | Deployment/toolchain/storage follow-ups tied to issues. | Keep deployment provenance and storage-restoration limitations explicit. |

The three reference repositories have shared issue/PR templates, security and
contribution guidance, CI and topic-specific docs. AccordBridge already has shared
templates, security reporting and CI; those are retained instead of duplicated.
No public `.github` repository was returned for StellarTickets during this review;
the reusable lessons here come from its application repositories, not an assumed
organization-profile template.

More documents and more PRs are not themselves quality evidence. In particular,
we do not import ticketing, resale, organizer roles or mainnet support into a
freelance escrow prototype. Runtime feature changes need their own requirements,
tests and authority review.
