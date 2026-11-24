# Mach-O fixtures

The initial fixture matrix is planned. This directory currently contains the specification only.

| Input | Architectures | Intended runtime check |
| --- | --- | --- |
| Executable (`MH_EXECUTE`) | x86_64, arm64 | Run normally and with `--wait`. |
| Dynamic library (`MH_DYLIB`) | x86_64, arm64 | Load from a matching process and call the normal and wait exports. |

Use the same four marker byte sequences as the PE and ELF fixtures, in executable code, read-only data, writable data and a dedicated section. The normal and wait paths should both verify the markers. In wait mode the fixture should signal readiness and remain alive until terminated.

Add a loadable `MH_BUNDLE` when testing a packer that requires one, such as Pakr. For a compressing linker such as Muncho, keep the object input and identify its compiler and target. Historical i386 cases need their own OS X profile.

For a universal binary, record the actual slices and verify each one. Record the macOS version, whether execution was native or translated by Rosetta, and signature status before packing, after packing and after any re-signing used for the test. [Apple universal binary guide](https://developer.apple.com/documentation/apple-silicon/building-a-universal-macos-binary)
