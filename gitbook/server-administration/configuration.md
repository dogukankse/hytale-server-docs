# Server Configuration

## Configuration Files

The main configuration file is `config.json` located in the server root. World-specific settings are in `universe/worlds/<world_name>/config.json`.

### Basic `config.json` Example
```json
{
  "max-players": 10,
  "view-distance": 12,
  "port": 5520,
  "bind-address": "0.0.0.0"
}
```

## Performance Settings
- **Memory:** Use `-Xmx` flag to set max RAM (e.g., `-Xmx8G`).
- **View Distance:** Lowering `view-distance` significantly improves performance.

## World Configuration
- **Seed:** Set in world config or via command arguments.
- **Game Mode:** Default game mode for new players.

---

# Hytale Server Manager (HSM)

HSM is a community tool for managing Hytale servers.
**Repository:** [nebula-codes/hytale_server_manager](https://github.com/nebula-codes/hytale_server_manager)

### Features
- Web Interface
- Mod/Plugin Management
- Automatic Backups
- Auto-updates

### Installation
1. Download the latest release from GitHub.
2. Run the installer/executable.
3. Configure the path to your Hytale Server instance.

### Usage
- Start HSM and access the web dashboard (usually `localhost:3000` or configured port).
- Use the dashboard to stop/start the server, view logs, and manage players.
