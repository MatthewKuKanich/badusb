# Comprehensive DuckyScript 1.0 and Flipper Zero Extended Commands Chart

This chart combines the standard DuckyScript 1.0 commands and the updated extended commands specific to the Flipper Zero platform.
The Flipper Zero Bad USB functionality also goes by the name Bad KB for some firmwares due to its Bluetooth abilities. Programming
for these is the exact same.

---

| Command                    | Syntax                                  | Description                                                          |
|----------------------------|-----------------------------------------|----------------------------------------------------------------------|
| `REM`                      | `REM [comment text]`                    | Adds comments; ignored during execution.                             |
| `DELAY`                    | `DELAY [time in ms]`                    | Pauses execution for specified time in milliseconds.                 |
| `STRING`                   | `STRING [text to type]`                 | Types a string as keyboard input.                                    |
| `STRINGLN`                 | `STRINGLN [text to type]`               | Types a string and adds a newline character at the end.             |
| `DEFAULT_DELAY` / `DEFAULTDELAY` | `DEFAULT_DELAY [time in ms]`     | Sets a default delay between commands.                               |
| `STRINGDELAY` / `STRING_DELAY` | `STRINGDELAY [time in ms]`         | Sets a delay between each character in a string.                    |
| `REPEAT`                   | `REPEAT [times]`                        | Repeats the last command a specified number of times.                |
| `SYSRQ`                    | `SYSRQ [Single character]`              | Executes a command using the Magic SysRq key (Linux).                |
| `ALTCHAR`                  | `ALTCHAR [Character code]`              | Prints a single character using ALT+Numpad method (Windows).         |
| `ALTSTRING` / `ALTCODE`    | `ALTSTRING [Text string]`               | Prints a text string using ALT+Numpad method (Windows).              |
| `HOLD`                     | `HOLD [key]`                            | Holds down a specified key.                                         |
| `RELEASE`                  | `RELEASE [key]`                         | Releases a specified key that was held down.                        |
| `WAIT_FOR_BUTTON_PRESS`    | `WAIT_FOR_BUTTON_PRESS [button]`                 | Waits for a button press to continue execution.                      |
| `GUI`                      | `GUI [key]`                             | Represents the Windows key or Command key on Mac.                   |
| `ALT`                      | `ALT [key]`                             | Holds down the Alt key; can combine with other keys.                |
| `CTRL`                     | `CONTROL [key]` or `CTRL [key]`         | Holds down the Ctrl key; can combine with other keys.               |
| `SHIFT`                    | `SHIFT [key]`                           | Holds down the Shift key; can combine with other keys.              |
| `DOWNARROW`                | `DOWNARROW`                             | Represents the Down Arrow key.                                      |
| `UPARROW`                  | `UPARROW`                               | Represents the Up Arrow key.                                        |
| `LEFTARROW`                | `LEFTARROW`                             | Represents the Left Arrow key.                                      |
| `RIGHTARROW`               | `RIGHTARROW`                            | Represents the Right Arrow key.                                     |
| `ENTER`                    | `ENTER`                                 | Simulates the Enter key.                                            |
| `TAB`                      | `TAB`                                   | Simulates the Tab key.                                              |
| `ESCAPE`                   | `ESCAPE` or `ESC`                       | Simulates the Escape key.                                           |
| `PRINTSCREEN`              | `PRINTSCREEN`                           | Simulates the Print Screen key.                                     |
| `DELETE`                   | `DELETE`                                | Simulates the Delete key.                                           |
| `INSERT`                   | `INSERT`                                | Simulates the Insert key.                                           |
| `SPACE`                    | `SPACE`                                 | Simulates the Spacebar key.                                         |
| `CAPSLOCK`                 | `CAPSLOCK`                              | Toggles the Caps Lock key.                                          |
| `F1` to `F12`              | `F1` to `F12`                           | Represents the function keys.                                       |
| `BREAK`                    | `BREAK` or `PAUSE`                      | Simulates the Break or Pause key.                                   |
| `NUMLOCK`                  | `NUMLOCK`                               | Toggles the Num Lock key.                                           |
| `SCROLLLOCK`               | `SCROLLLOCK`                            | Toggles the Scroll Lock key.                                        |

---

# Overview and Use

---

## DuckyScript 1.0 Basic Commands

DuckyScript is a scripting language used for creating payloads for USB Rubber Ducky and similar devices. The basic syntax includes the following commands:

- **REM**: Used for adding comments in the script. Anything following `REM` on the same line is ignored during execution.
- **DELAY**: Pauses execution for a specified number of milliseconds.
- **STRING**: Types out a string of characters as if typed on a keyboard.
- **REPLAY**: Repeats the last command the specified number of times.

Refer to the [original DuckyScript documentation](https://web.archive.org/web/20220816200129/http://github.com/hak5darren/USB-Rubber-Ducky/wiki/Duckyscript) for more details on these commands.

---

## Flipper Zero Extended Commands

The Flipper Zero Bad USB functionality extends the DuckyScript 1.0 with additional commands to leverage its unique features:

### Modifier Keys

These commands use various keyboard modifiers:

- **CTRL-ALT**
- **CTRL-SHIFT**
- **ALT-SHIFT**
- **ALT-GUI**
- **GUI-SHIFT**

### ALT+Numpad Input

For inputting characters using the ALT key and a code on the Numpad on Windows:

- **ALTCHAR**: Prints a single character.
- **ALTSTRING / ALTCODE**: Prints a text string using the ALT+Numpad method.

### Magic SysRq Key

For Linux systems, to execute commands using the Magic SysRq Key:

- **SYSRQ**: Executes a command using a single character with the SysRq key.

### Usage

- Scripts must be in `.txt` format.
- Both `\n` and `\r\n` line endings are supported.
- Empty lines and indentation using spaces or tabs are allowed.

---

## Uploading and Executing Payloads on Flipper Zero

To use these scripts on Flipper Zero:

1. Write the payload in a text editor and save it as a `.txt` file.
2. Upload the script to your Flipper Zero using either qFlipper or Flipper Mobile App into the `SD Card/badusb/` folder.
3. On the Flipper Zero, navigate to `Main Menu -> Bad USB`.
4. Select the payload and press `OK`.
5. Connect the Flipper Zero to the computer via USB.
6. Execute the payload.

---

## Additional Information

- The Flipper Zero acts as a BadUSB device, recognized as a Human Interface Device (HID).
- It can execute extended Rubber Ducky script syntax compatible with classic USB Rubber Ducky 1.0 scripts.
- Flipper Zero offers additional features like custom USB ID, ALT+Numpad input method, SYSRQ command, and more functional keys.

For further details, refer to the [Flipper Zero documentation](https://docs.flipper.net/bad-usb).

---
As with any tool, use it responsibly. I'm not responsible for what you do with this.
