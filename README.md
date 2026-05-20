# SF3 Input Display

A browser-based input display for Street Fighter III 3rd Strike. Shows your joystick inputs in real time with history.

![Screenshot](screenshot.png)

## Requirements

- Chrome browser
- Any gamepad / arcade stick supported by your OS

## How to Use

1. Download the ZIP and extract
2. Open the extracted folder (`sf3-input-display-main`)
3. Open `index.html` with Chrome
4. Plug in your controller and press any button

## Features

- Real-time direction + button display
- Input history (last 20–35 entries, configurable)
- 1P / 2P layout toggle
- Super Art Input Tracker — detects SA input attempts and marks failed inputs in history
- Custom button mapping (click a button name, then press the stick)
- Custom direction mapping (supports standard stick and Hat Switch)
- Settings saved automatically in browser

## Super Art Input Tracker

Open **⚙ SUPER ART INPUT TRACKER** and toggle the moves you want to track. Each toggle is independent.

| Toggle | Input | Notes |
|--------|-------|-------|
| LP·LP·F·LK·HP | LP → LP → FWD → LK → HP | SGS |
| 222+PP | D → D → D → PP | KKZ (any 2+ punches) |
| DQCF+P | 236236 + P | Must pass through direction 6 |
| DQCF+K | 236236 + K | Must pass through direction 6 |
| 720+P | Full 720° rotation + P | Exclusive with other trackers |

When an attempt fails, a colored label appears on the history entry where the input went wrong:

| Label | Meaning |
|-------|---------|
| `!SGS` | SGS sequence broken |
| `!KKZ` | KKZ sequence broken |
| `!DQCF+P` | DQCF+P motion incomplete |
| `!DQCF+K` | DQCF+K motion incomplete |
| `!720+P` | 720 rotation incomplete |

If the move activates successfully, the **!** is automatically removed.

### DQCF Notes
- The QCF motion **must pass through direction 6** (pure forward). Stopping at diagonal 3 is detected as a failed attempt.
- Button can be pressed slightly before or after the final direction — all timing is accepted.

### 720+P Notes
- **Exclusive toggle**: activating 720+P disables all other trackers.
- Detection requires all 4 cardinal directions (2/4/6/8) within 11 frames, including direction 8 (up).
- Trigger: any punch (LP / MP / HP / PP / PPP).

## Button Mapping

Open **⚙ BUTTON & DIRECTION MAPPING** at the bottom of the page.

**Buttons (LP / MP / HP / LK / MK / HK / 3P / 3K)**
1. Click the button name
2. Press the corresponding button on your stick — done

**Directions (↑ ↓ ← →)**
1. Click the direction you want to remap
2. Wait for the label to change from `Ready...` to `Move!` (~1.5 seconds)
3. Push the stick in that direction and **hold it** until confirmed
4. Repeat for all 4 directions

> If your stick uses a Hat Switch, the direction mapping still works the same way — just push and hold each direction one at a time.

## License

MIT
