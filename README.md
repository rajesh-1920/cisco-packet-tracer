# Cisco Packet Tracer — Lab Practice

Hands-on labs for **Cisco Packet Tracer**: the topologies (`.pkt`) plus the configs and
verification steps for each one. Focus is CCNA-level networking — switching, VLANs,
routing, IP services and security.

## Requirements

**Cisco Packet Tracer 9.x** — free. Enrol in the short *Getting Started with Cisco Packet
Tracer* course at <https://www.netacad.com> to get the download.

## Clone

```bash
git clone https://github.com/rajesh-1920/cisco-packet-tracer.git
cd cisco-packet-tracer
```

## Labs

| Lab | Topic |
| --- | --- |
| [`01.hub-based-lan-connection-among-4pc.pkt`](algo-bangla-youtube/01.hub-based-lan-connection-among-4pc.pkt) | LAN with a hub |
| [`02.switch-to-switch-lan-connection.pkt`](algo-bangla-youtube/02.switch-to-switch-lan-connection.pkt) | LAN between two switches |

## Running a lab

Open a lab with **File → Open** in Packet Tracer, or double-click the `.pkt` file.

Use **Realtime** mode for `ping` and CLI checks, then **Simulation** mode to watch the
actual PDUs move between devices.

## Adding a lab

Drop the `.pkt` in with the other labs, add a `README.md` next to it covering the goal,
the config and the verification commands, then add a row to the table above.
