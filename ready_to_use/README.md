# ✅ Ready To Use — Copy & Paste into your modpack

This folder contains a complete, minimal single-planet example (**Solara Prime**) ready to drop into your modpack.

---

## 📁 What's inside

```
ready_to_use/
├── datapack/           ← Put this in your world's datapacks folder
│   ├── pack.mcmeta
│   └── data/
│       └── custommod/
│           ├── dimension/
│           │   ├── solara_prime.json
│           │   └── solara_prime_orbit.json
│           ├── dimension_type/
│           │   └── solara_prime.json
│           └── planet_data/
│               └── planets/
│                   └── solara_prime.json
│
├── resourcepack/       ← Put this in your resourcepacks folder
│   ├── pack.mcmeta
│   └── assets/
│       └── custommod/
│           ├── lang/
│           │   └── en_us.json
│           ├── textures/
│           │   └── sky/
│           │       ├── custom_galaxy.png   ← YOU MUST ADD THIS
│           │       └── solara_prime.png    ← YOU MUST ADD THIS
│           └── planet_resources/
│               ├── galaxy/
│               │   └── custom_galaxy.json
│               ├── solar_systems/
│               │   └── solara.json
│               ├── planet_rings/
│               │   └── solara/
│               │       └── solara_prime.json
│               └── sky_renderers/
│                   └── solara_prime_orbit.json
│
└── TEXTURES_GUIDE.md   ← Read this for the PNG files
```

---

## 🚀 Step-by-step installation

### Step 1 — Add the datapack

1. Launch your modpack and **create or open a world**
2. In the world's folder (`.minecraft/saves/<YourWorld>/`), find the **`datapacks`** subfolder
3. Copy the entire **`datapack/`** folder from here into it:
   ```
   .minecraft/saves/YourWorld/datapacks/datapack/
   ```
4. In-game, run: `/reload`

### Step 2 — Add the 2 PNG textures

Before the resource pack will look right, you need to add 2 PNG images.
**Read `TEXTURES_GUIDE.md`** for exactly what they should look like and where they go.

Put your PNGs here (inside the `resourcepack/` folder):
```
resourcepack/assets/custommod/textures/sky/custom_galaxy.png
resourcepack/assets/custommod/textures/sky/solara_prime.png
```

A plain 256×256 colored PNG is fine for testing — you can make proper art later.

### Step 3 — Enable the resource pack

1. Copy the **`resourcepack/`** folder to your `.minecraft/resourcepacks/` folder:
   ```
   .minecraft/resourcepacks/resourcepack/
   ```
2. In-game go to **Options → Resource Packs** and move **"resourcepack"** to the right (active) side
3. Click **Done**

### Step 4 — Test it!

1. Right-click any **Tier 1 rocket** to open the Planet Selection GUI
2. You should see a new **"Custom Galaxy"** button
3. Click it → **"Solara System"** → **"Solara Prime"**
4. Launch! 🚀

---

## ⚠️ Important notes

| Thing | Value |
|---|---|
| Mod ID used | `custommod` |
| Planet name | `solara_prime` |
| Rocket tier needed | Tier 1 |
| Has oxygen? | ❌ No (bring a space suit) |
| Has atmosphere? | ❌ No |
| Gravity | 4.5 |

If you want to rename everything (change `custommod` to your own mod ID), do a **find & replace** of `custommod` across all JSON files.

---

## 📖 Pack format numbers by Minecraft version

If your modpack uses a different MC version, update the `"pack_format"` in both `pack.mcmeta` files:

| Minecraft version | pack_format |
|---|---|
| 1.19.4 | 12 |
| 1.20.1 | 15 |
| 1.20.4 | 22 |
| 1.20.6 | 32 |
| 1.21.x | 34+ |
