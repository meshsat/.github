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
| **[MeshSat Hub](https://github.com/meshsat/meshsat-hub)** | Multi-tenant fleet management for a fleet of bridges. Currently a private beta with no public sign-up. |
| **[meshsat-website](https://github.com/meshsat/meshsat-website)** | meshsat.net, the documentation site, and the install script. |

MeshSat began inside the [CubeOS](https://github.com/cubeos-app) project and has outgrown it. The
repositories moved here in August 2026; old `cubeos-app` links redirect.
[`meshsat/meshsat`](https://github.com/meshsat/meshsat) is the place to start.

## Get started

```bash
docker compose up -d   # see the Bridge README for the compose file
```

Then open `http://<your-ip>:6050`.

## Talk to us

- **Matrix:** [`#meshsat:matrix.nuclearlighters.net`](https://matrix.to/#/%23meshsat%3Amatrix.nuclearlighters.net)
- **Website:** [meshsat.net](https://meshsat.net) and [docs.meshsat.net](https://docs.meshsat.net)
- **Elsewhere:** [X](https://x.com/meshsat) and [LinkedIn](https://www.linkedin.com/company/meshsat/)
- **Email:** info@meshsat.org

Bug reports from people running unusual hardware are the most useful thing you can send us. The
supported-device tables are short because they only list what we have physically run.

## Funding

Supported by [SIDN fonds](https://www.sidnfonds.nl/projecten/meshsat-keeping-people-connected-when-the-network-is-not).
A six month field programme starts in November 2026.

## License

Everything here is free software under the **GPLv3**. Built in Leiden, the Netherlands, by Elli and
Kyriakos.
