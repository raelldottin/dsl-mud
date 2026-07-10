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

- `docs/background.md` — what DSL is and the client choice from the conversation.
- `configs/dsl.tin` — starter TinTin++ profile for macOS.
- `docs/connection-status.md` — connection address and server-status notes.
- `docs/tintin-setup.md` — client install and usability notes.
- `docs/paths-and-aliases.md` — travel aliases, including the Room of Healing path.
- `docs/prompt-and-colors.md` — DSL prompt variables and color-coded prompt examples.
- `docs/tintin-release-notes.md` — TinTin++ release, install, and safety notes from the check we discussed.
- `docs/resources.md` — useful external DSL research resources, including Shattered Archive.
- `docs/areas-index.md` — parsed DSL area index with level-5 planning notes.
- `data/raw/areas-2026-07-07.txt` — raw pasted DSL area listing.
- `characters/yttawstp/2026-07-07-score.md` — Yttawstp level 5 Yinn Mage score snapshot.

## Current preferred setup

Use **TinTin++** with:

- split mode, so game output does not overwrite the command being typed;
- large scrollback buffer;
- command echo off;
- speedwalk on;
- basic movement aliases;
- named travel aliases for important routes;
- a readable color-coded DSL prompt.

## Character snapshots

### Yttawstp

Current tracked snapshot:

```text
Level: 5
Race: Yinn
Class: Mage
Profession: Alchemist
Alignment: True Neutral
HP/Mana/Move: 74/74, 126/126, 124/124
XP To Level: 17957
Silver: 1827
```

See: `characters/yttawstp/2026-07-07-score.md`

## Area planning

The captured area listing was parsed into **416 area entries** across DSL regions.

Level-5 planning for Yttawstp:

```text
Level-5-accessible entries: 175
Tight beginner entries, max level <= 15: 44
Nearby low-level entries, max level 16-25: 7
```

See:

```text
docs/areas-index.md
data/raw/areas-2026-07-07.txt
```

## Research resources

Shattered Archive is now tracked as a key external source:

```text
https://shatteredarchive.com
```

Use it for directions, items, rooms, races, classes, trainers, and player guides. See: `docs/resources.md`.

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
- Shattered Archive: <https://shatteredarchive.com>
- TinTin++: <https://tintin.mudhalla.net/>
- Homebrew TinTin++ formula: <https://formulae.brew.sh/formula/tintin>
- TinTin++ releases: <https://github.com/scandum/tintin/releases>
- NVD CVE-2019-7629: <https://nvd.nist.gov/vuln/detail/CVE-2019-7629>
