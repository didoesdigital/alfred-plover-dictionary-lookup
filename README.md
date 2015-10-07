# README

This is an [Alfred workflow](https://www.alfredapp.com/help/workflows/) for using [this dictionary lookup tool](https://github.com/dimonster/plover-dictionary-lookup) for [Plover](https://github.com/openstenoproject/plover) made for OS X.

Derived from [this Automator workflow](http://stenoknight.com/plover/aviary/phpBB3/viewtopic.php?f=14&t=4386&p=6524&hilit=dictionary+lookup#p6524).


# Features

* Keyboard shortcut (⌃⌥⇧⌘P) to look up a selected word
* Alfred keyword ("plover") to activate lookup (eg, "plover dictionary")


# Dependencies

Requires a [dictionary lookup tool](https://github.com/dimonster/plover-dictionary-lookup).


# Installation

*  Dependency: Download and configure the [dictionary lookup tool](https://github.com/dimonster/plover-dictionary-lookup).

1.  Download the Alfred workflow:

    `git clone https://github.com/dimonster/alfred-plover-dictionary-lookup.git ~/alfred-plover-dictionary-lookup`

2.  Import the Alfred workflow (by double-clicking on it).
3.  Update the path in the Alfred workflow script to your `dictlook-ui.scpt` file.


# Usage

There are a few options for using the Alfred workflow:

- Select a word and use the keyboard shortcut (⌃⌥⇧⌘P) when Plover is switched off.
- Launch Alfred and type `plover the-word-you-want-to-lookup` (the space is optional).
- Create a brief for the keyboard shortcut to use on a selected word:

    `"PHR*FR": "{#Shift_L(Alt_L(Super_L(Control_L(p))))}",`

Note: I use the following brief to launch Alfred (normally ⌘ SPACE) without a subsequent space:

    `"A*FRL": "{#Super_L(space)} {^}",`
