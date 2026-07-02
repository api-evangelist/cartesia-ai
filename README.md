# Cartesia (cartesia-ai)

Cartesia builds real-time voice AI - the Sonic family of text-to-speech models, Ink speech-to-text models, and a Voice Agents platform for building and deploying telephone and web voice agents. The core generation surface is exposed both as REST (bytes and Server-Sent Events) and as a low-latency, bidirectional WebSocket protocol at `wss://api.cartesia.ai` for streaming TTS and STT with multiplexed contexts, word/phoneme timestamps, and mid-stream flush and cancel.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cartesia-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cartesia-ai/refs/heads/main/apis.yml)

## Tags

- AI
- Voice AI
- Text to Speech
- Speech to Text
- Realtime
- WebSocket
- Voice Cloning
- Voice Agents

## Timestamps

- **Created:** 2026-07-02
- **Modified:** 2026-07-02

## APIs

### Cartesia Text-to-Speech API

Synthesize speech from text with the Sonic model family (sonic-3.5, sonic-3, sonic-latest) over plain HTTP - a single-shot binary response at `POST /tts/bytes` or a Server-Sent Events stream with per-chunk metadata at `POST /tts/sse`. Supports 40+ languages, raw/wav/mp3 output formats, and generation controls for volume, speed, and emotion.

- **Human URL:** [https://docs.cartesia.ai/api-reference/tts/bytes](https://docs.cartesia.ai/api-reference/tts/bytes)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- Text to Speech
- Sonic
- Audio

#### Properties

- [Documentation](https://docs.cartesia.ai/build-with-cartesia/tts-models/latest)
- [API Reference](https://docs.cartesia.ai/api-reference/tts/bytes)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cartesia TTS WebSocket API

Bidirectional, multiplexed WebSocket at `wss://api.cartesia.ai/tts/websocket` for realtime speech generation. Clients send JSON generation requests keyed by a `context_id` (continuing a context preserves prosody across chunks of transcript) and receive base64-encoded audio chunks, optional word and phoneme timestamps, flush acknowledgements, and a final done message. A single connection scales to dozens of concurrent generation contexts.

- **Human URL:** [https://docs.cartesia.ai/api-reference/tts/websocket](https://docs.cartesia.ai/api-reference/tts/websocket)
- **Base URL:** `wss://api.cartesia.ai`

#### Tags

- WebSocket
- Text to Speech
- Realtime
- Streaming

#### Properties

- [Documentation](https://docs.cartesia.ai/api-reference/tts/websocket)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/cartesia-ai-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Cartesia Speech-to-Text API

Batch transcription of an audio file of any length with the ink-whisper model at `POST /stt`. Accepts flac, m4a, mp3, mp4, and mpeg uploads, 99+ languages, and optional word-level timestamp granularity.

- **Human URL:** [https://docs.cartesia.ai/api-reference/stt/transcribe](https://docs.cartesia.ai/api-reference/stt/transcribe)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- Speech to Text
- Transcription
- Ink Whisper

#### Properties

- [Documentation](https://docs.cartesia.ai/build-with-cartesia/stt/latest)
- [API Reference](https://docs.cartesia.ai/api-reference/stt/transcribe)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cartesia STT WebSocket API

Realtime transcription over WebSocket at `wss://api.cartesia.ai/stt/websocket`. Clients stream raw binary audio in 100ms chunks and issue finalize/close text commands; the server returns incremental and final transcript messages with word-level timing. A companion "Auto" variant at `/stt/turns/websocket` adds built-in turn detection for conversational agents.

- **Human URL:** [https://docs.cartesia.ai/api-reference/stt/websocket](https://docs.cartesia.ai/api-reference/stt/websocket)
- **Base URL:** `wss://api.cartesia.ai`

#### Tags

- WebSocket
- Speech to Text
- Realtime
- Turn Detection

#### Properties

- [Documentation](https://docs.cartesia.ai/api-reference/stt/turns/websocket)
- [API Reference](https://docs.cartesia.ai/api-reference/stt/websocket)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/cartesia-ai-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Cartesia Voices API

Manage the voice catalog - list, search, and filter voices by gender, language, and ownership; get, update, and delete a voice; clone a new voice from an uploaded audio clip at `POST /voices/clone`; and localize an existing voice into a new language and dialect at `POST /voices/localize`.

- **Human URL:** [https://docs.cartesia.ai/api-reference/voices/list](https://docs.cartesia.ai/api-reference/voices/list)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- Voices
- Voice Cloning
- Localization

#### Properties

- [API Reference](https://docs.cartesia.ai/api-reference/voices/list)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cartesia Voice Changer API

Transform an input speech recording into a different target voice - a single-shot binary response at `POST /voice-changer/bytes` or a Server-Sent Events stream at `POST /voice-changer/sse`.

- **Human URL:** [https://docs.cartesia.ai/api-reference/voice-changer/bytes](https://docs.cartesia.ai/api-reference/voice-changer/bytes)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- Voice Changer
- Audio
- Speech to Speech

#### Properties

- [API Reference](https://docs.cartesia.ai/api-reference/voice-changer/bytes)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cartesia Infill API

Generate audio that smoothly connects two existing audio segments at `POST /infill/bytes` - supply a left and/or right audio clip plus the transcript to be spoken between them, useful for fixing or extending existing voice recordings without a full re-record.

- **Human URL:** [https://docs.cartesia.ai/api-reference/infill/bytes](https://docs.cartesia.ai/api-reference/infill/bytes)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- Infill
- Audio Editing
- Sonic

#### Properties

- [API Reference](https://docs.cartesia.ai/api-reference/infill/bytes)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cartesia Datasets API

Create, list, get, update, and delete datasets, and upload, list, and delete files within a dataset - the audio/text collections used to build custom fine-tunes and voices.

- **Human URL:** [https://docs.cartesia.ai/api-reference/datasets/list](https://docs.cartesia.ai/api-reference/datasets/list)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- Datasets
- Fine-Tuning
- Files

#### Properties

- [API Reference](https://docs.cartesia.ai/api-reference/datasets/list)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cartesia Pronunciation Dictionaries API

Create, list, get, update, and delete custom pronunciation dictionaries that can be referenced by `pronunciation_dict_id` on TTS requests to override how specific words or terms are spoken.

- **Human URL:** [https://docs.cartesia.ai/api-reference/pronunciation-dicts/list](https://docs.cartesia.ai/api-reference/pronunciation-dicts/list)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- Pronunciation
- Dictionaries
- Text to Speech

#### Properties

- [API Reference](https://docs.cartesia.ai/api-reference/pronunciation-dicts/list)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cartesia API Keys and Auth API

List and get metadata for standard API keys, and mint short-lived (up to 3600s) scoped access tokens at `POST /access-token` with tts/stt/agent grants for safe use in browser and client-side contexts.

- **Human URL:** [https://docs.cartesia.ai/api-reference/api-keys/list](https://docs.cartesia.ai/api-reference/api-keys/list)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- API Keys
- Authentication
- Access Tokens

#### Properties

- [API Reference](https://docs.cartesia.ai/api-reference/api-keys/list)
- [Documentation](https://docs.cartesia.ai/api-reference/auth/access-token)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cartesia Voice Agents API

Build and operate voice agents end to end - manage agents and public templates; place, list, cancel, and batch outbound calls and download call audio and logs; import, provision, and manage telephony phone numbers and provider accounts; register webhooks; inspect deployments; and maintain a knowledge base of documents and folders plus LLM-as-a-judge metrics used to evaluate agent quality.

- **Human URL:** [https://docs.cartesia.ai/api-reference/agents/agents/list](https://docs.cartesia.ai/api-reference/agents/agents/list)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- Voice Agents
- Telephony
- Calls
- Knowledge Base

#### Properties

- [API Reference](https://docs.cartesia.ai/api-reference/agents/agents/list)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cartesia Usage API

Read-only usage endpoints returning credit consumption and agent usage over time, bucketed by the requested interval, for monitoring spend against a plan's included credits.

- **Human URL:** [https://docs.cartesia.ai/api-reference/usage/credits](https://docs.cartesia.ai/api-reference/usage/credits)
- **Base URL:** `https://api.cartesia.ai`

#### Tags

- Usage
- Credits
- Billing

#### Properties

- [API Reference](https://docs.cartesia.ai/api-reference/usage/credits)
- [API Reference](https://docs.cartesia.ai/api-reference/usage/agents)
- [OpenAPI](openapi/cartesia-ai-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cartesia-ai.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cartesia-ai.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/cartesia-ai)
- [LinkedIn](https://www.linkedin.com/company/cartesia-ai)
- [Website](https://cartesia.ai/)
- [Documentation](https://docs.cartesia.ai)
- [Plans](plans/cartesia-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/cartesia-ai-rate-limits.yml)
- [Fin Ops](finops/cartesia-ai-finops.yml)

## Review

Cartesia is one of the few providers in this catalog with a **documented public WebSocket API** - see [review.yml](review.yml). Both the TTS WebSocket (`wss://api.cartesia.ai/tts/websocket`) and the STT WebSocket (`wss://api.cartesia.ai/stt/websocket`, plus a turn-detecting `/stt/turns/websocket` variant) are confirmed, bidirectional protocols with published message schemas, modeled in full in [asyncapi/cartesia-ai-asyncapi.yml](asyncapi/cartesia-ai-asyncapi.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
