# In My Time — Showcase

**Live at [inmytime.app](https://inmytime.app)** · Try the no-sign-up demo at [inmytime.app/storycatcher/demo](https://inmytime.app/storycatcher/demo)

*Helping families capture the stories of the people they love — in their own voices, in their own time.*

This repository is the public showcase for **In My Time**, a small suite of tools for
preserving family memory, built by [Barry Sisk](https://github.com/BBSISK), a maths teacher
and developer in Limerick, Ireland. The application source is kept in a private repository;
this page explains what the project is, how it works, and the principles behind it.

> Currently in beta with real families. Feedback is very welcome — open an issue here or
> get in touch through the site.

---

## StoryCatcher — record a life, privately

StoryCatcher lets a family member sit down with a parent, grandparent or friend, ask good
questions, and keep the answers as audio or video — organised on a **LifeLine** timeline the
whole family can return to for years.

### Start with a photograph

The best conversations often begin with a photo. StoryCatcher has a photograph-first route:

1. Gather the printed photographs and sit down together.
2. Tap **Start with a photograph** and talk your way through each one.
3. Press Stop, then snap or upload the photos you discussed — they're attached to the recording.
4. On a laptop? Scan the on-screen **QR code** with your phone, take the picture, and it
   appears on the laptop in seconds. No app, no sign-in on the phone.
5. Photos appear as thumbnails on the LifeLine and in playback, and can be swapped for a
   better scan later.

### What's in it

- **Curated questions** — a free starter pack and themed packs, with gentle cues during recording
- **Time Traveler** — personalised, chronological questions built from the person's birth
  year, place and life events, with regional historical milestones dropped onto their timeline
- **LifeLine** — a colour-graded timeline of recordings, photos, notes and milestones
- **Capture a chat** — no script needed, just press record
- **Hands-free recording** and offline queueing, so nothing is lost to a bad connection
- **Interviewee portal** — the storyteller can listen back from any browser
- **Your storage, your choice** — managed storage, or your own Google Drive
- **Multilingual** — English, German, French and Spanish
- **Interactive demo** — runs entirely in your browser with sample data

## Private by design: zero-knowledge encryption

Family recordings are some of the most personal data there is. In StoryCatcher:

- Everything — audio, video, photographs, names — is **encrypted in your browser** before it
  leaves your device.
- The server stores **only ciphertext**. The keys live on your devices; the service cannot
  read your content, even if it wanted to.
- Photos sent from a phone to a laptop use a **one-time key that exists only in the QR code's
  URL fragment** — browsers never send that part to a server. The relay holds the encrypted
  photo for minutes, then deletes it.
- Optional recovery lets you restore an archive after losing a device — still without the
  server ever seeing a key.

The honest flip side: because we can't read your recordings, we can't recover them for you
either. The design takes that trade deliberately.

## The wider suite

| | |
|---|---|
| **StoryCatcher** | One-to-one recording of a family member's life story (zero-knowledge) |
| **CircleofFriends** | Record a group conversation — a table of friends or relatives together (zero-knowledge) |
| **NationalTapestry** | A shared, moderated timeline of a country's memories across generations |
| **In My Time (WhatsApp)** | A weekly WhatsApp prompt that walks an elder through the chapters of their life |

## Under the hood

Python / Flask · WebCrypto (ECDH P-256, AES-GCM) in the browser · PostgreSQL (SQLite in
development) · Cloudflare R2 and Google Drive for encrypted media · Stripe · Flask-Babel
for translations · deployed on Render.

## Status & roadmap

Beta testing with families in Ireland, with outreach to community and older-adult
organisations. Near-term ideas: pre-loading a shelf of photographs before a session,
encrypted thumbnails, and more languages.

## Get involved

- **Try it:** [inmytime.app](https://inmytime.app)
- **Feedback or questions:** open an [issue](https://github.com/BBSISK/inmytime-showcase/issues) on this repository

© Barry Sisk. All rights reserved; this repository is for information and does not grant a
licence to the private application source.
