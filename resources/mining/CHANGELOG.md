# CHANGELOG

## v5.0.0

- Removes all walk implementations and references from script after razor `walk` command was disabled lol

## v4.0.0

- Implements automatic rail system
- Splits script configuration into its own separate file
- Switch most for loops to `findtype` shorthand piped argments notation (eg: `if findtype 0000|1111`)
- Several bugfixes

## v0.3.2

- Script now recalls home when cant find pickaxes to equip

## v0.3.1

- Disables autounload to free weigth before recalling home until i find a fix for it

## v0.3.0

- Opens regs bag when starting to make sure razor will detect pots and regs inside loadout bag
- Switches bandage timers for the new 'bandaging' command
- Updates packies weight check to conform to new material weight changes

## v0.2.1

- Adds gump serial to gumpresponse command on recall routine
- Adds Archery to supported weapon skills when defending against monsters
- Fix bug where script would keep trying to smelt packies ores, even if char got far from forge
- Fix bug where char would enter defense routine even without monsters nearby
- Adds missing gump serial to tracking gumpresponse and gumpclose calls
- Script now closes the tracking gump after Starting Hunting
- Script will now rename packies according to their weight status: 'full packie' and 'light packie', to make it easier to track which one is full or not
- Add weigth check on each packie unloading so char doenst try to iterate thought all packies even after completely unloaded
- Improves weight check logic to determine when packie is heavy
- Fix bandage delay reseting when full restoring hp while atacking mobs

## v0.2.0

- Switches from list configs back to variables using setvar!
- Script should now do ore maps as well when finding ore maps in backpack
- Temporary fix for the "removing from full packies list" bug that happened when a packie got full and then was unloaded, which would make script stop working
- Adds outpost forge position to smelt after recalling routine for players that dont have a house and use the outpost forge when escaping PKs/recalling

## v0.1.4-rc1

- Fix sysmsg that was mistakenly assuming char got iron instead of shadow iron (tkx GCinco!)
- Makes 'go home and unload' routine reusable and triggered in different parts of the script
- Tries to detect when all packies are heavy and takes char home and unload

## v0.1.3

- Fixed bug where char would keep equipping all combat weaopns found in backpack while fightning mobs
- Added some missing lists that were causing script to crash while fighting mobs
- Added startup warnings about script requirements

## v0.1.2

- Fixes bug where char would constantly use bandages when finding multiple mobs to kill

## v0.1.1

- Check for ores in char or packies before starting smelting routine
- addresses grab bug when ore fell on ground

## v0.1.0

- Adds more checks of ore and ingots on packie to determine if its heavy
- Improves combat and weapon equipping logic to fight monsters
- Fix bug where char would count ingots from its backpack while checking packies weight (tkx @Guga#1138 for noticing!)
- Fix some calls to wrong variable name (tkx @daniel\_#6593 for noticing!)

## v0.0.9

- Fixes error happening on chars without healing due to script trying to access a variable that is only created on chars with healing (tkx to @BaLLa#7588 for finding and reporting it)

## v0.0.8

- Makes char undress pickaxe to fight monsters with appropriate combat weapon
- Fixes error when char tried to heal himself when attacked
- Handles 'You have worn out your tool' sysmsgs
- Fixed blue chars not finding packies (tkx to @renatoestevao#8568 for subimitting a PR)

## v0.0.7

- Adds missing variables containing rune positions in runetome and runebook

## v0.0.6

- Adds survival routine to defend char against closed-ranged combat creatures
- Adds sysmsg check to see if char got far from forge while inside the smelting loop

## v0.0.5

- Stops double clicking packie to open packpack when unloading ores while heavy
- Adds wait timer after recalling and before unloading when getting home

## v0.0.4

- Adds setting to choose if script will auto smelt ores when close to forge

## v0.0.3

- Makes sysmsgs checks even when gump is detected (so char can escape PKs even when answering gumps)

## v0.0.2

- Adds checks for several map-forges around the world
- Adds option to not smelt colored ores (makes it hard for PKS to take them)

## v0.0.1

- Initial release
