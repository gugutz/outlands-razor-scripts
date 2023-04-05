**setup tailoring societies v0.0.2**

This script will:

- Open the **Order of Armorers** society gump
- Search for all societies present in the gump
- Open the tailoring crafting gump (by either stockpile or sewing kit in backpack)
- Add all societies job items into the crafting queue

It doenst setup everything for you, it only simplifies the process by adding the items to the crafting queue so you only need to set the quality and quantities afterwards.

**CAVEATS**

- **You have to start the macro with the material color set to regular leather!**
  I cant read the tailoring gump text due to a bug in razor so the script changes material color literally by clicking the switch material buttons a specific X number of times, so if a save happens in between clicks the material color will be set wrong.
  If a world save happens while the script is running it will mess things up and you will have to replay it.

- **If there are colored material items in the societies, both the colored and the regular color version of that job item will be added to queue.**
  Example: **Craft 75 Avarhide Leather Cap** contains the term `Leather Cap` in it, so both script checks for `Avarhide Leather Cap` and `Leather Cap` will match and both will be added to queue.
  So after each execution, there is a need to 'clean' the crafting queue of the 'duplicated' regular colored job items.
  I could make the script skip the regular color check of an item if it already added a colored version of it, but i figured its easier to remove wrong jobs from the queue than having to add skiped jobs manually (in case both colors are actually present in the society gump).

  Been testing it for a few weeks and its been helpful so i thought i'd share, but beware its still subject to bugs.
