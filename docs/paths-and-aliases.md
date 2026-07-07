# DSL paths and aliases

## Room of Healing

Original route captured from the session:

```text
d|se|e|e|e|n|e|e|e|e|open east|e|e|s
```

TinTin++ alias:

```tintin
#alias {roomofheal} {d;se;e;e;e;n;e;e;e;e;open east;e;e;s}
```

## Easier names to remember

Use multiple aliases that all point to the same route:

```tintin
#alias {roomofheal}    {d;se;e;e;e;n;e;e;e;e;open east;e;e;s}
#alias {roomofhealing} {roomofheal}
#alias {toheal}        {roomofheal}
#alias {healroom}      {roomofheal}
#alias {roh}           {roomofheal}
```

Recommended alias:

```text
toheal
```

Reason: it reads like an action — go to the healing room.

## Slower version

If DSL ignores some commands because they arrive too fast, use delays:

```tintin
#alias {tohealslow} {
  d;
  #delay {0.2} {se};
  #delay {0.4} {e};
  #delay {0.6} {e};
  #delay {0.8} {e};
  #delay {1.0} {n};
  #delay {1.2} {e};
  #delay {1.4} {e};
  #delay {1.6} {e};
  #delay {1.8} {e};
  #delay {2.0} {open east};
  #delay {2.2} {e};
  #delay {2.4} {e};
  #delay {2.6} {s}
}
```

## Local route help

Add a small command so the alias names are easy to rediscover:

```tintin
#alias {paths} {
  #showme {Travel aliases:};
  #showme {  toheal / roh / roomofheal = Room of Healing};
  #showme {  tohealslow               = slower Room of Healing route}
}
```

Then type:

```text
paths
```

## Naming warning

Avoid naming a route alias simply `heal`. In MUDs, `heal` may already be a game command, spell, NPC interaction, or shop command.
