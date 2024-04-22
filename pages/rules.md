# Rules + Setup

### Intro

There are multiple valid ways to play GoG. The main theme of all rulesets is limited world gen/dimension access and limited starter items.

See below for rulesets.

### Manual Garden of Grind (2022-2024)
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
6. **Questbook allowed**
    - You need this for three items and bee start:
    - Silverwood + greatwood sapling (used for certain crafting recipes in Thaumcraft; there’s a coin trade)
    - Flawless diamond (needed to make MV lathe for circuit progression)
    - For bee start, make a scoop and get bee coins. You can use these to trade for two hives. If the hives do not drop a princess and a drone (needed for the next step of QB bees), reset to a backup. After you clear the princess/drone boundary, breed carefully (eg gentle frames) until you can get to alveary swarmer, which lets you generate new ignobles. After this, work towards Botania Hiveacynth, which will unlock new bees for you.
7. **No using bugs (eg disassembler) for obtaining resources**
    - Previously we used cupronickel coil disassembly to get mica, but there are viable methods to avoid this now.


### Gates of the Garden (2024-)

This ruleset is still in progress, intended for new GoG community run starting May 1st 2024. Subject to change until that date.

1. **Ensure using a Hodgepodge version after this commit**
    - https://github.com/GTNewHorizons/Hodgepodge/pull/358
    - This removes world gen on a code level, allowing us to keep biomes and making modded dimensions empty
2. **Config changes**
    - `hodgepodge.cfg`
        - `disableChunkTerrainGeneration=true`
        - `disableWorldTypeChunkPopulation=true`
        - don't change `disableModdedChunkPopulation` - we use this to access chaos shards late game
3. **Generate world normally**
4. **Questbook allowed**
    - You need this for three items and bee start:
    - Silverwood + greatwood sapling (used for certain crafting recipes in Thaumcraft; there’s a coin trade)
    - Flawless diamond (needed to make MV lathe for circuit progression)
    - For bee start, make a scoop and get bee coins. You can use these to trade for two hives. If the hives do not drop a princess and a drone (needed for the next step of QB bees), reset to a backup. After you clear the princess/drone boundary, breed carefully (eg gentle frames) until you can get to alveary swarmer, which lets you generate new ignobles. After this, work towards Botania Hiveacynth, which will unlock new bees for you.
5. **No collecting progression resources from non-OW dims**
    - In other words, non-OW void mining is disallowed, and anything else that relies on that dim - eg kobold hollow hill farming in TF.
    - You can use other dims to progress in QB.
    - Feel free to break this rule for your own run, this is just what we did for GotG run.
6. **difficulty=hard**

### Other run types
1. Nether roof / nether only run
2. No rocket (we share a lot of progression with the traditional no-rocket run)
3. Peaceful (you may have to spawn in some items to bypass mob gates, like the first nether star)
