# Mach-O Packers Collection

A collection of popular and rare packers for native macOS Mach-O files, with sources for obtaining the tools and studying their output. Packed fixtures can serve as inputs for unpackers, dumpers and emulators.

## Known packers

These projects provide a tool, source code or a documented way to pack a user-supplied input. The target column describes upstream evidence. No fixtures have been built or tested in this collection yet. A directory link appears when hands-on research starts.

| Packer | Mechanism | Input or target | Directory | Sources |
| --- | --- | --- | --- | --- |
| UPX | Executable compression | Historical Darwin executables, including i386 and x86_64. From 4.2.0, macOS packing is disabled by default over compatibility with macOS 13+. | | [4.1.0 release](https://github.com/upx/upx/releases/tag/v4.1.0) · [Release history](https://github.com/upx/upx/blob/v5.3.0/NEWS) · [5.3.0 compatibility check](https://github.com/upx/upx/blob/v5.3.0/src/p_mach.cpp#L2179-L2185) |
| MPRESS | Executable compression | Intel Darwin applications (i386 and x86_64) and historical universal binaries. The vendor history does not identify an Apple Silicon target. | | [Archived MATCODE site](https://web.archive.org/web/20150305181805/http://www.matcode.com/mpress.htm) · [Distribution mirror](https://github.com/requaos/mPress) · [MATCODE release history](https://raw.githubusercontent.com/requaos/mPress/master/History.txt) |
| xsfx | LZMA2 self-extracting wrapper | Upstream lists x86_64 and arm64 Darwin targets. Which Mach-O payload types run on each remains unverified here. | | [Target matrix and source](https://github.com/ratushnyi-labs/xsfx) · [Releases](https://github.com/ratushnyi-labs/xsfx/releases) |
| Muncho | Compressing linker for 4K intros | Object files for historical Intel OS X. The author reports that the resulting executables stopped working on later systems. | | [Author's notes](https://jix.one/muncho/) · [Original release listing](https://www.pouet.net/prod.php?which=51324) |
| Pakr | Reversible bundle transformation | 64-bit `MH_BUNDLE` with a `main` entry point. The upstream example uses x86_64. | | [Source, input constraints and build instructions](https://github.com/iangcarroll/pakr) |

## Partially known packers

For tools with independent research or an unpacker whose workflow for packing our own Mach-O input is still unknown.

| Packer | Mechanism | Material | Sources |
| --- | --- | --- | --- |

## Unknown packers

For names identified only by a detector rule.

| Packer | Detector evidence | Sources |
| --- | --- | --- |

[Fixture profiles](fixtures/README.md) · [Research sources](sources.md) · [Contributing](CONTRIBUTING.md) · [Packer template](templates/README.md)
