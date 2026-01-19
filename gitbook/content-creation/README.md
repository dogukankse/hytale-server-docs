# Content Creation (Packs)

Hytale **Packs** allow you to add new blocks, items, mobs, and behavior to the game without requiring deep coding knowledge.

## Getting Started

### 1. Create a Pack Folder
Navigate to your Hytale directory:
`%appdata%/Roaming/Hytale/UserData/Mods/`

Create a folder with your pack name, e.g., `MyFirstPack`.

### 2. Manifest File
Every pack requires a `manifest.json` in its root folder.

```json
{
  "Group": "YourGroup",
  "Name": "MyFirstPack",
  "Version": "1.0.0",
  "Description": "My first content pack!",
  "Authors": [
    {
      "Name": "YourName"
    }
  ],
  "ServerVersion": "*"
}
```

### 3. Folder Structure
Inside your pack folder, create two main subfolders:

- **Common/**: For client-side assets (Models, Textures, Sounds).
- **Server/**: For game logic (Items, Blocks, Behaviors).

#### Example Structure
```
MyFirstPack/
├── manifest.json
├── Common/
│   ├── Models/
│   └── Textures/
└── Server/
    ├── Block/
    └── Item/
```

### 4. Activating Your Pack
1. Open Hytale.
2. Go to **Worlds** > Right-click your world > **Edit**.
3. Toggle your pack to **ON**.
