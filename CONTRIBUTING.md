# Contributing

- Keep one [index entry](README.md#known-packers) per family. Prefer the author's release, source or manual. Use an archive or mirror when a historical distribution is hard to obtain.
- Create a packer directory when hands-on work starts. Link it in the Directory column and place entries with directories first. Use the [packer template](templates/README.md).
- Generate cases from copies of the [shared fixtures](fixtures/README.md). Record the input profile, packer version, options, output type, macOS version and test environment. For a wrapper, identify the input and outer Mach-O types separately.
- Keep working outputs in `packed-fixtures/` after checking normal execution, wait behavior and markers under the documented conditions. Record failed checks, unsupported inputs and untested slices in the packer's README. Say whether recovery reproduced the original bytes or a narrower property.
- Keep third-party samples separate and document their source, original filename and provenance. Run automated fixture checks only on collection-owned inputs.
- Use English and plain Markdown. Preserve executable permissions in Git. Commit each newly researched packer separately as `add <Packer name>`. Run `python tools/check_links.py` after editing documentation.
