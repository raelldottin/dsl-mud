# DSL area index

Captured from the DSL `areas` listing pasted on **2026-07-07**.

Raw capture:

```text
data/raw/areas-2026-07-07.txt
```

Parsed area entries: **416**

## Region counts

| Region | Areas |
| --- | ---: |
| Limbo | 43 |
| Althainia | 130 |
| Arkania | 92 |
| Icewall | 59 |
| Tropica | 30 |
| Ships | 6 |
| Neocean | 3 |
| Nwocean | 2 |
| Seocean | 12 |
| Swocean | 7 |
| Ctrocean | 2 |
| Shokono | 25 |
| Nocean | 2 |
| Socean | 3 |
| Underworld | 0 |

## Level 5 planning for Yttawstp

Yttawstp is level 5, so these are areas where the listed range includes level 5 and the range is not `[0 0]`.

- Level-5-accessible entries parsed: **175**
- Tight beginner entries with max level 15 or lower: **44**
- Nearby low-level entries with max level 16-25: **7**

### Tight beginner ranges

| Region | Min | Max | Qt | Area | Builder |
| --- | ---: | ---: | ---: | --- | --- |
| Althainia | 1 | 5 | 0 | Faerie Forest | Tashio |
| Althainia | 1 | 5 | 0 | Machine Dreams | Furey |
| Althainia | 1 | 5 | 0 | Squatter Village | Taltos |
| Arkania | 1 | 5 | 0 | Orchard | Calzam Nazca |
| Arkania | 1 | 5 | 0 | Woodland Village | Laika |
| Limbo | 1 | 5 | 0 | New Mudschool | Kyri |
| Limbo | 1 | 5 | 0 | The Academy | Scorn Solum |
| Tropica | 1 | 5 | 0 | Tropica Trails | Joules |
| Althainia | 1 | 10 | 0 | Lower Dwarven Kingdom | Xiola |
| Althainia | 1 | 10 | 0 | Shalonesti Guardhouse | Taidra |
| Althainia | 1 | 10 | 0 | The Halls of Glory | Volodya |
| Althainia | 1 | 10 | 0 | Uxjukopoap Tunnels | Beliya'al |
| Icewall | 1 | 10 | 0 | The Ice Caverns | Solum |
| Althainia | 1 | 15 | 0 | Coalthen Farms | Kyri |
| Althainia | 1 | 15 | 0 | Dwarven Training Camp | Taidra |
| Althainia | 1 | 15 | 0 | Kingdom of Aghar | Kyri |
| Althainia | 1 | 15 | 0 | The Garrison | Kyri |
| Althainia | 1 | 15 | 0 | The Stony Barrens | Volodya |
| Arkania | 1 | 15 | 0 | Mired Banks | Dekaios |
| Arkania | 1 | 15 | 0 | Old Lanstone Village | Cayenna |
| Icewall | 1 | 15 | 0 | The Bre Amaethdai | Jaehea |
| Icewall | 1 | 15 | 0 | The Ice Crystal Caverns | Nazca |
| Icewall | 1 | 15 | 0 | Yinn Encampment | Zypher |
| Shokono | 3 | 7 | 0 | The Shonoko Coast | Jubbie |
| Althainia | 3 | 10 | 0 | Thaxanos Upper Mines | Laika |
| Icewall | 4 | 8 | 0 | The Lost Cave | Istiak |
| Althainia | 5 | 10 | 0 | Graveyard | Alfa |
| Althainia | 5 | 10 | 0 | Haon Dor | Diku Joules |
| Althainia | 5 | 10 | 0 | In the Air | Copper |
| Althainia | 5 | 10 | 0 | Mount Axpvjib | Laika Joules |
| Seocean | 5 | 10 | 0 | The Caverns | Tashio |
| Shokono | 5 | 10 | 0 | Misty Woods | Calzam |
| Shokono | 5 | 10 | 0 | The Spirit Gardens | Syrestina Tetsuko |
| Shokono | 5 | 10 | 0 | Tokaido | Astinus Laika |
| Tropica | 5 | 10 | 0 | The Rainforest | Laika |
| Althainia | 5 | 15 | 0 | Miden'nir | Copper Kanoir |
| Althainia | 5 | 15 | 0 | Moria | Alfa Laika |
| Althainia | 5 | 15 | 0 | The Sub-Issue Gladiator A | Raff Joules Calzam |
| Althainia | 5 | 15 | 0 | University of Althainia | Scorn |
| Arkania | 5 | 15 | 0 | Gnome Village | Vougon |
| Arkania | 5 | 15 | 0 | The Farmstead | Cahlizna |
| Arkania | 5 | 15 | 0 | The Training Ground | Joules |
| Arkania | 5 | 15 | 0 | Verminasia Bastille | Cahlizna |
| Icewall | 5 | 15 | 0 | Highland Trails | Laika |

### Nearby low-level ranges

| Region | Min | Max | Qt | Area | Builder |
| --- | ---: | ---: | ---: | --- | --- |
| Althainia | 1 | 20 | 0 | Plains | Copper |
| Arkania | 1 | 25 | 0 | Arkane Sewers | Kanoir Desmothius |
| Althainia | 5 | 20 | 0 | Arachnos | Mahatma Joules |
| Althainia | 5 | 20 | 0 | Holy Grove | Alfa |
| Althainia | 5 | 20 | 0 | Valley of the Elves | Hatchet |
| Arkania | 5 | 20 | 0 | Glassrose Mansion | Joules |
| Nwocean | 5 | 25 | 0 | Prismatic Reef | Xiangzhi |

## Notes

- Level ranges are recorded exactly from the DSL listing.
- `[0 0]` entries were treated as special/nonstandard entries rather than normal leveling areas.
- Some names are truncated because the source table truncates columns.
- `Qt` is `0` for all parsed entries except `The Hall of Costs`, which showed `Qt` as `1`.
