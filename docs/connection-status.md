# DSL connection and status notes

## Connection address

```text
Host: dsl-mud.org
Port: 4000
```

## Terminal test

```bash
telnet dsl-mud.org 4000
```

## TinTin++ connection

```bash
tt++ dsl-mud.org 4000
```

Or from inside TinTin++:

```tintin
#session {dsl} {dsl-mud.org} {4000}
```

## Status note from the check

Public MUD listings showed **Dark and Shattered Lands** at:

```text
dsl-mud.org 4000
```

The listing checked showed the MUD server as up at the time, with active players connected.

The official DSL web pages may be flaky even when the MUD server itself is reachable. During the check, some official web pages returned a bad gateway response, but the MUD listing still showed the game server as running.

## Practical interpretation

If the website fails but the MUD listing or direct connection works, the MUD server may still be up.

Try the direct connection first:

```bash
tt++ dsl-mud.org 4000
```

If that fails, retry later or check public MUD status listings.
