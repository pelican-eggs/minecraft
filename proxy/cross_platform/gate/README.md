# Gate Minecraft Proxy

Gate is an ultra lightweight, high-performance Minecraft reverse proxy from [Minekube](https://gate.minekube.com), written in Go.

This egg configures [Lite mode](https://gate.minekube.com/guide/lite) by default, see the [Gate docs](https://gate.minekube.com/guide/quick-start.html) for full configuration options.

## Server Ports

The proxy requires a single port for access, this is set by the primary server port allocation in Pelican.

## Egg Variables

| Variable | Description |
|----------|-------------|
| Gate Version | Release tag to install, or `latest`. |
| Initial Config Template | `gate config -t` template to be used only if no `config.yml` exists yet (full, simple, lite, bedrock, minimal). |
| Receive PROXY Protocol | Sets `config.proxyProtocol`. Use if your proxy is running behind a TCP proxy. |
