# LOOT ORGANIZER

This script organizers the loot on your backpack.

## Char Loot Pouch and Pouches Organizer

When first run, it will search for all your traped pouches and define 1 to use as the char loot pouch, and then organize all your traped pouches in the following way:

- It will set 1 pouch as the main loot pouch
- It will take the chosen loot pouch and hide it in another pouch
- It will then take that pouch and hide it within another pouch
- It will repeat nesting pouches like this until 4 pouches have been nested
- Then it will move all pouches to the top left corner of your loadout container (bag if char has one in backpack, otherwise its char's backpack)

This is intended to make your char almost immune to thiefs.
The thief would have to first find which pouch has all the nested pouches in it, and then pop another 4 pouches before finally getting to your loot pouch, hopefully giving you time to notice and just re-run the script to re-trap all the pouches again

The script will only try to re-organize the pouches again under the following conditions:

- Closing and reopening the client
- One of the previously saved traped pouches cant be found anymore (could be from ressuplying or loosing a pouch)
- You lost one of the pouches

## Hiding Valuables

After the pouches have already been organized, running the script again will do the following:

- Re-trap any of the saved pouches that have been poped
- Search and hide the following items in the loot pouch:
- Shepherds Crooks
- Skinning Knifes
- Valuables and rares (tmaps, aspect items, etc...)
- Print all items hidden in the loot pouch so you can keep track of whats in it
