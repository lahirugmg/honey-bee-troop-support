---
title: Honey Bee Troop — Privacy Policy
---

# Privacy Policy — Honey Bee Troop

_Last updated: October 27, 2026_

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

**Screen Recording permission.** Used only to capture system audio. See
[Screen Recording data](#screen-recording-data) below.

**Notes, transcripts, and tags.** Generated on-device by default, using a
small open-source AI model that runs locally. Stored locally on your Mac.

**Speaker diarization.** Runs on-device (CoreML). No audio is sent anywhere
to identify speakers.

## Screen Recording data

Honey Bee Troop asks for the macOS Screen Recording permission for one purpose
only: to capture **system audio** (the other people on a call) while a meeting
recording is running. ScreenCaptureKit is the only sandbox-compatible way to
capture system audio on macOS.

- **What is collected:** only the system audio stream. The app requests the
  smallest video stream the API allows (2×2 pixels at 1 frame per second) and
  never reads, stores, or transmits any video frame, screenshot, or screen
  content.
- **How it is used:** the audio is transcribed on your Mac with Apple's
  on-device speech recognition, speakers are separated on-device, and the
  transcript is used to create your meeting notes. It is not used for
  analytics, advertising, profiling, or AI training.
- **Sharing and disclosure:** the audio is never sent to the developer or to
  any third party; Honey Bee Troop operates no server. If you connect an
  optional AI provider (see [Optional cloud features](#optional-cloud-features)),
  only the text transcript (never the audio) is sent to the provider you
  configured, using your own API key.
- **Storage:** recordings are saved only on your Mac, in the app's sandboxed
  container. If you choose a notes folder in Settings, a copy of each note and
  its recording is also written to that folder.
- **Retention:** recordings are kept until you delete the note (which deletes
  its recording and any mirrored copy) or uninstall the app. If you deny
  Screen Recording, the app records the microphone only.

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
sandboxed container. If you chose a notes folder in Settings, mirrored copies
are also kept there. Deleting a note in the app deletes its data, including
its recording and any mirrored copy. Uninstalling the app removes its
container and all associated data.

## Changes to this policy

If this policy changes, the "Last updated" date above will change
accordingly.

## Contact

Questions about this policy: **lahirugmg@gmail.com**

---

[Back to Support](index.html)
