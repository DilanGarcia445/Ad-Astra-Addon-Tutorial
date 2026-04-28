# 🖼️ Textures Guide — What PNGs you need and where they go

All PNGs live inside the **resource pack**, under:

```
resourcepack/
└── assets/
    └── custommod/
        └── textures/
            └── sky/
                ├── custom_galaxy.png      ← 1 file for the galaxy
                └── solara_prime.png       ← 1 file for the planet
```

That's it — **just 2 PNG files** for this single-planet example.

---

## What each PNG is and where it appears

### 1. `custom_galaxy.png`
**Path:** `assets/custommod/textures/sky/custom_galaxy.png`

**Where it appears:**
- On the **Galaxy Selection screen** (first screen when you open a rocket's GUI).
  It is shown as the background/icon for "Custom Galaxy".

**What it should look like:**
- A galaxy image — a spiral or nebula image works great.
- Recommended size: **256×256 pixels** (or any power of 2, up to 512×512).
- Format: PNG with or without transparency.

**Quick placeholder:** Any colorful PNG image works. You can use a plain colored square to test.

---

### 2. `solara_prime.png`
**Path:** `assets/custommod/textures/sky/solara_prime.png`

**Where it appears in TWO places:**

#### A) Planet Selection Screen (the "rings" menu)
Referenced in `planet_rings/solara/solara_prime.json`:
```json
"texture": "custommod:textures/sky/solara_prime.png"
```
This is the **icon/thumbnail of your planet** shown in the solar system orbit diagram where planets spin around the sun.

#### B) In-orbit sky (what you see when flying in orbit above the planet)
Referenced in `sky_renderers/solara_prime_orbit.json`:
```json
"texture": "custommod:textures/sky/solara_prime.png"
```
This is the **big planet sphere** you see looking "down" from orbit space.

**What it should look like:**
- A round planet image, ideally on a **transparent (black) background**.
- Recommended size: **256×256 pixels**.
- For a planet that looks round in space: make a sphere/circle texture with the planet surface visible inside it and a transparent/black border around it.

**Quick placeholder:** A plain colored circle PNG on a black/transparent background works fine for testing.

---

## How to make quick placeholder PNGs (no art skills needed)

You can use **any image editor** (Paint, GIMP, Photoshop, or even online tools like https://www.photopea.com/):

1. Create a new **256×256** image
2. Fill it with any color (e.g. orange for a hot planet)
3. Save as `.png`
4. Rename the file and put it in the right folder

That's enough to test in-game — you can replace with proper art later.

---

## Final resource pack folder structure

```
resourcepack/
├── pack.mcmeta
└── assets/
    └── custommod/
        ├── lang/
        │   └── en_us.json
        ├── textures/
        │   └── sky/
        │       ├── custom_galaxy.png       ← YOU ADD THIS
        │       └── solara_prime.png        ← YOU ADD THIS
        └── planet_resources/
            ├── galaxy/
            │   └── custom_galaxy.json
            ├── solar_systems/
            │   └── solara.json
            ├── planet_rings/
            │   └── solara/
            │       └── solara_prime.json
            └── sky_renderers/
                └── solara_prime_orbit.json
```

---

## Summary table

| PNG file | Size | Where it shows |
|---|---|---|
| `textures/sky/custom_galaxy.png` | 256×256 | Galaxy selection menu background |
| `textures/sky/solara_prime.png` | 256×256 | Planet ring icon + in-orbit sky view |

> ⚠️ If you forget to add a PNG, the game won't crash but you'll see a **magenta/purple "missing texture" square** in those spots. The planet will still be accessible.
