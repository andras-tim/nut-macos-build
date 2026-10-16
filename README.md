# nut-macos-build

Universal (arm64 + x86_64) macOS build of the [Network UPS Tools](https://networkupstools.org/) **client** tools
(`upsmon`, `upssched`, `upsc`, ...) from the official NUT source release, for Macs that are NUT clients of a remote
`upsd`. Homebrew ships no Intel bottles for `nut` any more, and this gives one binary for every Mac.

- Source: the official `nut-<version>.tar.gz` release asset, verified by SHA-256 in the workflow.
- Installs under `/opt/nut` (`bin`, `sbin`, `etc`, `var/state/ups`), runs as `nobody` after dropping root.
- No SSL, USB, serial or SNMP: plain NUT protocol to the server, no hardware drivers.
- Minimum macOS: 12.
- A `v*` tag publishes `nut-<version>-macos-universal.tar.gz` as a GitHub release.
