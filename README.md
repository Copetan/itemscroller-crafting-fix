## Note
This is a customized version of Masa's itemscroller mod that fixes crafting features for 1.17.1. Masa's original mod can be found [here](https://github.com/maruohon/itemscroller)

Customizations:
* More accurate/faster crafting through recipe book protocol
* Toggleable crafting (so you can keep crafting without holding down a key, eg for crafting millions of pistons)
* Honey crafting

- Removed carpetControlQ crafting option as it causes a "slow crafting issue"
- Removed packetRateLimit as it may lead to problems.

## This is not Masa's original itemscroller. If you have issues with this mod, please contact Andrews54757 (or open a bug report here).

### What's different?
Post 1.13, Mojang has changed the crafting mechanics of the game. Before 1.13, crafting was very fast as much of the logic was handled client-side. In 1.13, most of the crafting logic was moved to the server. This broke Itemscroller's fast crafting features, since every ingredient now had to be moved one slot at a time to the crafting grid for it to work. This drastically worsened server-client desync, a compounding problem, leading to an increasing number of failed crafting attempts and accidental ingredient leaks which made afk crafting impossible. 

This customized version of the mod, fixes the problem by handling ingredient movement server-side using the recipe book protocols when it can. 

**Note: Some recipes like fireworks rockets that are not in the recipe book do not take advantage of this protocol, in those cases old itemscroller methods will be used**

Item Scroller
==============
Item Scroller is a tiny mod for Minecraft 1.8.9+, which adds the functionality of moving items in inventory GUIs
by scrolling the mouse wheel over slots with items in them.
This is basically what NEI does/did (and Mouse Tweaks also seems to do), but separated into this tiny mod,
and probably implemented in a different manner.
For more information and the downloads (compiled builds), see http://minecraft.curseforge.com/projects/item-scroller

Compiling
=========
* Clone the repository
* Open a command prompt/terminal to the repository directory
* run 'gradlew build'
* The built jar file will be in build/libs/
