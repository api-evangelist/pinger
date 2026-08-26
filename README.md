# Pinger

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Pinger, Inc. is a San Jose, California mobile communications company founded in 2005 by former Palm
managers Greg Woock and Joe Sipher. It builds consumer and small-business calling and texting apps —
**TextFree** (2009, the original free texting app with a free US phone number), **Sideline** (a second
phone number for work and privacy) and **Index** (a dedicated business line with auto-reply,
scheduling, broadcast messaging and payment collection). Sideline and TextFree have together been used
by more than 100 million people.

## API surface

**Pinger publishes no public API.** This was checked, not assumed:

| Probe | Result |
|---|---|
| `developer.pinger.com`, `docs.pinger.com` | DNS does not resolve |
| `api.pinger.com/` | 302 → `www.pinger.com` |
| `api.pinger.com/v1/`, `/1.0/`, `/docs`, `/openapi.json`, `/swagger.json`, `/api-docs` | **410 Gone** |
| `api.pinger.com/.well-known/*` | 403 |
| `/openapi.json` on pinger.com, sideline.com, textfree.com, getindex.com | 404 |
| `/.well-known/agent-card.json` and `/.well-known/agent.json` on every host | 404 (HTML) — no A2A agent card |
| `/.well-known/security.txt`, `/openid-configuration`, `/oauth-authorization-server`, `/api-catalog`, `/ai-plugin.json` on 7 hosts | 404 / 403 / 502 — nothing served |
| GitHub organization `pinger` / `pinger-inc` | 404 — no org |
| npm, PyPI first-party SDK | none |

Pinger's integrations run the other direction: Index *consumes* third-party calendar (Google, iCloud,
Outlook) and payment (PayPal, Venmo, Square) services rather than exposing its own.

## What is in this repository

- `llms/pinger-sideline-llms.txt` — the one machine-readable document on the estate, served verbatim
  at `https://www.sideline.com/llms.txt` (200). It is an AI information sheet about the Sideline app,
  not an llms.txt link index, and it names no API.
- `llms/pinger-llms.yml` — where that file came from, plus the 404/502 on the other hosts.
- `well-known/pinger-well-known.yml` — the full `/.well-known/*` probe matrix across seven hosts.
- `security/pinger-domain-security.yml` — TLS/HSTS/DNSSEC/CAA/SPF/DMARC across the four Pinger domains.
- `plans/pinger-plans-pricing.yml` — no API plans; the only published price is Index at $24.99/month.
- `rate-limits/pinger-rate-limits.yml` — no published limits, because there is no public API.

## Links

- Website — https://www.pinger.com/
- About — https://www.pinger.com/about/
- Support — https://www.pinger.com/support/
- Terms — https://www.pinger.com/terms-and-conditions/
- Privacy — https://www.pinger.com/privacy-policy/
- Products — https://textfree.com/ · https://www.sideline.com/ · https://getindex.com/
