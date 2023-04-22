**LOOT DROPOFF v1.5.0**

This script will execute the following actions, in the following order:

```md
1. Try to detect thiefs (optional)
2. Unload misc items: skill orbs, RMs, spell hue deeds...)
3. Drop the following items in their respective Tomes:
   - Links
   - Ship Upgrades
   - Treasure Maps
   - All Resource Maps
   - All Aspect Items
   - Skill Scrolls
   - Rare Cloths
   - All Types Of Dyes
   - Arcane Runes
   - Magery Scrolls
     NOTE: aspect items like focis, oils and bundles will be unloaded to tome only if full, and to a general container if not)
4. Use a repair bench if there is one nearby
5. Deposit gold and doublons from char and all pack animals
6. Smelt and unload all ores from char and packies
7. Make boards and unload logs from char and packies
8. Restock Storage Shelf from char and all packies
9. Restock Resource Stockpile from char and all packies
10. Restock Garden Shelf from char
11. Dump magic items in Recycler
12. Pull following items back from recycler (if recycler_mode == 0):
    - barding instruments (magic props controled by a editable list)
    - hatchets
    - pickaxes
    - shields
13. Dump completed tmaps on trashcan or ground
14. Shelf Ressuply
15. Print all unloaded items (optional)
```

**USING THE SCRIPT**

The script defaults is intended for using with all shelfs and tomes secured/locked down in the ground within 2 tiles of the char.

Every time the script runs, it will auto search for stuff like shelf, stockpile, deposit box, tomes and save them for use.
If it cant find something, the script will ask you to set it.
After setting something, it will only ask you to set it again if you run the script from more than 2 tiles from what was set.

If your tomes are not in the ground, but inside a container, the script will notice it cant find any tomes on ground and ask you for which container it should look for your tomes.

The NON TOME ITEMS the script refers to was the best name i could find for any item that dont have a tome for it, like Skill Balls, Battle Commodities, Research Mats and such. The script will also ask you to set a container for them at first run or whenever it cant find the one previously set.

**CHANGES v1.5.0**

```md
- Uses new 'Adds all from backpack' option on all tomes
- Only dump focis, oils and bundles into misc container if they are not fully charged or no aspect tome nearby
- Adds check on deposit safe for 'locked in' money, that was droped inside by scripting bug, and takes it out
- Adds while loop to force target generation on recycler dump items button when recycler gump is already open (gump has a bug where first click wont open target)
- Simplifies a little logic behind getting bard instrument back from recycler and closing recycler gump
- Improves shelf re-use throughout scripts and removes related setvars (improves performance a bit)
- Moves garden shelf restock to before stockpile restock so plant chemicals go into garden shelf first
- Fix bug where script would only move 1 stack of misc items of the same type and leave other stacks
- Adds suport to restock shelf using a container (bag/pouch/backpack) instead of using 'self'
- Switches list configs to non-persistent variables (simplifies code maintenance and greatly improve performance)
```
