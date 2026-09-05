# Tracelucid

An intelligent network traffic analyzer — conceptually similar to Wireshark, but built to explain what's happening in network traffic to people without deep networking knowledge, while keeping every conclusion traceable back to raw packet evidence. Cross-platform desktop app (Windows, Linux; macOS untested — no Mac available during development).

**Website:** https://djbrar.github.io/tracelucid-releases/
**Guide:** https://djbrar.github.io/tracelucid-releases/guide.html

## This repo

This repository holds only the built installers and the project's landing page (via GitHub Pages) — no source code. Tracelucid's source lives in a private repository; this split keeps release binaries public without requiring the source itself to be open.

## Download

Installers for Windows (`.msi`, `.exe`) and Linux (`.deb`, `.rpm`, `.AppImage`) are on the [Releases page](https://github.com/djbrar/tracelucid-releases/releases/latest). [Wireshark](https://www.wireshark.org/download.html) must be installed separately — Tracelucid drives its `tshark`/`dumpcap` tools rather than bundling them. See the release notes for full per-platform install steps.

## What it does

- Import PCAP/PCAPNG files (single or merged), or capture live traffic from a network interface
- Reconstructs TCP/UDP/ICMP flows and DNS conversations from the raw packet stream
- Deterministic analysis: TCP state/retransmissions/duplicate ACKs, DNS success/failure, IP fragmentation and PMTU issues, handshake and DNS response latency, asymmetric routing paths
- A transparent, weighted network health score — never a black-box number, always shows which factors contributed and why
- Evidence-linked findings — title, severity, confidence, possible causes, recommended actions, and the exact packets behind each one
- Follow Stream — reassembles one TCP/UDP/HTTP conversation into a readable transcript, click-to-jump to the underlying packet
- Optional, opt-in AI explanations and IP reputation lookups — both off by default, nothing leaves your machine unless you enable them
- PDF report export with section selection

## Support

- **Found a bug?** [Open an issue](https://github.com/djbrar/tracelucid-releases/issues/new)
- **General feedback?** project.tracelucid@gmail.com

## License

MIT.
