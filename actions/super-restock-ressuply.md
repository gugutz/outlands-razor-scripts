**super-restock-ressuply v1.5.0**

**CHANGES v1.5.0**

```md
- Uses new 'Adds all from backpack' option on all tomes
- Only dump focis, oils and bundles into misc container if they are not fully charges or cant find a aspect items tome
- Adds check on deposit safe for 'locked in' money, that was droped inside by scripting bug, and takes it out
- Adds while loop to force target generation on recycler dump items button when recycler gump is already open (gump has a bug where first click wont open target)
- Simplifies a little logic behind getting bard instrument back from recycler and closing recycler gump
- Improves shelf re-use throughout scripts and removes related setvars (improves performance a bit)
- Moves garden shelf restock to before stockpile restock so plant chemicals go into garden shelf first
- Fix bug where script would only move 1 stack of misc items of the same type and leave other stacks
- Adds suport to restock shelf using a container (bag/pouch/backpack) instead of using 'self'
- Switches list configs to non-persistent variables (simplifies code maintenance and greatly improve performance)
```

This script will execute the following actions, in the following order:

```md
1. Use Detect Hidden (default: off)
2. Unload misc items: skill orbs, RMs, spell hue deeds...)
3. Drop the following items in their respective Tomes:
   - Links
   - Treasure Maps
   - All Resource Maps
   - All Aspect Items
   - Skill Scrolls
   - Rare Cloths
   - All Types Of Dyes
   - Arcane Runes
   - Magery Scrolls
4. Use a repair bench if there is one nearby
5. Deposit gold and doublons from char and all pack animals
6. Smelt all ores in pack animals
7. Make boards from logs in pack animals
8. Restock Storage Shelf from char and all packies
9. Restock Resource Stockpile from char and all packies
10. Restock Garden Shelf from char
11. Dump magic items in Recycler
12. Pull following items back from recycler
    - barding instruments (magic props controled by a editable list)
    - hatchets
    - pickaxes
13. Dump completed tmaps on trashcan or ground
14. Shelf Ressuply
```

**SETUPS**

**Ground Setup (Default/Recommended Setup)**

All shelfs and tomes secured/locked down in the ground within 2 tiles of the char.

**Custom Setup**

You can change where the script will search for tomes/unload containers by changing the following options:

- **unload_misc_items_container_location**
- **gold_container_location**
- **tomes_location**

The possible values for the above options are:

- `ground`: if unload destination (tome/container) is located directly in the ground
- `subcontainer`: if should unload to a subcontainer inside the `Master Unload Container`
- `master_container`: if should unload inside the `Master Unload Container`
- `ground_container` (TOMES ONLY!): if tomes are inside their own container in the ground

If you use **master container** or **subcontainer** in any option, the script will ask you once for the **Master Unload Container**.
On first run it should also ask for the Misc Items container

The script will only ask you to select any container again if its not within 2 tiles.

**OTHER SCRIPT SETTINGS:**

- **verbose_mode**
  Toggle informative msgs
- **unload_misc_items**
  If should also unload misc items (skill orbs, RMs...)
- **action_delay**
  Delay for all actions (default 350ms)
- **sysmsgs_color**
  Color for all sysmsgs
