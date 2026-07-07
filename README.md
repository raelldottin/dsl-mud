# DSL MUD Notes

Personal notes and TinTin++ setup for **Dark and Shattered Lands** / **DSL MUD**.

## Connection

```text
Host: dsl-mud.org
Port: 4000
```

Quick terminal connection:

```bash
telnet dsl-mud.org 4000
```

Preferred command-line client on macOS:

```bash
brew install tintin
tt++ dsl-mud.org 4000
```

Or start with the included profile:

```bash
mkdir -p ~/.tintin/logs
cp configs/dsl.tin ~/.tintin/dsl.tin
tt++ ~/.tintin/dsl.tin
```

## What is in this repo

- `configs/dsl.tin` — starter TinTin++ profile for macOS.
- `docs/tintin-setup.md` — client install and usability notes.
- `docs/paths-and-aliases.md` — travel aliases, including the Room of Healing path.
- `docs/prompt-and-colors.md` — DSL prompt variables and color-coded prompt examples.
- `docs/security-notes.md` — TinTin++ supply-chain and vulnerability notes from the check we discussed.

## Current preferred setup

Use **TinTin++** with:

- split mode, so game output does not overwrite the command being typed;
- large scrollback buffer;
- command echo off;
- speedwalk on;
- basic movement aliases;
- named travel aliases for important routes;
- a readable color-coded DSL prompt.

## Room of Healing path

Original path:

```text
d|se|e|e|e|n|e|e|e|e|open east|e|e|s
```

TinTin++ alias:

```tintin
#alias {roomofheal} {d;se;e;e;e;n;e;e;e;e;open east;e;e;s}
```

Easier aliases are also included:

```tintin
#alias {roomofhealing} {roomofheal}
#alias {toheal}        {roomofheal}
#alias {healroom}      {roomofheal}
#alias {roh}           {roomofheal}
```

Recommended alias to remember: `toheal`.

## Recommended DSL prompt

Directly in DSL:

```text
prompt <{RHP {W%h/%H {w| {CM {W%m/%M {w| {GMV {W%v/%V {w| {Y%e {w| {M%Xtnl {w| {y%gg {W%ss {w| {C%d{x>
```

Example shape:

```text
<HP 74/74 | M 126/126 | MV 124/124 | WD | 17957tnl | 0g 1827s | Night Time>
```

## Useful references

- Official DSL site: <https://www.dsl-mud.org/>
- DSL play page: <https://www.dsl-mud.org/playdsl/playdsl.asp>
- TinTin++: <https://tintin.mudhalla.net/>
- Homebrew TinTin++ formula: <https://formulae.brew.sh/formula/tintin>
- TinTin++ releases: <https://github.com/scandum/tintin/releases>
- NVD CVE-2019-7629: <https://nvd.nist.gov/vuln/detail/CVE-2019-7629>
