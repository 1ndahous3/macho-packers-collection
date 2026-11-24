# Research sources

| Source | Use |
| --- | --- |
| [Awesome Executable Packing](https://github.com/packing-box/awesome-executable-packing) | Find historical names, packer projects and original distributions. |
| [Detect It Easy Mach-O rules](https://github.com/horsicq/Detect-It-Easy/tree/master/db/MACH) | Trace a detector label to its rule and cross-check aliases. |
| [Apple Mach-O definitions](https://github.com/apple-oss-distributions/xnu/blob/main/EXTERNAL_HEADERS/mach-o/loader.h) | Identify file types, CPU fields, segments and load commands. |
| [Apple universal binary guide](https://developer.apple.com/documentation/apple-silicon/building-a-universal-macos-binary) | Identify the slices of a universal binary and select each one for testing. |
| [Apple code signing guide](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Procedures/Procedures.html) | Inspect and verify signatures before and after packing. |

The [index](README.md#known-packers) links to the release or source for each tool. Scope includes native executable packers, wrappers for user-supplied Mach-O payloads and compressing linkers for macOS. Record the accepted input type for each. Generic disk images, installers, ordinary app bundles and iOS-only tools are outside this index.
