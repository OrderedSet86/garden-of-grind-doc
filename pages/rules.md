# Rules + Setup

### Intro

There are multiple valid ways to play GoG. The main theme of all rulesets is limited world gen/dimension access and limited starter items.

See below for rulesets.

### Garden of Grind (GoG) (2024-)

--------------------------------------

Applies for new run starting May 3rd 2024! Thanks to `nzbasic` (Discord) for writing a mixin to remove world gen. The benefit of this new mixin is that it allows us to travel to other dims (yay no more OW skybox), and not be stuck with a single biome. **With these rules Stargate is possible!!**

1. **Ensure using a Hodgepodge version after this commit. (If you are on 2.6.1 or later version of GTNH, you can completely ignore this step)**
    - https://github.com/GTNewHorizons/Hodgepodge/pull/358
    - You can easily download the jar at this release tag https://github.com/nzbasic/Hodgepodge/releases/tag/Skygate
    - This removes world gen on a code level, allowing us to keep biomes and making modded dimensions empty
2. **Config changes. Make sure to launch the instance at least once to generate all configs!**
    - `GregTech/Worldgeneration.cfg`
        - Under `endasteroids`, set:
            - `B:generateEndAsteroids=false`
    - `hodgepodge.cfg`
        - Under the `tweaks` section, add the following three settings:
            - `B:disableChunkTerrainGeneration=true`
            - `B:disableWorldTypeChunkPopulation=true`
            - `B:disableModdedChunkPopulation=true` (Revert this to false when you're ready to find a chaos dragon. This allows the chaos island to generate for chaos shards.)
    - `Natura.cfg`
        - Under `disabler`, set:
            - `B:"Generate Ash Clouds"=false`
            - `B:"Generate Dark Clouds"=false`
            - `B:"Generate Overworld Clouds"=false`
            - `B:"Generate Sulfur Clouds"=false`
            - `B:"Generate Thornvines"=false`
    - `Thaumcraft.cfg`
        - Under `world_generation`, set:
            - `B:generate_aura_nodes=false`
            - `B:generate_structures=false`
    - `TinkersConstruct.cfg`
        - Under `dimblacklist`, set:
            - `B:slimeIslGenDim0=false`
    - `witchery.cfg`
        - Under `general`, set:
            - `B:GenerateCovens=false`
            - `B:GenerateHobgoblinHuts=false`
            - `B:GenerateShacks=false`
            - `B:GenerateWickerMen=false`
            - `B:GenerateWitchHuts=false`
        - Make sure you leave `B:GenerateApothecaries=true`. Apothecary villagers don’t spawn if this is false, which prevents clay trade for bypassing RC tank.
3. **Generate world normally**
    - You don't have to turn "generate structures" off!
4. **Questbook allowed**
    - You need this for bee start:
        - For bee start, make a scoop and get bee coins. You can use these to trade for two hives. If the hives do not drop a princess and a drone (needed for the next step of QB bees), reset to a backup. After you clear the princess/drone boundary, breed carefully (make sure production is never above 16) until you can get another source of princesses, such as the alveary swarmer or hiveacynth. The Hiveacynth, is required for questbook-locked bees, since to unlock the trade, you need to visit the end, which is behind one of these bees. 
    
#### Optional Rules. You do not have to follow these if you decide not to. Some of these are flawed.

This is just what we did for GotG run. We modified some rules further to increase difficulty.

5. **Opening questbook lootbags is banned.**
6. **Non-OW dimensions may be used only for questbook progression (This was a flawed rule as several dimensions are required for progression.)**
    - Anything that relies on the dim to do something not possible in the same tier at OW is banned, including but not limited to:
        - Bee breeding (nether dimensions, hellish, space bees)
        - Mob farming (kobold farming in TF)
        - Dragon's Breath from Ender Dragon in end dimension (OW Ender Dragon is fine and required progression)
    - This rule has become flawed for a second time with 2.8, as skips exist for both the twilight forest and nether quests. No other dimension quests block progression.
7. **Use questbook to get flawless diamond**
    - As a result of our earlier rule, we cannot breed Diamond bee until much later (EV+ biome change) as we require a nether biome. But flawless diamond is required to enter HV. So we are allowed to do the Questbook trade for diamond ore, which lets us make the MV lathe for HV circuit progression.
    - (NOTE: We collected all questbook rewards anyway (except lootbags), so this isn't really a new allowance for us, just noting it for min questbook runs that also ban non-OW dims.)
8. **Exceptions to rule 6**
    - Convocation of the Damned is blacklisted from working in the OW, so we are allowed to do it in another dimension.
    - To get Barnarda C Sapling, you need to first breed the Treetwister trait onto a bee and then apply it to a sapling in a "magically active dimension" which right now means Spectre, Bedrock, Last Millenium, or Pocket Plane dimensions.
    - Since Chaos Crystal is needed for stargate, you are allowed to travel to the end and kill the Chaos Dragon for Chaos Crystals. Due to earlier config it should be the only thing that generates in the end.
    - The Deep Dark is the sole way to acquire Dark Iron, a progression-blocking material.
    - The Nether is now required for the Netherite line, which requires Nether Air, sourced solely from the Nether using air intake hatches.
9. **OW void rules**
    - For our run, we banned overworld void pumping (as this makes oil trivial), but allowed overworld void mining (LUV+).
10. **Savescumming is allowed**
    - Do RNG task, check outcome, restore backup if failed
11. **difficulty=hard**
    - This is recommended regardless, as it increases the Thaumcraft Champion chance from 1% on normal to 3%. This chance can go further to 5% if the spawned mob is within a 'spooky' biome. (Biome tags can be found on the biomes page on the GTNH wiki)
12. **Worldedit is allowed**
    - We initially tried to do Schematica only, as this takes from player inventory, but it doesn't support microblocks. This was burning out our builders so we voted that it would be allowed.
    - Note that normal stargate rules allow Worldedit for cosmetic purposes: https://docs.google.com/document/d/1Iww1FNLkCuun6s6LW7Q6_1Z1aldtxYeRxYOeq_P-vK8/edit
13. **Pollution off**

### Manual Garden of Grind (MGoG) (2022-2024)

--------------------------------------

1. **Update config files to remove structures**
    - `witchery.cfg`
        - `B:GenerateApothecaries=true` (apothecary villagers don’t spawn if this is false, which prevents clay trade for bypassing RC tank. doesn’t do world gen without villages, which are disabled)
        - `B:GenerateBookShops=false`
        - `B:GenerateCovens=false`
        - `B:GenerateHobgoblinHuts=false`
        - `B:GenerateShacks=false`
        - `B:GenerateWickerMen=false`
        - `B:GenerateWitchHuts=false`
    - `Thaumcraft.cfg`
        - `B:generate_aura_nodes=false`
        - `B:generate_structures=false`
2. **Delete defaultworldgenerator mod** (this lets you select superflat worldgen config in game)
    - If you’re on a server, you can just directly modify **generator-settings** when making a world.
3. **Generate superflat world with config 2;0;68;**
    - This generates a completely empty world with the “Grassland” biome
    - The IC2 crop and RC humidity stats are fairly high here while still being normal/normal for bee progression. You can pick a different biome to make it harder for yourself if you want, but the run is already hard enough as is 🙂
    - Note that “Grassland” counts as “Plains” for the purposes of Rural bee
4. **Dimension: overworld**
5. **No going to dims outside overworld. This means no rockets, TF, etc.**
5. **difficulty=hard**
    - This is recommended regardless, as it increases the Thaumcraft champion spawn chance from 1% to 3%.
7. **Questbook allowed**
    - You need this for three items and bee start:
    - Silverwood + greatwood sapling (used for certain crafting recipes in Thaumcraft; there’s a coin trade)
    - Flawless diamond (needed to make MV lathe for circuit progression)
    - For bee start, make a scoop and get bee coins. You can use these to trade for two hives. If the hives do not drop a princess and a drone (needed for the next step of QB bees), reset to a backup. After you clear the princess/drone boundary, breed carefully (eg gentle frames) until you can get to alveary swarmer, which lets you generate new ignobles. After this, work towards Botania Hiveacynth, which will unlock new bees for you.
8. **No using bugs (eg disassembler) for obtaining resources**
    - Previously we used cupronickel coil disassembly to get mica, but there are viable methods to avoid this now.


### Original Skyblock Run (2021-2022)

--------------------------------------

https://docs.google.com/document/d/1Ajmpajbpw8H9rOpiPgX6AcUOcpdIfArwb-aoVrKly4I/edit

### Other run types

--------------------------------------

1. Nether only run (Dim-locked challenges are inherently impossible, as you need access to the End, a magic dimension, the Deep Dark, and, starting in 2.8, the Nether. There are currently no alternative acquisition methods for their dimension-specific resources. Barring the exceptions, a Nether only run is quite fun.)
2. No rocket (we share a lot of progression with the traditional no-rocket run)
3. Peaceful (you may have to spawn in some items to bypass mob gates, like the first nether star)
4. Other-dim starts. (While other dimensions are required for progression, starting in another prevents you from having to make said exceptions. In order of ease of difficulty, there are the Ross start, Nether start, End start, Nether void start (but not all dimensions void), End void start (It's harder than Nether void as the only hostiles are creepers and enderman, so no zombies/pigmen for a villager), and Mars start (you can get oxygen gear from killing mobs, and water is present in ice. I recommend giving yourself starting gear and going from there)) 
