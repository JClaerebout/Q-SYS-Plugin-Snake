# Snake 1.0.0

Classic Snake for Q-SYS on a 24-by-16 board, rendered as dynamic SVG. [Snake_1.0.0.qplug](Snake_1.0.0.qplug) contains the game and generates all artwork; no separate image files or external services are needed.

## Install and play

1. Double-click `Snake_1.0.0.qplug`. QSysPluginHelper will prompt you to install the plugin.
2. Add **Games > Snake** to a design and start emulation or run the design on a Core.
3. Open the component and press **Start / Restart**. Use **Up**, **Down**, **Left**, and **Right** to steer toward the red food.

Eating food grows the snake and adds 10 points. Hitting a wall or your body ends the game. Fill the board to win. Immediate direction reversals are ignored, and up to two turns can be queued.

## Controls

- `Start` starts a new game or restarts the current one, resetting the score.
- `Up`, `Down`, `Left`, and `Right` steer the snake.
- `Pause` toggles pause and resume.
- `Speed` ranges from 1 (slowest) to 10 (fastest), with a default of 4. You can change it during play.
- `Score`, `HighScore`, and `Status` show the current score, best score this session, and game state. The best score survives a game restart but resets when the runtime restarts.
- `Display` shows the board and score.

## UCI integration

Copy `Display` and the game controls from the component into a UCI. Keep the display at its original 610:420 aspect ratio. Direction and start controls expose input pins; `Pause` and `Speed` expose input and output pins. Score and status text expose output pins. The display is UI-only.

## License

[MIT](LICENSE). Copyright (c) 2026 Jens Claerebout.
