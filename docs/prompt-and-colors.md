# DSL prompt and colors

DSL supports custom prompts with variables and color codes.

## Prompt variables captured from `help prompt`

```text
%h : current hits
%H : maximum hits
%m : current mana
%M : maximum mana
%v : current moves
%V : maximum moves
%x : current experience
%X : experience to level
%g : gold held
%s : silver carried
%q : questpoints
%C : craftskill
%S : battle stance
%a : alignment
%r : room name
%e : exits in NESWDU style
%c : carriage return, useful for multi-line prompts
%R : vnum, immortal only
%z : area name, immortal only
%t : current game time
%T : current game time
%d : Dawn / Day / Sun Set / Night Time
%y : current wimpy setting
%f : flying status
%l : current language
%L : XP until merit, level 51
%D : chamber for dragons, otherwise day status
```

## DSL color codes captured from `help color`

DSL color codes start with `{` and should end with `{x` to prevent color bleed.

```text
{r red        {R light red
{y yellow     {Y light yellow
{b blue       {B light blue
{c cyan       {C light cyan
{m magenta    {M light magenta
{g green      {G light green
{D black      {W light white
{o orange     {p pink
{n brown      {u purple
{w grey       {x reset colors
{! beep, immortals only
{- tilde ~
{& reverse color, immortals only
{_ underline
```

Extended colors marked by DSL may not work in every MUD client unless `Color256` is enabled.

## Current prompt shape

Observed prompt shape:

```text
<74hp/74 126m/126 124mv/124 | WD | 17957tnl | 0g 1827s | Night Time>
```

## Best readable color prompt

Paste directly into DSL:

```text
prompt <{RHP {W%h/%H {w| {CM {W%m/%M {w| {GMV {W%v/%V {w| {Y%e {w| {M%Xtnl {w| {y%gg {W%ss {w| {C%d{x>
```

Color layout:

```text
HP     = light red
Mana   = light cyan
Moves  = light green
Exits  = light yellow
TNL    = light magenta
Gold   = yellow
Silver = light white
Time   = light cyan
```

Example shape:

```text
<HP 74/74 | M 126/126 | MV 124/124 | WD | 17957tnl | 0g 1827s | Night Time>
```

## Compact color prompt

Paste directly into DSL:

```text
prompt <{R%hhp/%H {C%mm/%M {G%vmv/%V {w| {Y%e {w| {M%Xtnl {w| {y%gg {W%ss {w| {C%d{x>
```

Example shape:

```text
<74hp/74 126m/126 124mv/124 | WD | 17957tnl | 0g 1827s | Night Time>
```

## Two-line color prompt

Paste directly into DSL:

```text
prompt {C%r {Y[%e]{x%c<{RHP {W%h/%H {w| {CM {W%m/%M {w| {GMV {W%v/%V {w| {M%Xtnl {w| {y%gg {W%ss {w| {C%d{x>
```

Example shape:

```text
Room Name [WD]
<HP 74/74 | M 126/126 | MV 124/124 | 17957tnl | 0g 1827s | Night Time>
```

## Color bleed warning

Always end the prompt with:

```text
{x
```

Without `{x`, future output and future prompts can inherit the last color.

## TinTin++ note

DSL uses literal braces like `{R` and `{x` for color. TinTin++ also uses braces for its own command syntax. For that reason, set the color prompt directly in DSL first. After it works, create a TinTin++ alias only if the braces are properly escaped for your client version.
