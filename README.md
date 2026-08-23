[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE.md) [![Haxelib Version](https://img.shields.io/github/tag/openfl/dragonbones.svg?style=flat&label=haxelib)](http://lib.haxe.org/p/dragonbones)

DragonBones
===========

Haxe runtime support for DragonBones, a skeletal animation editor.

## Haxe 4 & HXCPP Fork Notes

This repository is an experimental fork of [openfl/dragonbones](https://github.com/openfl/dragonbones) focused on Haxe 4 and C++ (HXCPP) target compatibility.

### Compatibility & Status
* **Target Engine**: Haxe 4.x + HXCPP (Android).
* **Backend Status**:
  * **Starling Backend**: Refactored for Haxe 4 / HXCPP; initial compilation and basic rendering verified with test armatures.
  * **Core Engine**: Modernized type checks (`Std.isOfType`) and safe array padding (`ObjectDataParser`, `BaseFactory`).
  * **Flixel / OpenFL Backends**: Untested (kept at upstream version).
* **Key Fixes**: Replaced `Vector<Object>` with `Array<Dynamic>` to fix C++ template casting errors and normalized `Std.isOfType` usage.


Installation
------------

You can easily install DragonBones using haxelib:

    haxelib install dragonbones

To add it to a Lime or OpenFL project, add this to your project file:

    <haxelib name="dragonbones" />


Development Builds
------------------

Clone the DragonBones repository:

    git clone https://github.com/openfl/dragonbones


Tell haxelib where your development copy of DragonBones is installed:

    haxelib dev dragonbones dragonbones


To return to release builds:

    haxelib dev dragonbones



