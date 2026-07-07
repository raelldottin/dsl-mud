# TinTin++ release and install notes

These notes summarize the TinTin++ package check discussed before using the client for DSL.

## Recommended install path

Use Homebrew or the official source release.

```bash
brew update
brew install tintin
tt++ -V
```

Avoid random installers, bundled binaries, unknown images, or downloaded `.tin` scripts from people you do not trust.

## Version noted during the check

```text
TinTin++ 2.02.61
Release date found: Jan. 29, 2026
```

Homebrew was also found to be on TinTin++ `2.02.61` at the time of the check.

## Development changes noted

The detailed TinTin++ changelog entry for `2.02.61` noted a fix in `substitute.c` for improper handling of large variables.

The previous `2.02.60` release notes included:

- upgrade from PCRE1 to PCRE2;
- base64 conversion fixes;
- sorting upgraded to quadsort;
- a map event addition.

## Practical safety rules

- Keep TinTin++ current.
- Prefer Homebrew or official source.
- Be cautious with `.tin` scripts from other players.
- Read scripts before running them.
- Do not store real passwords or private notes in shared config files.
- Keep logs local unless you intentionally want to publish them.

## Links

- TinTin++ releases: <https://github.com/scandum/tintin/releases>
- TinTin++ official site: <https://tintin.mudhalla.net/>
- Homebrew formula: <https://formulae.brew.sh/formula/tintin>
