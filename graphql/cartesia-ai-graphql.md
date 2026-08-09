# Cartesia GraphQL Schema

This document describes a conceptual GraphQL schema for the Cartesia real-time text-to-speech and voice cloning API. Cartesia's native interfaces are REST, server-sent events, and WebSocket; this schema models those capabilities as a GraphQL surface to support tooling, federation, and developer exploration.

## Coverage

The schema covers the full Cartesia API surface across both Sonic (TTS) and Ink (STT) product lines:

- **Voice Library** — query, filter, and inspect prebuilt and custom voices
- **Voice Cloning** — instant and professional clone creation and status tracking
- **Text-to-Speech** — synchronous renders and streaming output chunks
- **Speech-to-Text** — transcript creation with sentence and word granularity
- **Prosody Controls** — emotion, speed, pitch, and output speed configuration
- **Models** — enumerate Sonic and Ink model versions and their capabilities
- **Render Jobs** — async render lifecycle and job status
- **Usage and Billing** — character counts, audio minutes, and rate limit state
- **Auth** — API key and token management
- **Webhooks** — webhook endpoint registration and event types
- **Errors** — structured error envelopes with rate limit metadata

## File

- `cartesia-schema.graphql` — full GraphQL SDL with 55+ named types

## Source

- API Reference: https://docs.cartesia.ai/api-reference
- Documentation: https://docs.cartesia.ai
- Provider: https://cartesia.ai
