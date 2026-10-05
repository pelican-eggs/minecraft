# CurseForge Generic

## This is a generic egg for CurseForge modpacks

You will need to give it a modpack project ID. The project ID for [All the Mods 8 - ATM8](https://www.curseforge.com/minecraft/modpacks/all-the-mods-8) is `520914` for example.
This can be found on the modpack page in the `About Project` section in the right sidebar.

You can also optionally specify a file ID. If you do not specify a file ID, the latest version will be used. 
The file ID for the server pack for [All the Mods 8 - ATM8](https://www.curseforge.com/minecraft/modpacks/all-the-mods-8) version `1.0.17` is `4504876` for example. 
This can be found on the modpack page by clicking the wanted file and copying the id at the end of the URL (the number after `/files/`).

The script will automatically setup of Forge, Fabric, or Quilt depending on the modpack.

You *must* specify a CurseForge API key. 
You can obtain an API key by creating a developer account [here](https://console.curseforge.com/) and then clicking on the "API keys" tab.

## Installing an uploaded ZIP

Set the project ID to `zip` and upload `server.zip` before reinstalling. The archive can contain a CurseForge `manifest.json`, including one exported by Packwiz, or an already prepared server. Native Packwiz `pack.toml` files are not supported.

A prepared server must include a nonempty `unix_args.txt`, or a `.serverjar` file containing the relative path to its server JAR without spaces. For example, a ZIP with `server.jar` should also contain `.serverjar` with `server.jar` as its contents. A ZIP with neither a supported manifest nor usable startup files fails installation.

Manifest installs support Forge, Fabric, NeoForge, and Quilt. All required mods must download successfully; a missing required mod fails the installation.

## Server Ports

The minecraft server requires a single port for access (default 25565) but plugins may require extra ports to enabled for the server.

| Port  | Default |
|-------|---------|
| Game  | 25565   |
