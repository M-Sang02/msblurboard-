# FrostKeys Gboard-like UI update

This build keeps the existing FrostKeys/HeliBoard functionality and adjusts the toolbar/access-point workflow toward the interaction pattern shown in the supplied Gboard video.

Included:
- Emoji panel with built-in emoji search.
- Emoji search key in the emoji bottom row.
- Fixed persistent voice-input button at the right side of the suggestion/toolbar strip.
- Access-point menu changed to a two-column, horizontal-pill layout.
- Access-point menu defaults include Settings, Resize, Clipboard, Emoji, GIFs, Stickers, One-handed, Floating, Select all, Select word, Copy, Cut, Paste, Undo, Redo and cursor movement.
- Floating keyboard toggle remains available.
- Toolbar mode settings remain: Pinned buttons + suggestions, Pinned buttons only, Suggestions only, Hidden.
- Toolbar/pinned/clipboard key customization and quick-pin remain.
- Existing Vietnamese Telex and landscape floating behavior remain.

The UI is an independent implementation inspired by the interaction pattern in the supplied video; it does not copy Gboard proprietary source/assets.


## Theme additions in this build

- Keeps FrostKeys 2.5.7's frosted-glass rendering as the visual base.
- Adds a second built-in **Frosted Glass (Opaque) / Kính mờ đục** preset directly to the default theme list. It uses the same frosted/blur pipeline but with a denser translucent surface so it is closer to the semi-opaque look in the supplied reference.
- The Gboard-Patched repository is used only as a reference for interaction/layout ideas; this build does not copy Gboard proprietary code or assets.

## msblurboard integration notes

This build keeps FrostKeys' existing translucent/frosted visual pipeline as the visual baseline. Gboard-like behavior is implemented independently using the existing keyboard architecture and public Android/AOSP LatinIME concepts.

Added in this revision:
- Floating keyboard bottom controls: hide keyboard and switch to the next input method.
- Toolbar actions: Translate, Switch keyboard, Hide keyboard.
- Clipboard remains the primary paste surface; the default access-point toolbar no longer promotes the standalone Paste action.
- Clipboard history already supports text and image/screenshot entries and can expose a recent screenshot as a suggestion when the screenshot setting and permission are enabled.
- Translation opens a lightweight translation panel and hands the text to Google Translate in the browser; no proprietary Gboard code or assets are bundled.
- Output archive name is unified as `msblurboard.zip`.

Public-source reference: Android Open Source Project LatinIME provides the open implementation patterns for language switching and input-method switching. Gboard-Patched is an APKTool/smali patching project rather than a public Gboard source tree, so it is used only as a behavioral/UI reference.
