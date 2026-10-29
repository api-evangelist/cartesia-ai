# Cartesia

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

Cartesia builds real-time voice AI - the Sonic family of text-to-speech models, Ink speech-to-text models, and a Voice Agents platform for building and deploying telephone and web voice agents. The core generation surface is exposed both as REST (bytes and Server-Sent Events) and as a low-latency, bidirectional WebSocket protocol at wss://api.cartesia.ai for streaming TTS and STT with multiplexed contexts, word/phoneme timestamps, and mid-stream flush and cancel.

**Areas:** Artificial Intelligence · Voice AI · Text-to-Speech · Speech-to-Text · Real-Time · WebSocket · Voice Cloning · Voice Agents · Voice

## Cartesia on APIs.io

Everything profiled for Cartesia is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cartesia-ai/](https://apis.io/providers/cartesia-ai/)** — or go straight to one of the APIs or properties below.

### APIs (22)

- [Cartesia TTS WebSocket API](https://apis.io/apis/cartesia-ai/cartesia-ai-tts-websocket-api/) — Bidirectional, multiplexed WebSocket at wss://api.cartesia.ai/tts/websocket for realtime speech generation. Clients send JSON generation requests keyed by a…
- [Cartesia STT WebSocket API](https://apis.io/apis/cartesia-ai/cartesia-ai-stt-websocket-api/) — Realtime transcription over WebSocket at wss://api.cartesia.ai/stt/websocket. Clients stream raw binary audio in 100ms chunks and issue finalize/close text…
- [Cartesia Agents API](https://apis.io/apis/cartesia-ai/cartesia-ai-agents-api/) — Voice agent configuration and public templates.
- [Cartesia API Keys API](https://apis.io/apis/cartesia-ai/cartesia-ai-api-keys-api/) — Standard API key metadata.
- [Cartesia Auth API](https://apis.io/apis/cartesia-ai/cartesia-ai-auth-api/) — Short-lived, scoped access token generation.
- [Cartesia Calls API](https://apis.io/apis/cartesia-ai/cartesia-ai-calls-api/) — Outbound call placement, batching, and history.
- [Cartesia Datasets API](https://apis.io/apis/cartesia-ai/cartesia-ai-datasets-api/) — Audio/text collections used to build custom fine-tunes and voices.
- [Cartesia Deployments API](https://apis.io/apis/cartesia-ai/cartesia-ai-deployments-api/) — Agent deployment inspection.
- [Cartesia Infill API](https://apis.io/apis/cartesia-ai/cartesia-ai-infill-api/) — Generate audio that smoothly connects two existing audio segments.
- [Cartesia Knowledge Base API](https://apis.io/apis/cartesia-ai/cartesia-ai-knowledge-base-api/) — Documents and folders used by agents.
- [Cartesia Metrics API](https://apis.io/apis/cartesia-ai/cartesia-ai-metrics-api/) — LLM-as-a-judge quality metrics for agents.
- [Cartesia Phone Numbers API](https://apis.io/apis/cartesia-ai/cartesia-ai-phone-numbers-api/) — Telephony number provisioning and import.
- [Cartesia Pronunciation Dictionaries API](https://apis.io/apis/cartesia-ai/cartesia-ai-pronunciation-dictionaries-api/) — Custom pronunciation overrides referenced by TTS requests.
- [Cartesia Providers API](https://apis.io/apis/cartesia-ai/cartesia-ai-providers-api/) — Linked telephony provider accounts.
- [Cartesia Speech-to-Text API](https://apis.io/apis/cartesia-ai/cartesia-ai-speech-to-text-api/) — Batch transcription of an audio file of any length.
- [Cartesia Status API](https://apis.io/apis/cartesia-ai/cartesia-ai-status-api/) — API health and version.
- [Cartesia Text-to-Speech API](https://apis.io/apis/cartesia-ai/cartesia-ai-text-to-speech-api/) — Single-shot and streamed speech generation over plain HTTP.
- [Cartesia Usage API](https://apis.io/apis/cartesia-ai/cartesia-ai-usage-api/) — Credit and agent usage reporting.
- [Cartesia Voice Changer API](https://apis.io/apis/cartesia-ai/cartesia-ai-voice-changer-api/) — Transform speech into a different target voice.
- [Cartesia Voices API](https://apis.io/apis/cartesia-ai/cartesia-ai-voices-api/) — Voice catalog management and voice cloning.
- [Cartesia Webhooks API](https://apis.io/apis/cartesia-ai/cartesia-ai-webhooks-api/) — Webhook endpoint registration.
- [Cartesia STT API](https://apis.io/apis/cartesia-ai/cartesia-ai-stt-api/) — The STT API from Cartesia — 1 operation(s) for stt.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Cartesia Realtime WebSocket API (TTS + STT)](https://apis.io/asyncapis/cartesia-ai/cartesia-ai-asyncapi/)

#### Event channels (2)

Individual events and webhooks the provider emits.

- [/stt/websocket](https://apis.io/channels/cartesia-ai/stt-websocket/)
- [/tts/websocket](https://apis.io/channels/cartesia-ai/tts-websocket/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/cartesia-ai/](https://apis.io/graphqls/cartesia-ai/cartesia-ai-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [cartesia-ai](https://apis.io/servers/cartesia-ai/cartesia-ai/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Cartesia Ai Agentic Access](https://apis.io/agentic-access/cartesia-ai/cartesia-ai-agentic-access/)

#### Collections (23)

Postman and Open Collection request collections.

- [Cartesia API](https://apis.io/collections/cartesia-ai/open-cartesia/)
- [Cartesia API](https://apis.io/collections/cartesia-ai/open-cartesia-ai/)
- [Cartesia Agents API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-agents-api/)
- [Cartesia Agents API Keys API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-api-keys-api/)
- [Cartesia Agents Auth API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-auth-api/)
- [Cartesia Agents Calls API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-calls-api/)
- [Cartesia Agents Datasets API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-datasets-api/)
- [Cartesia Agents Deployments API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-deployments-api/)
- [Cartesia Agents Infill API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-infill-api/)
- [Cartesia Agents Knowledge Base API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-knowledge-base-api/)
- [Cartesia Agents Metrics API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-metrics-api/)
- [Cartesia Agents Phone Numbers API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-phone-numbers-api/)
- [Cartesia Agents Pronunciation Dictionaries API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-pronunciation-dictionaries-api/)
- [Cartesia Agents Providers API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-providers-api/)
- [Cartesia Agents Speech-to-Text API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-speech-to-text-api/)
- [Cartesia Agents Status API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-status-api/)
- [Cartesia Auth STT API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-stt-api/)
- [Cartesia Agents Text-to-Speech API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-text-to-speech-api/)
- [Cartesia Auth TTS API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-tts-api/)
- [Cartesia Agents Usage API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-usage-api/)
- [Cartesia Agents Voice Changer API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-voice-changer-api/)
- [Cartesia Agents Voices API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-voices-api/)
- [Cartesia Agents Webhooks API](https://apis.io/collections/cartesia-ai/open-cartesia-ai-webhooks-api/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Cartesia — asyncapi rules](https://apis.io/rules/cartesia-ai/cartesia-ai-asyncapi-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Cartesia Ai Authentication](https://apis.io/security/cartesia-ai/cartesia-ai-authentication/)
- [Cartesia Ai Domain Security](https://apis.io/security/cartesia-ai/cartesia-ai-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Cartesia Ai Plans Pricing](https://apis.io/plans/cartesia-ai/cartesia-ai-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Cartesia Ai Rate Limits](https://apis.io/rate-limits/cartesia-ai/cartesia-ai-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Cartesia Ai Finops](https://apis.io/finops/cartesia-ai/cartesia-ai-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://cartesia.ai/)
- [Documentation](https://docs.cartesia.ai)
- [Pricing](https://cartesia.ai/pricing)
- [Blog](https://cartesia.ai/blog)
- [Terms of service](https://cartesia.ai/legal/terms-of-service)
- [Privacy policy](https://cartesia.ai/legal/privacy-policy)
- [GitHub](https://github.com/cartesia-ai)

## API Evangelist rating

**Kin Score 37.9** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 55.5 |
| Contract governance | 11.4 |
| Operational transparency | 10.5 |
| Developer ergonomics | 35.7 |
| Access clarity | 42.1 |

**Agent readiness 22.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | platform (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 10.5** — AI & Biometrics

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cartesia-ai/](https://apis.io/providers/cartesia-ai/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Cartesia: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cartesia-ai/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
