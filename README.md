[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE.md) [![Haxelib Version](https://img.shields.io/github/tag/openfl/dragonbones.svg?style=flat&label=haxelib)](http://lib.haxe.org/p/dragonbones)

DragonBones
===========

Haxe runtime support for DragonBones, a skeletal animation editor.

## Haxe 4 & HXCPP Fork Notes

This repository is a fork of [openfl/dragonbones](https://github.com/openfl/dragonbones) focused on Haxe 4 and C++ (HXCPP) target compatibility.

### Compatibility & Status
* **Target Engine**: Haxe 4.x + HXCPP (Android).
* **Backend Status**:
  * **Starling Backend**: Production-tested on Android.
  * **Core Engine**: Modernized type checks (`Std.isOfType`), safe array padding (`ObjectDataParser`, `BaseFactory`), and a defensive null-check in `ArmatureData.getBone` / `getSlot` (guards against lookups with a `null` name).
  * **Flixel / OpenFL Backends**: Untested, kept at upstream version — no changes applied.
* **Key Fixes**: Replaced `Vector<Object>` with `Array<Dynamic>` to fix C++ template casting errors and normalized `Std.isOfType` usage.

Note: `Vector<Dynamic>` alone does not fix this. HXCPP's `Vector<T>` abstract resolves `Dynamic` ambiguously against multiple `@:to` overloads (Bool/Int/Float/Object), so `Array<Dynamic>` was used instead to bypass the specialization entirely.


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

