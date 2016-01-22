# Sublime-P
P language plugin for Sublime Text 3. Includes basic syntax highlighting, comments format and some snippets.

# Screenshot
![Screenshot](/example.png?raw=true)

# Install
Clone this repo into the user packages directory. E.g. `C:\Users\Paul\AppData\Roaming\Sublime Text 3\Packages\User\`.

Files with the `.p` extension will be recognized as Pascal files by default. 
Open a `.p` file and use `View -> Syntax -> Open all with current extension as ...` to change the default to the P language.

# Conventions
The syntax highlighting assumes the following conventions, but you don't have to follow them.  
* Type names end with `Type`. E.g. `StartMessageType`.
* Fields end with `V`. E.g. `TimerV`.
* Events start with `e`. E.g. `eStop`, `eStart`.
* Machine names end with `Machine`. E.g. `ElevatorMachine`.
* State names have no conventions and so have no color.

These conventions are followed by the snippets, so you don't have to remember them.

# Snippets
Snippets include: `event`, `implementation`, `machine`, `module`, `test`, `type`, `var` (for fields), `whileindex`.
To use a snippet, start typing one of these words and press tab. Then continue typing to replace the placeholder names and press tab further times to jump to the next placeholder or cursor position.

E.g. Start typing `while`. The `whileindex` completion pops up. Press tab to get:
```
index = 0;
while(index < sizeof(Array))
{
	
    index = index + 1;
}
```
Typing will replace all instances of `index`. Pressing tab jumps to `Array` which is the next placeholder. Pressing tab again places the cursor after the first curly brace.

# Making changes to `p.tmLanguage`
The `p.tmLanguage` file defines the syntax highlighting. It is a generated file, but is committed for convenience.
To make changes, do the following: 

1. Install [Package Control](https://packagecontrol.io/installation) in Sublime Text 3 and then use the Command Palette `Ctrl+Shift+P` to `Install Package` and search for and install `AAAPackageDev`. 
2. Open `p.YAML-tmLanguage`.
3. Make your changes.
4. Use the Command Palette to execute `Build With: Convert to ... - Property List`.
