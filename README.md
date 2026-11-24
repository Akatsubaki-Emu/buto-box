# buto-box
> An application that converts and repackages windows and Linux applications into iOS/IpadOS, TVOS and VisionOS applications
>
> 
 # buto-box

Packager that wraps Windows `.exe` binaries and game directories with the *Kenran Butō* runtime into standalone `.ipa` archives for iOS and tvOS.

Part of [Akatsubaki-Emu](https://github.com).

> **Note:** This project is currently in early development and not yet ready for building or general use.

## Overview

`buto-box` aims to automate bundling PC executables and their required runtime dependencies into self-contained, sideloadable iOS and tvOS app packages.

### Planned Workflow

1. Unpack a base iOS/tvOS host stub linked against the Kenran Butō core.
2. Inject the target `.exe` and supporting files into the app bundle's payload directory.
3. Patch `Info.plist` with custom bundle identifiers, display names, icons, and launch arguments.
4. Package the `Payload/` structure into an `.ipa` ready for sideloading (AltStore, SideStore, Sideloadly) and JIT attachment.

## Target Requirements

- iOS / iPadOS 17.4+ or tvOS 17.4+
- Compatible JIT enabler or debugger attachment (e.g., StikDebug, SideStore, or Xcode)

## Roadmap

- [ ] Base `.ipa` stub injection and `Info.plist` patching
- [ ] Single `.exe` and full game directory packaging
- [ ] Static `.dll` dependency scan
- [ ] Per-bundle controller mapping and environment profiles
- [ ] Optional `ldid` / provisioning profile signing

## License

GPL-3.0. See `LICENSE`.

