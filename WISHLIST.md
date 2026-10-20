# Wishlist

Future features planned for this recomp. These are loose goals to work toward
as the project progresses — not committed timelines.

To add a new item, copy the template at the bottom and fill it in.

---

## 1. Adaptive Widescreen (16:9 / 21:9)
- **Status:** Planned
- **Description:** Instead of merely stretching the native 240×160 resolution,
  extend camera boundaries, realign HUDs, and smart-render assets so backgrounds
  naturally fill modern displays without graphical tearing, borders, or culling.

## 2. Uncapped Frame Rates
- **Status:** Planned
- **Description:** GBA games natively target ~60 FPS. Unlock the frame rate to
  take advantage of high-refresh-rate monitors without speeding up the internal
  engine logic (decouple render rate from game tick).

## 3. Skip Tutorial & Opening Cutscenes
- **Status:** Planned
- **Description:** Add options to skip the tutorial and skip the opening cutscene
  for each character, so repeat playthroughs start faster.

## 4. Resolution Upscaling & HD Texture Dumping
- **Status:** Planned
- **Description:** Add options for upscaling the render resolution and dumping
  HD textures/sprites, allowing higher-fidelity visuals on modern displays.

## 5. Fast Forward Without Audio Pitch Change
- **Status:** Planned
- **Description:** Add fast-forward that speeds up gameplay without changing
  music/sound speed (or with pitch correction), so audio doesn't become
  chipmunked during fast-forward.
- **Notes (2026-10-20):** User confirms the current build has NO sound at all
  during fast-forward. Target state: fast-forward active with audio playing
  unaffected (normal speed/pitch).

## 6. PS5 Controller Fullscreen Toggle
- **Status:** Done (2026-10-20)
- **Description:** Allow mapping a pad button (e.g., PS5 controller touchpad
  or other button) to toggle fullscreen, so you don't need the keyboard.
- **Notes:** Implemented as a DualSense/DualShock touchpad click handler in
  the host window event pump (`SDL_CONTROLLER_BUTTON_TOUCHPAD` →
  `toggle_fullscreen`, same flag as the keyboard hotkey). Suppressed while
  the runtime UI is open. Shipped in the launcher build of 2026-10-20.

## 7. Improved Text Clarity & Resolution
- **Status:** Planned
- **Description:** Improve text rendering clarity and resolution — sharper fonts,
  better scaling, so dialogue and UI text is crisp on high-DPI displays.

## 8. Save States via Controller/Keyboard
- **Status:** Planned
- **Description:** Add save state / load state triggers mappable to keyboard
  or controller buttons (e.g., L3 to load state, R3 to save state) for
  quick save/load without opening menus.

## 9. Quit Game Option
- **Status:** Planned
- **Description:** Add a quit-game option in the main menu / in-game options,
  or a dedicated keybind, so you can exit cleanly without Alt+F4.

## 10. Controller Remapping
- **Status:** Planned
- **Description:** Let the player remap controller buttons in-game (the way
  keybinds.ini already allows keyboard remapping), so any pad layout —
  PS5, Xbox, or generic — can be customized and saved.

## 11. Help Menu (Build Version + GitHub Issue Tickets)
- **Status:** Planned — HOLD: do not implement until there is a proper
  playable alpha without graphical glitches (user directive, 2026-10-20).
- **Description:** Add a Help selection to the menu bar with two options:
  (a) **About / Version** — shows the current build version (e.g. v001,
  numbering starts with the first playable alpha, per the user), and
  (b) **Report Issue** — lets the user open a GitHub issue ticket directly
  against the project repo from inside the game.

---

## Template (copy for new items)

```markdown
## N. Feature Title
- **Status:** Planned
- **Description:** What it does and why.
```
