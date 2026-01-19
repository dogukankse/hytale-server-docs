# Setting Up a Server

This guide covers setting up both local and dedicated Hytale servers.

## Prerequisites

- **Java 25** installed (OpenJDK/Adoptium recommended).
- **Hytale** installed via the official launcher.
- Basic command line knowledge.

---

## Setting Up a Local Server

Useful for testing mods, LAN play, or development.

### 1. Locate Server Files
1. Open Hytale Launcher → **Settings** → **Open Directory**.
2. Navigate to: `%appdata%\Hytale\install\release\package\game\latest\`.
3. Copy the **Server/** folder and **Assets.zip** to a new folder (e.g., `C:\HytaleServer\`).

### 2. Launching the Server
Open a terminal in your server directory and run:

```powershell
cd C:\HytaleServer
java -Xmx4G -jar Server\HytaleServer.jar --assets Assets.zip
```

### 3. Connection
- **Local:** `localhost:5520`
- **LAN:** `YourLocalIP:5520` (e.g., `192.168.1.5:5520`)

> [!NOTE]
> Hytale uses **UDP port 5520**. Ensure this port is allowed in your firewall.

### 4. Authentication
You **MUST** authenticate your server to allow connections.
1. In the server console, run: `/auth login device`
2. Visit the printed URL and enter the code.
3. Login with your Hytale account.
4. To save authentication, run: `/auth persistence Encrypted`

> [!WARNING]
> Never share your encrypted auth file!

---

## Running a Dedicated Server

For 24/7 hosting on a VPS or dedicated machine.

### Requirements
- **OS:** Linux (Ubuntu/Debian recommended) or Windows Server.
- **RAM:** 4GB+ recommended.
- **Network:** Static IP or domain name. UDP Port 5520 open.

### Installation Steps
1. Install Java 25.
2. Transfer the `Server/` folder and `Assets.zip` from your local installation to the remote server.
3. Authenticate using the same steps as above (`/auth login device`).

### Firewall Configuration
Ensure **UDP 5520** is open.
- **Windows:** `New-NetFirewallRule -DisplayName "Hytale Server" -Direction Inbound -Protocol UDP -LocalPort 5520 -Action Allow`
- **Linux (UFW):** `sudo ufw allow 5520/udp`

---

## Installing Mods
1. Create a `mods/` directory in your server root.
2. Place `.jar` (plugins) or `.zip` (mods) files into the folder.
3. Restart the server.

## Troubleshooting
- **Server won't start:** Verify Java version (`java --version`) is 25. Check `Assets.zip` path.
- **Can't connect:** Verify firewall allows UDP 5520.
- **Port in use:** Change port with `--bind 0.0.0.0:YourPort` or kill the process using port 5520.
