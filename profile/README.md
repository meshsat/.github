# MeshSat

### Keeping people connected when the network is not.

When a storm, an outage or a disaster takes the network down, the radios people already own mostly
cannot help. A Meshtastic LoRa mesh keeps a village talking to itself, but it has no route out of
the valley. A satellite modem can reach the far side of the planet, but it costs real money per
message and almost nobody carries one. A phone is useless without a tower.

MeshSat is the piece in between: open source gateways that take a message off a local mesh and find
a way out over whatever bearer is still alive. Eight transport bearers, reachable across nine wired
Reticulum interfaces, with cost-aware routing so traffic stays on the free bearers and only reaches
for the metered ones when nothing free is left.

> **Pre-release.** These are working prototypes under active development, not finished products.
> Nothing here has been deployed to a real user or used in an actual emergency. Each repository
> states plainly what has run on hardware and what has not.

## Projects

| | What it is |
|---|---|
| **[MeshSat Bridge](https://github.com/meshsat/meshsat)** | The gateway. Go, runs as a Docker container on a Raspberry Pi. Meshtastic LoRa, Iridium satellite, cellular SMS, APRS/AX.25, ZigBee, BLE, TAK and MQTT, routed over Reticulum. |
| **[MeshSat Android](https://github.com/meshsat/meshsat-android)** | Standalone mobile gateway. Kotlin and Compose, with BLE mesh, SPP Iridium and native SMS. |
| **[MeshSat Hub](https://github.com/meshsat/meshsat-hub)** | Multi-tenant fleet management for a fleet of bridges. Sign-up at [hub.meshsat.net](https://hub.meshsat.net) is open, and each account is approved by hand before it activates. |
| **[meshsat-website](https://github.com/meshsat/meshsat-website)** | meshsat.net, the documentation site, and the install script. |
| **[MeshSat Field Kit](https://github.com/meshsat/meshsat-fieldkit)** | The hardware. The two kits built so far (tesseract and parallax: Pi 5, UPS, five radios and a satellite modem in an IP67 case) with their build guide, and the V2 carrier PCB set for a Peli 1520 case: KiCad sources, the scripts that generate the boards, the case CAD, the Rev A release files. Rev A is designed and prepared for fabrication, not built yet. |
| **[MeshSat node](https://github.com/meshsat/meshsat-esp32)** | A pocket-sized node: a Meshtastic LoRa radio and a RockBLOCK 9603 Iridium modem in one small case, paired with MeshSat Android over a single Bluetooth link. Hardware versions, wiring, the Iridium Bluetooth service contract and bench tools. v1, on a LILYGO T-Beam Supreme, has run since 21 September 2026 and, since 27 September, carries a mesh channel over Iridium on its own when no phone is connected. |
| **[meshsat-firmware](https://github.com/meshsat/meshsat-firmware)** | The node's firmware: a fork of the Meshtastic firmware that adds an Iridium serial service next to the Meshtastic one. Based on Meshtastic® firmware; not affiliated with or endorsed by Meshtastic LLC. |
| **[meshsat-lora-backplate](https://github.com/meshsat/meshsat-lora-backplate)** | The Pine64 LoRa back cover on a PinePhone Pro as a Meshtastic node under Linux, then the phone as a pocket MeshSat gateway. Just started; nothing has run on hardware yet. |
| **[meshsat-sx1262-driver-android](https://github.com/meshsat/meshsat-sx1262-driver-android)** | MeshSat Android as a Meshtastic node on a PinePhone Pro: a Kotlin driver for the back cover's radio and Meshtastic's mesh layer in Kotlin. Just started; nothing has run on hardware yet. |

MeshSat began inside the [CubeOS](https://github.com/cubeos-app) project and has outgrown it. The
repositories moved here in August 2026; old `cubeos-app` links redirect.
[`meshsat/meshsat`](https://github.com/meshsat/meshsat) is the place to start.

## Get started

```bash
docker compose up -d   # see the Bridge README for the compose file
```

Then open `http://<your-ip>:6050`.

## Talk to us

- **Matrix:** [`#meshsat:matrix.nuclearlighters.net`](https://matrix.to/#/#meshsat:matrix.nuclearlighters.net)
- **Website:** [meshsat.net](https://meshsat.net) and [docs.meshsat.net](https://docs.meshsat.net)
- **Elsewhere:** [X](https://x.com/meshsat) and [LinkedIn](https://www.linkedin.com/company/meshsat/)
- **Email:** info@meshsat.org

Bug reports from people running unusual hardware are the most useful thing you can send us. The
supported-device tables are short because they only list what we have physically run.

## Funding

Supported by [SIDN fonds](https://www.sidnfonds.nl/projecten/meshsat-keeping-people-connected-when-the-network-is-not).
A six month field programme starts in November 2026.

## License

The software is free software under the **GPLv3**, except the Hub, which is **Apache 2.0**; the
hardware repository is released under the **CERN-OHL-S-2.0**. Built in Leiden, the Netherlands, by Elli and Kyriakos.
