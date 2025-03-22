# Chronicles of Bebanburg
### Stage: Early-Alpha | BuildNum#: 0.18.1 | Ver: 0.1.3.0
> A Heavily Modified Port of the **RiskRP** Discord Bot (Originally Python) to **Pure HTML** & JavaScript

![Chronicles of Bebanburg Banner](https://i.ibb.co/KnkmF0Q/image-2025-03-20-073410315.png)

**Author / Developer:** [gamedev44 (Asterisk)](https://github.com/gamedev44)  
**Support Our Work:** [Patreon - PGD Indue Unlimited](https://www.patreon.com/c/iu_pgd/membership)  
**License:** Semi-Open Source - [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) (Private Repo)

---

## Table of Contents
- [Introduction](#introduction)
- [Directory Structure](#directory-structure)
- [Key HTML Files](#key-html-files)
- [Features](#features)
- [Gameplay & Mechanics](#gameplay--mechanics)
- [Technical Info & Setup](#technical-info--setup)
- [Credits & References](#credits--references)
- [License & Support](#license--support)

---

## Introduction
**Chronicles of Bebanburg** is a **2D Browser-Based Top-Down** / **Turn-Based Combat** / **Action RPG** reminiscent of classic titles like **Pokémon**—but set in a **RiskRP** medieval-fantasy world. Originally developed in Python for the **RiskRP** Discord Bot, this project has been **heavily modified and ported** into **pure HTML, CSS, and JavaScript** (no libraries besides Google Fonts). It includes:

- **Co-op couch** or single-player modes
- A **race system** (Human, Orc, Elf, Dragonkin, Mage, etc.)
- **Gold and shop** mechanics
- **Fast-travel map** and land-ruling systems
- **Neutral, hostile, and passive zones** with triggers
- **Advanced inventory** and leveling
- Future **multiplayer** with Socket.io & NeonDB (planned)

---

## Directory Structure
Below is the core folder layout (as shown in the provided screenshot). Each `.html` is self-contained (inline CSS/JS):

```
COB/
├─ Assets/
│   └─ Images/
│       └─ races/
│           ├─ dragon.png
│           ├─ elf.png
│           ├─ human.png
│           └─ orc.png
├─ Menus/
│   ├─ mainmenu.html
│   └─ settings.html
├─ Modules/
│   ├─ TopDownRpgBaseLevel.html
│   └─ TurnBasedBattle.html
├─ Components/
│   └─ map.html
├─ Worlds/
│   ├─ world1/
│   │   ├─ level1.html
│   │   ├─ level2.html
│   │   └─ BossLevel.html
│   └─ world2/
├─ index.html
└─ .gitattributes
```

- **Assets/Images/races/**: Contains character race images (human, orc, elf, etc.)  
- **Menus/**: Main menu and settings HTML files  
- **Modules/**: Core modules like top-down exploration and turn-based battle  
- **Components/**: Reusable or special-purpose screens (like the fast-travel map)  
- **Worlds/**: Each “world” folder can hold multiple levels or zones  
- **index.html**: Potential entry point or overall container  

---

## Key HTML Files
- **`mainmenu.html`** — The game’s main menu, handling mode selection (solo, co-op, online) and race choices.  
- **`TopDownRpgBaseLevel.html`** — The top-down exploration and movement screen. Contains triggers, item pickups, and door transfers.  
- **`TurnBasedBattle.html`** — The separate battle interface for turn-based combat (similar to classic JRPG encounters).  
- **`map.html`** — The fast-travel or overworld map, letting you jump between different worlds or zones.  
- **`level1.html`, `level2.html`, `BossLevel.html`** — Sample levels or zones with custom triggers, enemies, and door exits.

---

## Features
1. **Top-Down & Turn-Based Hybrid**  
   - Roam a 2D overworld in real-time  
   - Transition seamlessly into turn-based battles (like classic Pokémon or Final Fantasy)  
   - **Co-op couch** or single-player modes

2. **Rich Medieval-Fantasy Setting**  
   - **Races**: Human, Orc, Elf, Dragonkin, Mage, etc.  
   - **Neutral, Hostile, and Passive** zones with dynamic triggers  
   - **Land-ruling** system for controlling territory

3. **Dynamic Inventory & Shop System**  
   - Collect gold, buy gear from shops  
   - Use potions, weapons, and special items  
   - Gains from battles feed directly into your inventory

4. **Fast Travel & World Map**  
   - **`map.html`** shows a big overworld with clickable fast-travel points  
   - Multiple worlds: e.g., `world1/level1.html`, `world1/level2.html`, etc.

5. **Fully Self-Contained HTML**  
   - All `.html` files include their own inline CSS & JS  
   - Minimal external resources: only Google Fonts CDN  
   - No frameworks or libraries needed

6. **Upcoming Multiplayer**  
   - Plan to integrate **Socket.io** & **NeonDB** for real-time co-op or PvP  
   - More advanced sync for quest sharing, party formation, or territory battles

---

## Gameplay & Mechanics
1. **Overworld Exploration**  
   - Move your character in real-time top-down style  
   - Interact with triggers (doors, items, NPC dialogues)  
   - Races affect your stats, HP, and special abilities

2. **Turn-Based Combat**  
   - On trigger overlap, switch to **`TurnBasedBattle.html`**  
   - Attack, defend, use items—like a classic JRPG  
   - Victory yields XP, gold, or items; losing might cost gold or reset progress

3. **Map & Travel**  
   - Use **`map.html`** to jump quickly between discovered zones  
   - Some areas require key items or certain XP levels to unlock

4. **Multiplayer (Planned)**  
   - Real-time synchronization with **Socket.io**  
   - Possibly “couch co-op” using local inputs or separate browsers  
   - Potential online parties or PvP battles

---

## Technical Info & Setup
- **Pure HTML, CSS, JavaScript**  
  - Each file is a self-contained module or screen  
  - No bundlers or external build steps required

- **Local Testing**  
  1. Clone or download the repository  
  2. Open `index.html` or any `.html` file in a browser  
  3. Ensure local JS is allowed (some browsers block file-based scripts by default)

- **Future Multiplayer**  
  - **Socket.io** & **NeonDB** integration planned  
  - Possibly a small Node.js server for real-time events

---

## Credits & References
- **Heavily Modified from [RiskRP Bot](https://gist.github.com/gamedev44/14b0d3d87e0999f13a1a9de91359ed06)**  
  - Original advanced roleplay system in pure Python  
  - Adapted to a browser-based environment here
- **Author / Developer**: [**gamedev44 (Asterisk)**](https://github.com/gamedev44)  
- **Patreon**: [**Support Our Work**](https://www.patreon.com/c/iu_pgd/membership)  
- **Inspiration**:  
  - Classic 2D JRPGs (Pokémon, Final Fantasy)  
  - RiskRP’s medieval fantasy theming

---

## License & Support
- **License**: Semi-Open Source under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).  
- **Repository**: Private collaboration only (invite-based).  
- **Support**:  
  - [Patreon - PGD Indue Unlimited](https://www.patreon.com/c/iu_pgd/membership)  
  - [GitHub (gamedev44)](https://github.com/gamedev44)

> **Disclaimer**: All artwork and images are placeholders or user-provided assets.  
> This game is purely for demonstration and educational use, showcasing how a Python-based Discord Bot can be ported to a pure HTML/JS environment.

**Enjoy the Chronicles of Bebanburg!** Explore, battle, and shape this medieval fantasy world right in your browser. Good luck!