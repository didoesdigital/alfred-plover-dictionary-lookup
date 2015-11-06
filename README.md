# README

This is an [Alfred workflow](https://www.alfredapp.com/help/workflows/) for using [this dictionary lookup tool](https://github.com/dimonster/plover-dictionary-lookup) for [Plover](https://github.com/openstenoproject/plover) made for OS X.

Derived from [this Automator workflow](http://stenoknight.com/plover/aviary/phpBB3/viewtopic.php?f=14&t=4386&p=6524&hilit=dictionary+lookup#p6524).


# Features

* Keyboard shortcut (⌃⌥⇧⌘S) to look up a word from OS X clipboard contents
* Alfred keyword ("steno") to activate lookup (eg, "steno dictionary")


# Dependencies

Requires a [dictionary lookup tool](https://github.com/dimonster/plover-dictionary-lookup).


# Installation

*  Dependency: Download and configure the [dictionary lookup tool](https://github.com/dimonster/plover-dictionary-lookup).

1.  [Download the Alfred workflow](https://github.com/dimonster/alfred-plover-dictionary-lookup/archive/master.zip).
2.  Import the Alfred workflow (by double-clicking on it).
3.  Update the path to the `dictlook-ui.scpt` file in the Alfred workflow script.


# Usage

There are a few options for using the Alfred workflow:

1. Use the keyboard hotkey.
2. Launch Alfred and use the keyword.
3. Use a brief to look up the previous word next to your cursor.
4. Use a brief to look up the selected word.


## 1. Alfred Hotkey (`⌃⌥⇧⌘S`)

- Copy (`⌘C`) the word you want to look up.
- Use the keyboard shortcut (`⌃⌥⇧⌘S`).


## 2. Alfred Keyword (`steno`)

- Launch Alfred (⌘ SPACE) — you can configure this in Alfred:

    `"A*FRL": "{#Super_L(space)} {^}",`


- Type `steno the-word-you-want-to-look-up` (the space is optional):

    `"STOEUPB": "steno",`


## 3. Brief to look up previous word

- Use a brief to select the previous word next to your cursor, copy it, deselect the word by moving the cursor right, and finally look up the word:

    `"STOEUFRL": "{#Alt_L(Shift_L(Left))} {#Super_L(c)} {#Right} {#Control_L(Alt_L(Shift_L(Super_L(s))))}",`


## 4. Brief to look up a copied word from clipboard contents

- Use a brief to copy the selected word, deselect it by moving the cursor right, and finally look up the word:

    `"STOEUFRPBL": "{#Super_L(c)} {#Right} {#Control_L(Alt_L(Shift_L(Super_L(s))))}",`
