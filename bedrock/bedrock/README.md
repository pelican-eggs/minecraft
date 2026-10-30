# Minecraft Bedrock

The official Minecraft Bedrock (Formerly Minecraft Pocket Edition) server.

This is an alpha release server from the mojang team.

### Server Ports

Since 1.26.50 Bedrock uses the NetherNet (WebRTC) transport. Clients do a TCP signaling handshake on the
primary port, then BDS hands each player one UDP port from the `NetherNet UDP Ports` range.

Assign the primary allocation **plus** every port in the UDP range as additional allocations
(at least one per player, `max-players`), and set `Public IP` to the IP players connect to.
It must be an IP, not a hostname. If the range is not allocated, players time out after the handshake.

| Port            | default       |
|-----------------|---------------|
| Signaling (TCP) | 19132         |
| Gameplay (UDP)  | 19140-19155   |

### Known Issues
Also see the [Mojang Issue tracker](https://bugs.mojang.com/projects/BDS/issues/)

* On start the server will report is is listening on port 19132 but is listening on the correct port
* Constant `NO LOG FILE` in the console before every log line.
* Server chat is not printed to the console.
* when you set ops in game they do not get saved.

### arm64
* The arm64 may not perform as expected due to the amd64 to arm emulaton.
