# Treadwell Network

**A decentralized, encrypted, sneakernet-native messaging protocol.**

If current infrastructure fails — or is unavailable, degraded, surveilled, or untrusted — people can still communicate by carrying USB drives between locations. The Treadwell Protocol is built for this scenario.

## What is this repo?

This repository hosts the [treadwell.network](https://treadwell.network) website via GitHub Pages. It contains:

- **`index.html`** — The landing page describing the protocol's design and principles
- **`treadwell-protocol-design.docx`** — The full protocol design document (whitepaper)

## The Protocol

Treadwell replaces traditional message routing with **CRDT state replication**. USB drives carry state snapshots between nodes. Every sync is a bidirectional merge. The network converges naturally, regardless of who carries drives, in what order, or by what path.

### Key Properties

- **No fixed topology** — Runners carry drives in any direction. No servers, no routers, no routing tables.
- **Encrypted by default** — All content is ciphertext. Couriers cannot read what they carry.
- **Transport agnostic** — Designed for USB sneakernet, but works over LoRa, HF radio, TCP/IP, or any delay-tolerant channel.
- **Pluggable domains** — Message bases, private mail, file bases, ledgers, and future types all replicate through the same engine.
- **Metadata-first propagation** — Know what exists across the network before content arrives. Small metadata travels fast; large blobs follow on demand.

## Links

- **Website**: [treadwell.network](https://treadwell.network)
- **Discussion**: [Zulip](https://treadwell.zulipchat.com/)
- **Organization**: [github.com/Treadwell-Network](https://github.com/Treadwell-Network)

## DNS Configuration

To serve this site at `treadwell.network`, configure DNS as follows:

**A records** (apex domain):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME record** (www subdomain):
```
www -> Treadwell-Network.github.io
```

Then enable GitHub Pages in the repo settings (Settings → Pages → Source: main branch, root directory). GitHub will provision a TLS certificate automatically.

## License

This project's design documents and website content are shared for community discussion and development. See individual files for specific terms.
