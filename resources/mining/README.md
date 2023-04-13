# MINING BOT by gugutz

## Requirements

```md
- First run far from other friends pack animals
- Uncheck option 'filter repeating system messages' on razor
- Uncheck option 'Auto Stack Ore/Fish/Logs at feet' on razor
```

## COOLDOWNS

This script needs cooldowns set up in the client in order to work
You can download the **cooldowns.xml** file at the root of my repo with all the cooldowns set up.

The main cooldown is the 'RESOURCES' cooldown

ADD THESE TRIGGERS TO THE COOLDOWN:
Type: sysmsg | Text: you dig some
Type: sysmsg | Text: You have recently traveled
Type: sysmsg | Text: You have worn out your tool
Type: sysmsg | Text: The world is saving
Type: sysmsg | Text: You do not see any harvestable resources nearby
Type: sysmsg | Text: loosen some rocks but fail
Type: sysmsg | Text: You must wait to perform another action
Type: sysmsg | Text: Harvesting is not allowed in this area

## HOW TO USE THE RAIL SYSTEM

This script supports rails. To use it you must enable `auto_rail` to `1` in the script settings, and then record a rail for each rune you intend to use from your runetome.

You record rails with regular razor macros, and then convert the macro to razor list format using (Razor2Rail)[https://github.com/malbolger/Razor2Rail]

After recording each rail, go to the last line of each rail file and change the `script` command parameter to where the mining script is:

From:
`script 'M_Harvester'`

To:
`script 'resources\mining\mining'`

Then move the rail file into the same folder as the mining script (in the above exemple: 'resources\mining')

## Features

**_Movement Types_**

```md
- Auto rails.
- Auto walk randomly (default: off)
- Auto walk to specific diretion (default: off)
```

**_Packies Features_**

```md
- Auto finds all char packies and use them to unload.
- Auto names packies according to weight ('emptypackie', 'lightpackie', 'fullpackie')
- Detects when a packie is heavy and skips to next packie in list
```

**_Other Features_**

```md
- Tries to detects AFK Captchas and awaits for user input before continuing
- Auto turns on tracking on start if not already Hunting
- Auto re-equips pickaxe whenever needed
- Informs what color ore is being gathered
- Auto grabs ores found on ground
- Auto travel home to escape PKs
- Auto travel home when all packies are full
- Configurable rune position to auto travel (runetome or runebook)
- Auto use recall charges to travel if char doenst have magery
- Monitors and maintain char health (cure poison, heal pots, bandages, mage heals...)
- Autoheals with best skills available (pot > bandage (with timer) > mageheals)
- Auto smelt ores when: (default: on)
  - Within 2 tiles of player forges
  - Close to some hardcoded map forges locations
- Option to not smelt colored ores (PKs cant smelt colored ores so makes it hard for them to take em)
- Fights mobs in scenario (auto equips best weapon based on char weapon skill)
- Waits world saves
- Detects when char is resource locked (by failing a previous captcha) and stops script
```
