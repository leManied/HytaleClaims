# EasyClaims

> **Built for the European Hytale survival server at `play.hyfyve.net`**

Protect your builds on Hytale servers! Claim land, see it on your map, and share with friends.

## Quick Start

1. **Install**: Download the [latest release](../../releases/latest) and drop the JAR into your server's `mods/` folder
2. **Restart** your server
3. **Claim land**: Stand where you want to protect and type `/claim claim`
4. **See your claims**: Open your map (M) - claimed chunks show in color!

That's it! Your builds are now protected.

---

## Features

- **Visual Map Integration** - Claimed chunks appear colored on the world map
- **In-Game GUI** - Manage claims and trusted players through easy-to-use interfaces
- **Playtime Rewards** - Play longer, claim more land
- **Share With Friends** - Trust players with different permission levels
- **Full Protection** - Blocks breaking, placing, and interactions from strangers
- **Anti-Griefing Buffer** - 2-chunk buffer zone prevents others from claiming too close to you

---

## Commands

All commands use `/claim`.

### GUI Commands

| Command | What it does |
|---------|--------------|
| `/claim gui` | Open the claim map GUI (see and manage claims visually) |
| `/claim settings` | Open settings GUI to manage trusted players |

### Essential Commands

| Command | What it does |
|---------|--------------|
| `/claim claim` | Claim the chunk you're standing in |
| `/claim unclaim` | Remove your claim on current chunk |
| `/claim list` | List all your claimed chunks |
| `/claim help` | Show all available commands |

### Sharing With Friends

| Command | What it does |
|---------|--------------|
| `/claim trust PlayerName` | Give full access to a player |
| `/claim trust PlayerName use` | Let them use doors/buttons only |
| `/claim trust PlayerName container` | Let them open chests too |
| `/claim untrust PlayerName` | Remove a player's access |
| `/claim trustlist` | See who you've trusted |

**Tip:** Use `/claim settings` for an easier way to manage trusted players with a GUI!

### Other Commands

| Command | What it does |
|---------|--------------|
| `/claim unclaimall` | Remove ALL your claims (careful!) |
| `/claim playtime` | Check your playtime and claim slots |

### Admin Commands

| Command | What it does |
|---------|--------------|
| `/claim admin gui` | Open claim manager GUI (admin mode) |
| `/claim admin config` | Show current settings |
| `/claim admin set <key> <value>` | Change a setting (saves immediately) |
| `/claim admin reload` | Reload config from file |
| `/claim admin unclaim` | Remove claim at your location (any owner) |
| `/claim admin unclaim <player>` | Remove ALL claims from a player |

**Settings you can change:**
```
/claim admin set starting 6      # Starting claim slots for new players
/claim admin set perhour 3       # Extra claims earned per hour
/claim admin set max 100         # Maximum claims any player can have
/claim admin set buffer 2        # Buffer zone in chunks (0 = disabled)
```

---

## Trust Levels Explained

When you trust someone, you can choose how much access they get:

| Level | Command Example | What They Can Do |
|-------|-----------------|------------------|
| **use** | `/claim trust Steve use` | Open doors, press buttons, flip levers |
| **container** | `/claim trust Steve container` | Above + open chests, barrels |
| **workstation** | `/claim trust Steve workstation` | Above + use furnaces, crafting tables |
| **build** | `/claim trust Steve build` | Full access - can break and place blocks |

**Note:** If you don't specify a level, players get full `build` access.

**Tip:** Use `/claim trust PlayerName use` for visitors who just need to get through doors!

---

## How Claims Work

- Each claim protects a **32x32 block area** (one chunk)
- Claims extend from bedrock to sky - full vertical protection
- You start with **4 claim slots** and earn more by playing
- Open your **world map (M)** to see claims highlighted in color
- Your claims show in your unique color, others show in theirs
- **Buffer zone**: Other players can't claim within 2 chunks of your claims (prevents griefing)

### Earning More Claims

The longer you play, the more land you can claim:

| Playtime | Total Claim Slots |
|----------|-------------------|
| New player | 4 chunks |
| 1 hour | 6 chunks |
| 5 hours | 14 chunks |
| 10 hours | 24 chunks |

Use `/claim playtime` to check your progress!

---

## Installation

### For Server Owners

1. Download the latest JAR from [Releases](../../releases/latest)
2. Place it in your server's `mods/` folder
3. Restart the server

### Setting Up Permissions

Grant these permissions to let players use the plugin:

```
perm group add Adventure easyclaims.use
perm group add admin easyclaims.admin
```

The `easyclaims.use` permission grants access to all player commands (claim, unclaim, trust, etc.).
The `easyclaims.admin` permission grants access to `/easyclaims admin` commands (config, set, reload).

---

## Troubleshooting

### "You don't have permission"
Ask your server admin to grant you the `easyclaims.use` permission.

### Claims not showing on map?
Try closing and reopening your map, or reconnect to the server.

### Can't claim?
- Check if you have available slots: `/claim playtime`
- Make sure the chunk isn't already claimed by someone else
- You might be too close to another player's claim (2-chunk buffer zone)

---

## License

MIT - Use it however you like!
