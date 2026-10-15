# Case studies

Two shipped, working tools — not just source code — that show the same architecture discipline as the enterprise starter kits, applied to smaller standalone problems.

## car-maintenance — oil-change tracking on iOS/Android

A .NET MAUI reference app for tracking vehicle maintenance history. Demonstrates a real cross-platform build (not a web wrapper), a working data model, and troubleshooting docs written from actual build issues encountered along the way.

Repo: [github.com/qmmughal/car-maintenance](https://github.com/qmmughal/car-maintenance)

*Screenshots: coming soon.*

## Internet Monitor — local-first internet & Wi-Fi monitor (formerly wifi-monitor)

Started as a browser Wi-Fi dashboard that was honest about simulating most of its data. It was
rebuilt around one rule: every number is tagged *measured*, *estimated* or *simulated*, and a
missing reading is shown as missing — never invented. The project was renamed when it grew
beyond Wi-Fi.

What it does today:

- **Any connection** — live upload/download per interface (Wi-Fi, Ethernet, VPN, mobile).
- **Which app is using the internet** — data per app, over minutes or days, and live
  connections per app. On Windows this needs no admin rights: it reads the OS's own usage records.
  A 20 MB test download was attributed to the right process within ~1%.
- **Why it's slow** — a staged troubleshooter (link → router → DNS → HTTPS → latency). Each
  finding comes with evidence, a likely cause, a next step and a confidence level. It also says
  when another app was saturating the link.
- **Wi-Fi** — live signal, channel, band, generation, nearby networks, channel advice and a
  room-by-room signal survey.
- **History** — explainable anomaly alerts. Device discovery is passive by default.
- **Optional extras** — AI explanations (Claude or a local model; off by default; redacted; output
  schema-validated), a token-authenticated multi-machine hub, Prometheus, and Home Assistant via MQTT.

Testing on real hardware drove real fixes. A failed internal Wi-Fi adapter is now reported with its
Device Manager code instead of "no Wi-Fi". A USB adapter's stale scan list led to requesting
fresh scans through the Windows WLAN API. Channel advice learned to recognise the user's own
access points instead of suggesting a move onto one of their channels.

Maturity, labelled honestly: CI-tested on Windows, Linux and macOS. Verified on real Windows 11
hardware over Ethernet and Wi-Fi. Linux and macOS are not yet tested on real hardware.

Repo: [github.com/qmmughal/internet-monitor](https://github.com/qmmughal/internet-monitor) ·
[Usage guide](https://github.com/qmmughal/internet-monitor/blob/main/docs/USAGE.md)

*Screenshots: coming soon.*

---

*This page will get real screenshots as they're captured. Until then, treat the "coming soon" notes as accurate status, not filler.*
