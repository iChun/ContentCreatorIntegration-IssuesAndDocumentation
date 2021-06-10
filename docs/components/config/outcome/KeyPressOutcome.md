Key Press Outcome
============= 

## Description

Sets a keybind to the set pressed state. Either `keyName`, `inputName`, or `rawInput` needs to be set. CCI tries them in that order. This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `keyPress`       |         Not seen in the Editor.        |
| *`keyName`*[^1] | String |      Keybind to set. Key name can be found in options.txt. EG: `key_key.forward:key.keyboard.w`, the key is `key.forward`. Omit the `key_` prefix.       |                 |
| *`inputName`*[^1] | String |      Directly presses a key. Input name can be found in `options.txt`. EG: `key_key.forward:key.keyboard.w`, the input name is `key.keyboard.w`.       |                 |
| *`rawInput`*[^1] | String |      Directly interfaces with GLFW to simulate a key input.       |          Read below for instructions.       |
| `pressed` | Boolean |      Pressed state to set. Keeping it as `null` unpresses the key. Ignored on `rawInput`.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
[^1]: Either field is required for the Object to be valid.


## How to use `rawInput`

Direct raw input in numbers. Bit technical, but for when all else fails (or if you want to add modifiers like Shift, Ctrl, Alt). Split with commas. Order them by: `keyCode/button`,`scanCode/isMouse(-1)`,`action`,`modifiers`. Bit technical but look up `GLFW keyboard keycodes` or `GLFW key modifiers` for some guidance.

`scanCode` generally doesn't really matter if you're using key codes, and set it to `-1` if you want to trigger a mouse input instead

Action is `1` for pressed, `0` for unpress

EG: `87,17,1,0` to press down the W key (on QWERTY keyboards) with no modifiers
