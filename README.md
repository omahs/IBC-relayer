# IBC-relayer
What is IBC?
IBC is a reliable, ordered, and authenticated protocol for relaying arbitrary messages between independent distributed ledgers

StakeWithUs is currently relaying (Using Hermes) for the following projects:

1) Cosmos (ATOM)
2) Osmois (OSMOS)
3) EVMOS (EVMOS)
4) JUNO (JUNO)
4) Injective (INJ)
5) Bandchain (BAND) - Oracle

## Recommended Hardware and OS Configuration ##

OS: Ubuntu 20.04 LTS minimal
* Disable root login
* Change SSH default port
* Use SSH Keys
* Enable UFW and only allow SSH custom port and port 3001 (telemetry) to specific IP (bastion host and monitoring host)

Hardware: Hetzner Bare Metal AX101
* AMD Ryzen 9 5950X
* 128GB DDR4 ECC RAM
* 4 x 3.84TB NVMe SSD RAID 10

We require a more powerful bare metal node due to the fact that we are running relayer full nodes as well to improve the latency in relaying the packets.

## Channels

Chain | Chain-ID | Token | Dst-Chain | Channel | Port
----- | -------- | ----- | --------- | ------- | ----
CosmosHub | cosmoshub-4 | uatom | Osmosis | Channel-141 | Transfer
CosmosHub | cosmoshub-4 | uatom | Juno | Channel-207 | Transfer
CosmosHub | cosmoshub-4 | uatom | Evmos | Channel-292 | Transfer
Osmosis | osmosis-1 | uosmos | CosmosHub | Channel-0 | Transfer
Osmosis | osmosis-1 | uosmos | Juno | Channel-42 | Transfer
Osmosis | osmosis-1 | uosmos | Evmos | Channel-204 | Transfer
Osmosis | osmosis-1 | uosmos | Injective | Channel-122 | Transfer
