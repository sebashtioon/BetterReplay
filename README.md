# BetterReplay

Watch back your best scores (better)!

## FAQ

- How do I record a replay?
  - For now, the only way to record replays is with [BeatLeader](https://github.com/BeatLeader/beatleader-qmod/releases) or [ScoreSaber](https://scoresaber.com/quest). All you have to do is play any level with either installed. Replay will add a replay button next to the play button for levels that have a replay.
  - Replays from the old 1.17.1 replay mod are available to view, but cannot be recorded. Recording them will never be added because their format is much worse for viewing and rendering.

- What is the purpose of the Render Video feature?
  - The Render Video feature allows Quest gameplay to look identical to (or even better than) PC recordings. You can set FOV, enable mirrors, bloom, etc all running smoothly at the resolution and framerate you want.

- How can I know how close my render is to finishing?
  - During a render, information about the level and the rendering progress will be displayed on the screen of the Quest, including a timer showing how much of the level has been rendered so far, and the total length of the level.

- How can I exit a render before the level ends?
  - Enable "Allow Pauses" in the rendering section of the mod settings before starting the render and exit through the pause menu.
  - If you started the render without that setting enabled, you can exit the game through the Quest menu, but the output will not be saved.

# Credits

[Metalit](https://github.com/Metalit) for making the original Replay mod

[NSGolova](https://github.com/NSGolova) for making the BeatLeader format and recorder, buggy as it may be

[Fern](https://github.com/Fernthedev) for the original version of Hollywood, the renderer

[Sc2ad](https://github.com/Sc2ad) and the rest of the Quest modding people

## Building

- 1. Make your changes in the source files.

- 2. Open a terminal in the project root.

- 3. Rebuild the .so library:
pwsh ./scripts/build.ps1

- 4. Update the .qmod file (if you changed metadata like version, name, or cover image):
pwsh ./scripts/createqmod.ps1

- 5. Replace the old mod in your Quest/PC mods folder with the newly generated .qmod file.

- 6. Launch the game and test your changes.

Note: You only need to re-run CMake or change build configurations if you add new source files or alter build settings. For most tweaks, steps 3–5 are enough.

