# Style Guide

## General

- Use American English.
- Use capitals and spaces for folder names.
- Use capitals but no spaces for layout names.
- Global layers should be added to a layout named _GlobalLayers_.
- Objects that are never used in a layout (only instanced) should be kept in a layout named _ObjectBank_.
- Objects that are added to whole project (such as _Function_, _Keyboard_, etc.) should be added under a folder named _"System"._
- Objects are prefixed by type and a underscore (i.e. _spr_player_). The list of prefixes for this particular project follow:
  - _Not ready yet, sorry!_
- Audio files use the same syntaxis with the following prefixes:
  - Sound effects: __sfx__
  - Music: __msc__

## Code Basics

- Long function/variable names are fine, undescriptive ones aren't.
- Comment your code! 
- Includes should be added in alphabetical order.
- Every comma should be followed by a space.
- Spaces around operators so "2 + 2", not "2+2".

## Event Sheets

- Event sheets use the following syntaxis:
  - _el(EventSheetName)_ if it's a sheet a layout uses.
  - _e(EventSheetName)_ otherwise.
- All "el" event sheets should be kept in a separate folder named _Layout Sheets_.
- Group names follow the convention _(EventSheetName)/(GroupName)_.
- All groups should have descriptions.

## Functions

- Functions use the following naming convention:
  - _(EventSheetName)/(GroupName).(function_name)_ if it belongs to a group.
  - _(EventSheetName).(function_name)_ otherwise.
  - If the function is __"public"__ (called from another event sheet) the function name is capitalized.
- When creating a function that uses "Pick by unique ID", place it as a subevent, not a condition to the function event.
- If the functions does not require the pick subevent, add a blank subevent and place actions there.
- If not inmediately obvious, functions should have a comment that explains what it does.
- If a function is "public" it should contain a comment inside it listing which sheets call it.

## Variables

- Constant variables are in all-caps by Construct.
- If you require a local/global variable to serve as a boolean, make a string and use "true" or "false".
- In general prefer local variables, but if a global variable is necesarry all of them should be in a single event sheet named _eGlobalVariables_.
- Global variables should be capitalized (i.e. _Current_State_), while local variables use lower case (i.e. _player_health_).
- Family instance variables should be capitalized, while object variables should use lower case.

## Source Control

- Don't forget to ignore _*.uistate.xml_.
- Never commit debugging code.
- Commiting code with to-do comments is not ideal, but when it's done mark it with comment starting with _"TODO:"_ and bookmark it.
