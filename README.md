**English** · [Italiano](README.it.md)

# ASLI

Chat with an AI that runs **entirely on your phone**: the model sits on the
device and the conversation never travels the network. No account, no data
collection.

The app's interface is in Italian.

**This is a beta**: it exists to try the app out and collect reports, and it
may contain defects.

## Installing

1. Download the `.apk` from the [latest release](../../releases/latest).
2. Open it on the phone: Android will ask you to allow installation from
   unknown sources this once.
3. On first launch the app offers to download the model (about 2.6 GB): do it
   over Wi-Fi.

## Requirements

- Android 12 (API 31) or later
- 64-bit ARM (`arm64-v8a`)
- RAM: 7 GB or more, measured
- Free space: about 3.7 GB

Below Android 12 the APK will not install: Android itself refuses it. If the
memory is not enough, the app opens on a screen saying so and stops there,
without offering you the model. ASLI ships a single model tier and no smaller
fallback: a phone that cannot hold it cannot answer at all, and saying so up
front beats making you download 2.6 GB for nothing.

## Updates and withdrawals

The app **does not check for updates on its own**: that is part of the promise
not to use the network. This has a downside worth stating plainly: if a version
is withdrawn over a defect, **nobody warns you on the phone**.

Announcements — new versions and withdrawals — live here: on the
[releases](../../releases) page and on this one. To get an email when a version
ships or is withdrawn, press **Watch → Custom → Releases** at the top of this
page: it is GitHub warning you, not the app.

## Privacy

Conversations and photos stay on the phone, encrypted. The full privacy policy
is published on
[this page](https://andrea-salvadei.github.io/asli-beta/privacy/), in Italian.
