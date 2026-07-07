# TinTin++ setup for DSL on macOS

## Recommended client

Use **TinTin++** for a command-line MUD client on macOS.

Install with Homebrew:

```bash
brew install tintin
```

Connect directly:

```bash
tt++ dsl-mud.org 4000
```

Or use the profile in this repo:

```bash
mkdir -p ~/.tintin/logs
cp configs/dsl.tin ~/.tintin/dsl.tin
tt++ ~/.tintin/dsl.tin
```

## Why TinTin++

TinTin++ is a good terminal client for DSL because it supports:

- aliases;
- triggers/actions;
- delays;
- command history;
- split input/output;
- logging;
- speedwalk;
- mapper support later, after the basic route aliases are stable.

## Best comfort settings

The most important settings from the starter profile are:

```tintin
#split 0 1
#config {SCROLL LOCK} {ON}
#config {COMMAND ECHO} {OFF}
#config {BUFFER SIZE} {100000}
#config {SPEEDWALK} {ON}
```

### What they do

- `#split 0 1` keeps a stable input line so new game output does not overwrite what is being typed.
- `SCROLL LOCK` helps when reading back through output.
- `COMMAND ECHO OFF` keeps the display cleaner.
- `BUFFER SIZE 100000` keeps a larger scrollback history.
- `SPEEDWALK ON` allows compact movement strings.

## If game output overwrites typed commands

Inside TinTin++:

```tintin
#split
```

Turn it off with:

```tintin
#unsplit
```

## Speedwalk warning

With speedwalk enabled, TinTin++ may interpret strings made from direction letters as movement. For example:

```text
ssw2n
```

means:

```text
south, south, west, north, north
```

If a real command conflicts with speedwalk, type the command more explicitly or disable speedwalk temporarily.

## Mapper note

Do not rush into full automapping. Start with aliases and logs first. Automapping can create wrong rooms when a route hits a closed door, wall, no-exit message, or one-way movement unless it is configured carefully.
