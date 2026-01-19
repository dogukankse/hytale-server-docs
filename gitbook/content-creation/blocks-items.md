# Blocks and Items

## Adding Items
Items are the core of interaction in Hytale. They are defined in JSON files within your pack's `Server/Item/Items/` directory.

### Item Categories
To organize your items, you can create custom categories.
**Path:** `Server/Item/Category/`

Example `my_category.json`:
```json
{
  "name": "my_category",
  "text": "My Custom Category",
  "icon": "my_icon"
}
```

## Adding Blocks
Blocks are defined similarly to items but include specific behaviors and properties.
**Path:** `Server/Block/`

### Block State Changing
Block states allow blocks to change appearance or behavior when interacted with (e.g., opening a door, turning on a light).

**Interaction Example:**
To make a block change state on right-click:
```json
"interactions": [
  {
    "use": "RightClick",
    "type": "ChangeState",
    "changes": {
      "open": "closed",
      "closed": "open"
    }
  }
]
```

This configuration maps the current state to the next state, enabling simple toggles.
