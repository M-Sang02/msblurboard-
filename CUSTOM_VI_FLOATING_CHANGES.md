# FrostKeys custom changes

Based on FrostKeys 2.5.7 source.

Implemented:
- Vietnamese Telex composing engine:
  - aa -> â
  - aw -> ă
  - ee -> ê
  - oo -> ô
  - ow -> ơ
  - uw -> ư
  - dd -> đ
  - s/f/r/x/j tones and z tone removal
  - uppercase variants and NFC normalization
  - backspace operates on the raw composing sequence
- Vietnamese subtype now uses `CombiningRules=telex_vi`.
- Floating keyboard core:
  - toggle from toolbar/access-point
  - draggable floating keyboard
  - resize handle
  - persisted floating position and size per display width
  - automatic floating mode in landscape setting
  - floating mode disables one-handed mode while active
- Added Vietnamese translations for newly exposed settings/UI strings.
- Added floating keyboard strings in default and Vietnamese resources.
- Existing FrostKeys pinned-toolbar system remains available; Floating is an additional toolbar item.

Build note:
- The source was syntax/XML checked in this environment.
- A full Gradle build could not be run because the Gradle distribution was not cached and external download was unavailable.
