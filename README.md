# Proxy-dlls

A collection of proxy DLL projects used for game modding, research, debugging, and framework development.

## Why I Use Proxy DLLs

Many games automatically load specific DLL files from their game directory before loading the real system version. A proxy DLL takes advantage of this behavior by acting as a middle layer between the game and the original library.

This allows custom code to run as soon as the game starts without modifying the game's executable.

Using a proxy DLL provides several advantages:

* No executable patching required
* Loads automatically when the game starts
* Easier to distribute and update
* Works with many different games
* Useful for logging, debugging, and research
* Can load additional plugins and modules
* Can intercept and modify game functions
* Allows custom frameworks to initialize early

## How My Setup Works

The game starts normally.

The game attempts to load a DLL such as:

* steam_api.dll
* dinput8.dll
* xinput1_3.dll
* winmm.dll
* version.dll
* dsound.dll

Instead of loading the original library directly, it loads the proxy DLL.

The proxy DLL then:

1. Loads the original DLL from the system or backup location.
2. Resolves all required exports.
3. Forwards calls back to the original DLL.
4. Initializes custom code.
5. Loads plugins, hooks, patches, or debugging tools.

Flow example:

Game.exe

↓

Proxy DLL

↓

Custom Framework

↓

Original DLL

↓

Game Continues Normally

## Typical Uses

### Research

* Function tracing
* Memory inspection
* Network analysis
* File loading analysis

### Modding

* Custom loaders
* Plugin systems
* Asset replacement
* Script loading
* Quality of life features

### Development

* Debug consoles
* Logging systems
* Diagnostics
* Framework testing

## Example Startup Sequence

1. Game launches.
2. Game loads proxy DLL.
3. Proxy DLL loads original DLL.
4. Custom initialization runs.
5. Hooks and patches are installed.
6. Original functionality is preserved.
7. Game continues normally.

## Goals

This repository exists to document and archive various proxy DLL implementations and techniques used in personal projects.

The focus is on:

* Learning
* Reverse engineering research
* Framework development
* Modding tools
* Preservation projects

## Repository Structure

```text
Proxy-dlls/
├── steam_api/
├── dinput8/
├── xinput/
├── common/
├── examples/
└── docs/
```

## Notes

Different games load different DLLs during startup. Some projects use steam_api.dll while others use dinput8.dll, xinput, winmm, or other commonly loaded libraries.

The best DLL to proxy depends on the target application and how early initialization is required.

## Disclaimer

This repository is intended for educational purposes, software research, compatibility testing, preservation efforts, and modding development.

Users are responsible for complying with all applicable laws, licenses, and terms of service when using any code or techniques contained in this repository.
