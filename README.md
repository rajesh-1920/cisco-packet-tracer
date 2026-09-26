# Cisco Packet Tracer — Lab Practice

A hands-on lab notebook for **Cisco Packet Tracer**: topologies (`.pkt`), device configs kept as
plain text, and short write-ups for CCNA-level topics — switching, VLANs, routing, OSPF, IP
services and security.

Every lab is self-contained: the topology, the commands, and how to verify it actually works.

## Requirements

- **Cisco Packet Tracer 9.x** — free. Enrol in the short *Getting Started with Cisco Packet
  Tracer* course at <https://www.netacad.com> to get the download.
- Any text editor. `python3` only if you touch the automation scripts.

## Getting started

```bash
git clone https://github.com/rajesh-1920/cisco-packet-tracer.git
cd cisco-packet-tracer
```

Open a lab with **File → Open** in Packet Tracer, or double-click any `.pkt` file.

Use **Realtime** mode for `ping` and CLI checks, then **Simulation** mode to watch the real PDUs
hop between devices — that's where the interesting stuff shows up.

## Layout

| Folder | Topics |
| --- | --- |
| `01-basics` | Device models, cabling, interfaces, CLI navigation |
| `02-switching-vlans` | VLANs, access/trunk ports, VTP, STP |
| `03-routing-static` | Static routes, default gateways, routing table |
| `04-dynamic-routing` | OSPF, RIP, EIGRP, areas |
| `05-ip-services` | DHCP, DNS, NAT/PAT, port forwarding |
| `06-security` | ACLs, port security, SSH vs Telnet |
| `07-wireless` | WLANs, AP configuration, WDS |

Each lab gets its own folder:

```
03-routing-static/static-routes/
├── static-routes.pkt        # the topology
├── configs/                 # running-config / CLI snippets as plain text
├── README.md                # goal, steps, verification
└── screenshots/             # topology and test results
```

## How a write-up is structured

1. **Goal** — what should be true when the lab is done
2. **Topology** — device and IP address table
3. **Steps** — config in order, per device
4. **Verification** — the `show` / `ping` commands and the output you should see
5. **Gotchas** — what broke, and the fix

## Conventions

- `kebab-case` for folders and files; the `.pkt` name matches its folder.
- Configs are **text**, not screenshots — `show running-config` pasted into `configs/`.
- `*.pkt` / `*.pksz` are committed as-is; they're binary, so don't reformat or merge them.
- Topic numbering is fixed — new labs go in the matching existing folder.

## Automation

Optional Python helpers for driving Packet Tracer or parsing output. Virtualenvs, caches and
`__pycache__` are git-ignored; credentials go in `.env` (see `.env.example`), never in code.

## Note

Packet Tracer is Cisco's simulator and `.pkt` files are Cisco's property. This repo is for
personal study and educational use. The configs are my own notes, not Cisco documentation.
