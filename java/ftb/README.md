# FTB Modpacks

A generic service to pull FTB modpacks from the official FTB API at api.feed-the-beast.com.
There are 2 ways to install a server through this service.
The first method only requires you to know the modpacks name and version.
The second method requires you to know the id for both the modpack and version in the api.

## Method 1 (Recommended) - Search by Name

Use this method when you know the modpack name and version string. This is the easiest approach for most users.

*NOTE*: If the search term contains a space (to avoid multiple entries), you may want to use Method 2 instead to avoid issues.

### Required Variables:

- `FTB_SEARCH_TERM`: The modpack name to search for (minimum 4 characters!)
- `FTB_VERSION_STRING`: The exact version string you want to install

### Examples:

**FTB Evolution:**
- Search Term: `evolution`
- Version String: `1.22.0`

**FTB Revelation:**
- Search Term: `revelations`
- Version String: `3.7.0`

## Method 2 (Safe Approach) - Direct API IDs

Use this method if you know the exact API IDs. You can find these IDs through the official FTB website in the "Developer/Server Admin" section or by inspecting the API directly.

### Required Variables:

- `FTB_MODPACK_ID`: The numeric ID of the modpack in the API
- `FTB_MODPACK_VERSION_ID`: The numeric ID of the specific version

### Examples:

**FTB Evolution (ID: 125):**
- Modpack ID: `125`
- Version 1.22.0 ID: `100130`
- API URL: `https://api.feed-the-beast.com/v1/modpacks/public/modpack/125/100130`

**FTB Revelation (ID: 35):**
- Modpack ID: `35`
- Version 3.7.0 ID: `12180`
- API URL: `https://api.feed-the-beast.com/v1/modpacks/public/modpack/35/12180`

### Finding API IDs:

1. Visit the FTB website and navigate to your desired modpack
2. Look for the "Developer/Server Admin" section in the sidebar
3. The modpack ID and version IDs will be listed there
4. Alternatively, you can inspect the API directly at `https://api.feed-the-beast.com/v1/modpacks/public/modpack/{ID}`

## Server Ports

The Minecraft server requires a single port for access (default 25565) but plugins may require extra ports to enabled for the server.

| Port | default |
| ---- | ------- |
| Game | 25565   |

## Troubleshooting

### Problem with server.properties

Not all FTB packs come with a `server.properties` file. This results in the server not being able to set the server-ip and server-port automatically.
If this happens, restart the server once after the first launch to generate a new `server.properties` file.

### Neoforge

If you have trouble using a Neoforge modpack, make sure to select the latest Java yolk.

### Java Version

The required Java version is also listed on the modpack page under the "Requirements" section. Configure the yolk accordingly.


## Credits

This egg was originally created by [Runemaster580](mailto:runemaster580@gmail.com) and has been modified to improve functionality and implement the new official FTB API.
