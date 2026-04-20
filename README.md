# Recipedia - Paper Mario Recipe Checker

[Link](https://josephrooks.github.io/Recipedia/)

A tool for tracking cooking progress toward the [Kitchen Nightmare](https://retroachievements.org/achievement/79593) RetroAchievements achievement in Paper Mario (N64).

The correspondence between flag bit positions and specific recipe names was established by cross-referencing known-cooked save states against the item ID sequence, then verified by diffing save states before and after cooking individual recipes.

Not all 50 recipes required for the achievement have been explicitly confirmed yet, but the pattern has held for every recipe tested individually.

### Notes

- Compatible with the Kitchen Nightmare achievement as of the February 21, 2026 edit
- Save states only; `.srm` "battery save" files are not supported (recipe data only exists in active memory, not in the save file)
- You can create save states while RetroAchievements Hardcore Mode is on; you just cannot load them in Hardcore Mode
- Confirmed working with save states from MupenPlusNext on RetroArch; if you have save states from another emulator and want to help test compatibility, feel free to open an issue

---

## Web version

[Link](https://josephrooks.github.io/Recipedia/)

Upload a RetroArch save state and see exactly which of Tayce T.'s 50 recipes you have and haven't cooked. No data is uploaded from your computer.

You can also save the HTML file locally and it _should_ work fine.

### View modes

- **Chapter** - shows the earliest chapter each recipe becomes cookable, with optimized ingredient routes for completing the achievement as efficiently as possible
- **Single / Two** - groups recipes by ingredient count, alphabetically within each group
- **ID Order** - follows the game's internal item ID sequence (the order the achievement tracks them)
- **Shopping List** - shows a consolidated list of every ingredient needed for whichever recipes you have checked, with where to find or buy each one

### Shopping List

Each recipe card has a checkbox in the top-right corner. Check any recipes you still need to cook and then switch to Shopping List view to see every ingredient those recipes require, deduplicated and sorted alphabetically. If multiple checked recipes share an ingredient, the count appears in parentheses after the ingredient name (e.g. **Cake Mix (4)**). Each ingredient entry also shows where to find or purchase it.

The Shopping List is session-only and does not persist on reload. It works independently of your save state - you can use it with or without uploading a state, and you can check recipes regardless of whether they show as cooked or not.

### How to use

1. In RetroArch with Paper Mario running and the save file you want to check loaded, open **Quick Menu → Save State** (or press your hotkey).
2. Find the `.stateN` file in your `states/` folder and upload it to the tool.
3. Choose a view mode and filter to see your progress.
4. Check the box on any recipe card to add it to your Shopping List.

---

## Credits

**Flag data** from [Paper Mario Code Notes](https://retroachievements.org/codenotes.php?g=10154) on RetroAchievements.

**Item ID sequence** (the internal ordering used to map recipe flags to recipe names) from the [RPGClassics Paper Mario Hacking Guide](http://shrines.rpgclassics.com/n64/papermario/hacking.shtml).

**Chapter route** - the chapter mode ordering and optimized ingredient routes were posted by [Renia](https://retroachievements.org/achievement/79593/comments) on the Kitchen Nightmare achievement wall.

**Ingredient data** from the [RPGClassics Cooking Guide](http://shrines.rpgclassics.com/n64/papermario/cooking.shtml) and the [MarioWiki recipe list](https://www.mariowiki.com/List_of_recipes_in_Paper_Mario).