# Server Commands & Permissions

## Authentication Commands
These are critical for setting up your server.

- `/auth login device`: Initiates the authentication process. Generates a link and code to link the server to your Hytale account.
- `/auth persistence Encrypted`: Saves your authentication session securely. Use this after logging in so you don't have to re-authenticate on every restart.
  > [!WARNING]
  > **Never share your encrypted auth file!** It grants access to your server identity.

## Player Management
- `/op <playername>`: Grants operator status to a player, allowing them to bypass permissions.
- `/deop <playername>`: Removes operator status.
- `/kick <playername> [reason]`: Disconnects a player from the server.
- `/ban <playername> [reason]`: Bans a player preventing them from rejoining.
- `/pardon <playername>`: Unbans a player.

## Permission System
Hytale servers use a group-based permission system. Permissions are typically defined in configuration files or managed via plugins (implementation details may vary by server wrapper).

### Basic Levels
- **Guest:** Default for new players.
- **Operator (OP):** Full administrative access.
