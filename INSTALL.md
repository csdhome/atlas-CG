# Consortium Atlas File

The atlas contains all celestial body data for The Consortium MyDU server — planet positions, gravity, radius, atmosphere, ore distributions, and more. It is required by both ArchHUD and SagaHUD.

## Installation

Copy the atlas file to your DU autoconf directory:

```
atlas.lua  -->  <DU Install>/Game/data/lua/autoconf/custom/atlas.lua
```

### Default Install Path

```
C:\ProgramData\Dual Universe\Game\data\lua\autoconf\custom\
```

## Contents

The atlas includes all Consortium celestial bodies:

**Standard Planets & Moons:**
Madis (+ 3 moons), Alioth (+ 2 moons), Sanctuary, Haven, Thades (+ 2 moons + 34 asteroids), Talemai (+ 3 moons), Sicari, Sinnen (+ 1 moon), Teoma, Jago

**Prime Planets & Moons:**
Feli Prime (+ 1 moon), Alioth Prime (+ 2 moons), Lacobus Prime (+ 3 moons), Ion Prime (+ 2 moons), Jago Prime, Madis Prime (+ 3 moons), Sicari Prime, Sinnen Prime (+ 1 moon), Symeon Prime, Talemai Prime (+ 3 moons), Teoma Prime, Thades Prime (+ 2 moons)

**Custom Bodies:**
Consortium Home World, Terraforming Debris Asteroid 00

**CG Meganode Asteroids (40 total):**
Named after chemical elements (Al, C, Fe, Si, Ca, Cr, Cu, Na, Li, Ni, Ag, S, Co, F, Au, Sc, Mn, Nb, Ti, V) — each with an "_A" variant

## Data Structure

Each body entry contains:
- `id` — unique identifier
- `name` — display name (English, French, German)
- `type` — Planet, Moon, or Asteroid
- `center` — world coordinates {x, y, z}
- `radius` — body radius in meters
- `gravity` — surface gravity in m/s^2
- `GM` — gravitational parameter
- `atmosphereThickness` — atmosphere height in meters (0 for no atmosphere)
- `atmosphereRadius` — total radius including atmosphere
- `hasAtmosphere` — boolean
- `isSanctuary` / `isInSafeZone` — zone flags
- `ores` — list of ore type IDs available
- `territories` — number of hex territories

## Notes

- This file is loaded by HUDs via `require("autoconf/custom/atlas")` or `require("atlas")`
- Modified by Eggonomicon and Darc of CG for The Consortium server
