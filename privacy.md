---
title: Honey Bee Troop — Privacy Policy
---

# Privacy Policy — Honey Bee Troop

_Last updated: August 9, 2026_

Honey Bee Troop is a local-first meeting notes app for macOS, built by
Lahiru. This policy explains what data the app touches and where it goes.

## Summary

- No account or sign-in.
- No analytics, tracking, or advertising SDKs of any kind.
- Audio, transcripts, and notes are processed and stored **on your device**
  by default.
- Data leaves your device only if you explicitly configure an optional
  cloud AI provider.

## Data the app processes

**Microphone and system audio.** Used to record meetings and voice notes
you start (automatically or manually). Recordings are transcribed on-device
using Apple's Speech framework (`SFSpeechRecognizer`, on-device mode) and
are stored locally in the app's sandboxed container.

**Screen Recording permission.** Requested only to capture system audio via
ScreenCaptureKit — the only sandbox-legal API for capturing the other side
of a call on macOS. No video frame or screen content is ever read, stored,
or transmitted.

**Notes, transcripts, and tags.** Generated on-device by default, using a
small open-source AI model that runs locally. Stored locally on your Mac.

**Speaker diarization.** Runs on-device (CoreML). No audio is sent anywhere
to identify speakers.

## Optional cloud features

If you choose to connect an AI provider in Settings (Ollama on your own
server, OpenAI, Anthropic Claude, or another OpenAI-compatible endpoint),
transcript text is sent to that provider using your own API key to generate
notes, summaries, and tags. This is off by default, entirely optional, and
governed by that provider's own privacy policy and terms. Honey Bee Troop
does not operate any server of its own and does not see or store this data.

## What we don't do

- We don't collect analytics or usage telemetry.
- We don't use third-party tracking or advertising SDKs.
- We don't sell or share your data — we don't have it; it stays on your
  device unless you choose to send it to a provider you configured.

## Model downloads

The app downloads open-weight model files from Hugging Face for the
on-device AI backend. Only model weights (data) are downloaded, never
executable code. This is a one-time download used to run features locally.

## Data retention and deletion

All notes, transcripts, and recordings are stored locally in the app's
sandboxed container. Deleting a note in the app deletes its data.
Uninstalling the app removes its container and all associated data.

## Changes to this policy

If this policy changes, the "Last updated" date above will change
accordingly.

## Contact

Questions about this policy: **lahirugmg@gmail.com**

---

[Back to Support](index.html)
