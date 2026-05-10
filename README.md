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
4. Plug in your joystick and press any button

## Features

- Real-time direction + button display
- Input history (last 20 entries)
- 1P / 2P layout toggle
- Custom button mapping (click a button name, then press the stick)
- Custom direction mapping (supports standard stick and Hat Switch)
- Settings saved automatically in browser

## Button Mapping

Open **BUTTON & DIRECTION MAPPING** at the bottom of the page.

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
