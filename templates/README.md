# Packer directory layout

Copy the [README template](packer/README.md) when creating a directory in `packers/`. Create only the paths that the case uses.

```text
packers/<packer-id>/
  README.md
  internals.md
  packed-fixtures/<version>/fixture-<arch>-<kind>/<profile>/
  packed-samples/<version>/<sample-name>/
  tools/<version>/bin/
  tools/<version>/src/
```

- `README.md` lists references, tested versions, packing commands and results. Optional `internals.md` holds technical observations and reproducible experiments.
- `packed-fixtures/` holds verified packed outputs. Use the input architecture and role in the directory name, for example `fixture-x86_64-exe`, `fixture-arm64-dylib` or `fixture-x86_64-bundle`. Use `universal` for a multi-slice input and identify the slices in the README.
- `packed-samples/` holds imported samples under their own names.
- `bin/` holds the packer executable and required dependencies. Preserve source in `src/` or keep a distribution archive when a stable public download is unavailable. Use version `0` when a version is unknown or unnumbered.
