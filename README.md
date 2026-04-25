Showcase: https://youtu.be/WsySwFuiiTg


⚗️ SwitchDrugCreator
Advanced in‑game drug zone creator for FiveM (ESX/QBCore/Standalone) using ox_inventory + ox_lib


SwitchDrugCreator is a lightweight, admin‑controlled drug zone system for FiveM servers.
Create, edit, delete, and harvest drug zones entirely in‑game, with glow rings, animations, required items, and full database persistence.

Designed for ESX, QBCore, and standalone servers that use ox_inventory.

✨ Features
🧪 Create drug zones in‑game using an admin menu

🎨 Glow ring visual indicator (customizable colors)

🎞 Custom animations for harvesting

🎒 Supports required items (up to 3 per zone)

🎲 Fixed or random harvest amounts

⏳ Adjustable harvest time

📍 Teleport to zone (admin only)

💾 Automatic SQL table creation & schema patching

🔄 Full client/server zone syncing

🧹 No blips — clean map

🔐 ACE permission‑based admin access

🧱 Framework‑agnostic (ESX/QBCore/Standalone)

📦 Dependencies
Your server must have:

ox_inventory (github.com in Bing)

ox_lib (github.com in Bing)

oxmysql (github.com in Bing)

Works with:

ESX

QBCore

Standalone

As long as ox_inventory is installed.

📁 Installation
1️⃣ Drag & Drop
Place the folder into your server’s resources/ directory:

Code
resources/
└── switchdrugcreator/
    ├── client.lua
    ├── server.lua
    ├── fxmanifest.lua
    └── README.md
2️⃣ Add to server.cfg
Code
ensure switchdrugcreator
3️⃣ Add ACE Permission
Only admins with this permission can open the menu:

Code
add_ace group.admin drugcreator.admin allow
Or assign it to a custom group:

Code
add_ace group.superadmin drugcreator.admin allow
4️⃣ Database Setup
No SQL import required.

On first start, the script will:

Create the drug_zones table if missing

Remove old blip columns

Load all zones

Sync to all clients

Console output will show:

Code
[DrugCreator] Checking database schema...
[DrugCreator] Database schema cleaned (blip fields removed).
[DrugCreator] Loaded X zones.
🎮 Usage
Open Admin Menu
Admins can open the menu via:

Command:

Code
/drugcreator
Keybind:
F6 (can be changed in FiveM keybind settings)

Creating a Zone
Inside the menu:

Create New Zone

Enter:

Zone label

Item name (ox_inventory item)

Fixed or random amount

Radius

Harvest time

Glow ring color

Animation preset

Required items (optional)

Confirm — the zone is saved to the database instantly.

Managing Zones
Inside Manage Existing Zones, admins can:

📍 Teleport to zone

✏️ Edit zone

🗑 Delete zone

All changes sync instantly to all players.

Harvesting
Players walk into the glow ring and press E.

If required items are missing, they receive an error.
If successful, they receive the configured item amount.

Example
Code
[ID 3] Weed Field | radius=2.00 | time=3 | coords=123.45 456.78 78.90

🛠 Developer Notes
✔ Works on ESX

✔ Works on QBCore

✔ Works standalone

✔ No framework‑specific inventory calls

✔ Fully ox_inventory‑based


📜 License
MIT License — free to use.

❤️ Credits
Created by Switch
