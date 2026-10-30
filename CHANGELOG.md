# 📝 Changelog

Studio: ORIKAMI.

## 1.0.0 ⭐

- Local multiplayer: every connected controller becomes a player, up to 4. In the menu, players can swap places.
- New touch controller, half Switch, half GameCube. It adapts to the screen size, and all its buttons are clearly visible.
- "Settings" menu on the left, in Masu's colors. A handle and a bubble open it.
- Cast and external display: a TV (Smart View, Miracast) or a connected screen receives the game image, and the phone becomes the controller.
- Samsung DeX: the game runs in a window on the monitor, and the window follows its size.
- Much faster startup: already prepared shaders are reused from one launch to the next.
- Clean black screen until the title, no flicker.
- Launch through Masu: the game uses its own copy if Masu's copy is not version 1.0.0.

## 0.99

- No more ghost image of the village plaza before the title screen.
- First "Settings" menu: game, image, touch controller, controllers, saves.
- Settings changed in the game come back into Masu.

## 0.98

- Intro: straight back to the title screen, no more unskippable intro ending.
- Touch controller: labels, D-pad and − and + buttons better placed.

## 0.97 ⭐

- Local multiplayer with physical controllers, players 1 to 4.
- New GameCube-colored touch controller, with a camera stick.
- Touch controller settings (size, opacity, vibration) chosen in Masu.
- The game can be launched directly from Masu.
- Marina water stripes reduced (trial).

## 0.96

- Bluetooth sound: no more choppy or slowed-down audio.

## 0.95 ⭐

- Characters' dialogue bubbles finally displayed (Toad, Koopa…).

## 0.94

- Shadows: shadow draws are no longer lost while shaders are being prepared.

## 0.93

- First fixes for dialogue bubbles.

## 0.92

- Numbered shared logs.

## 0.91

- Diagnostic tools for bubbles and loading.

## 0.90

- Distant board spaces displayed.

## 0.89

- Diagnostic tools for the board spaces.

## 0.88

- Large 3D models visible again (regression from 0.87).
- More board spaces visible in wide view.

## 0.87

- Trial for the board spaces (removed in 0.88).

## 0.86

- Diagnostic tools for the board spaces.

## 0.85

- End-of-game text bubbles displayed.

## 0.84

- Fix for a crash during games.

## 0.83 ⭐

- Less heat and smoother play: far fewer data copies on every frame.

## 0.82

- Fixes for hangs and graphics crashes on the board.

## 0.81

- End of the game being closed for lack of memory after a few minutes.

## 0.80

- Characters and spaces correct in all memory modes.
- More complete log in case of graphics trouble.

## 0.79

- Fixes the 0.78 regression (frozen characters, missing spaces).

## 0.78

- New memory mode for fewer copies. It caused a regression, fixed in 0.79: prefer 0.79.

## 0.77 ⭐

- Board spaces: indirect draws (records written by the GPU) are now executed.

## 0.76

- Black-background transitions at scene changes fixed: a short stutter instead, while shaders compile.

## 0.75

- Crash when starting a mini-game fixed (missing basic functions: atof, qsort, bsearch).

## 0.74 ⭐

- Flattened characters fixed (bone matrices reading).
- End of a false "unknown vertex format" check.

## 0.73

- Richer LOG (attributes and vertex streams of each draw).

## 0.72

- Memory shared with the GPU: a word rewritten by the game is no longer overwritten by an old read-back.
- Richer LOG.

## 0.71

- No more crash when the app goes to the background.
- Richer LOG.

## 0.70 ⭐

- Characters, NPCs and Bowser in color (shader cache completed; the old cache is replaced automatically).

## 0.69

- Freeze when loading the board fixed: rendering no longer waits for prepared shaders.
- Last untranslated shader fixed (LEA).

## 0.68

- Hang when starting a game fixed.
- ATOM instruction of the skinning shaders; more complete hang report.

## 0.67

- Colors fixed on the plaza, the island map and the mode selection (3D color tables).

## 0.66

- White screen when loading a save fixed (background compilation).
- VOTE instruction translated; hang report in the log.

## 0.65

- Characters are finally computed (compute vertex shaders run in a dedicated pass).
- Overlapping shared memory areas merged.

## 0.64 ⭐

- Characters animated by the graphics card are finally drawn (transform feedback).
- Full debug image in the log.

## 0.63

- GPU-animated characters and objects are drawn with their real vertices (they were stretched into triangles or missing).

## 0.62

- Up to 64 textures per shader (characters and system rendering).
- Indexed attributes translated.
- Log: new checks and a vertex statistics line every 30 s.

## 0.61

- Flattened or flickering characters: draw lists are now stored outside the game's memory.
- Draws of cached programs shown again (missing since 0.58).
- Wrong colors: interpolated inputs are now handled correctly on screen.
- Graphics capabilities report at startup; pipeline cache protected when storage is full.

## 0.59

The graphics driver is shown in game.

- The HUD shows on a second line the graphics driver in use and its version (system driver or installed Turnip, Vulkan version).

## 0.58

Checks in the logs and one crash fewer.

- The log now contains `[check]` lines (rendering anomalies) and a `[health]` line every 30 seconds (memory, threads, render queue).
- The crash report is more complete (all registers, rendering context, wider stack).
- Crash on a texture without memory after several board changes fixed.

## 0.57

End of a crash when loading boards.

- Crash when loading a board (after Chance Time) fixed: graphics program copies are no longer rewritten beyond 2048.
- The crash e-mail no longer opens over the game at launch: the LOG button opens it, the next press gives the log.

## 0.56

Fixes for the ground, characters and text, plus a mini-game that no longer crashes.

- Shaders only request the `shadow_lod` GLSL extension when needed (the ground, characters and text had disappeared).
- Mini-game mg0107: 19 libc++ functions from the modules added, crash fixed.
- UTF text conversions aligned with the SDK (player names).

## 0.55

Lighting shader textures, player names and crash e-mail.

- Per-light lighting shader textures (7,771 stages out of 7,802 translated).
- Player names displayed.
- After a crash, a ready-to-send e-mail with the report and log attached.
- The report gives the exit reason reported by Android.

## 0.52 ⭐

Fast loading and a new touch controller.

- Game memory management in O(log n): loading went from 35 s to 46 ms.
- New party-themed touch controller, same sizes on both screens of the foldable.
- x2 button to speed up the game; discreet frames-per-second counter with temperatures.

## 0.49 ⭐

3D scenery appears.

- Cached command lists are no longer overwritten (0.48).
- The scenery's vertex shaders finally write their position (0.49).

## 0.33 ⭐

Sound arrives.

- Audio: voice mixing and playback through AAudio.
- LOG button: runtime log written to disk, shareable.
- Several more shaders translated (compute, bindless textures).

## 0.22

Character selection reached.

- Default user profile so the game loads its save.
- Video player now fails cleanly when no video is decoded.
- Intro subtitles removed from the title screen.
- Touch controller shown on top of the game.

## 0.15 ⭐

Title screen and main menu.

- The game starts, plays through the intro and reaches the title screen.
- After a crash, the report of the previous launch is written to `rapport.txt` and offered for sharing.
- Physical controllers 1 to 4 recognized.
