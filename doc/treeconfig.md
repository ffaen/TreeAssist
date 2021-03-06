# Tree Configuration File

This is the default tree configuration file.

    Automatic Destruction:
      # Main switch to deactivate automatic destruction
      Active: true
      Apply Full Tool Damage: true
      Auto Add To Inventory: false
      Cooldown Seconds: 0
      # Seconds to wait before (force) removing remnants of the tree
      Cleanup Delay Seconds: 20
      # Ticks to wait before breaking the next block, set to -1 for instant breaking
      Delay Ticks: 0
      # Always remove remnants of the tree, as soon as a tree has been verified and is being broken
      Forced Removal: false
      # Main switch for the Block Statistic nodes
      Increases Statistics: false
      # Should we wait before we kill the tree?
      Initial Delay: false
      Initial Delay Seconds: 10
      Remove Leaves: true
      # Required lore on tool in order to automatically remove a tree
      Required Lore: ''
      # Tools are set in the tree definitions or via command
      Requires Tools: true
      # Here you can restrict whether automation only happens when sneaking or not sneaking
      When Sneaking: true
      When Not Sneaking: true
    Block Statistics:
      Mine Block: false
      Pickup: false
    # Careful messing with this one, the tree extra blocks definition!
    Blocks:
      # How many leaves do require expect?
      Required: 10
      # Do we generate custom drops?
      Custom Drops: true
      # Branch caps, how high do leaves go, and how far out?
      Cap:
        Height: 2
        Radius: 3
      # Here you can add extra blocks to be expected inside or around tree leaves
      Materials:
      - 'minecraft:bee_nest'
      # How far out do leaves go
      Middle:
        Air: false
        Edges: false
        Radius: 2
      # How does the tree top look like?
      Top:
        Air: false
        Edges: false
        Radius: 3
        Height: 3
    # These drop chances are factors. 1.0 would be 100% chance!
    Custom Drops:
      minecraft:apple: 0.01
      minecraft:golden_apple: 0.001
    # These are additional factors, for example, by default, iron has half the chance to get custom drops
    Custom Drop Factor:
      minecraft:diamond_axe: 1.0
      minecraft:golden_axe: 0.75
      minecraft:iron_axe: 0.5
      minecraft:stone_axe: 0.25
      minecraft:wooden_axe: 0.1
    # Valid blocks that are below and around the saplings
    Ground Blocks:
    - 'minecraft:podzol'
    - 'minecraft:mycelium'
    - 'minecraft:grass_block'
    - 'minecraft:dirt'
    - 'minecraft:coarse_dirt'
    - 'minecraft:sand'
    # Blocks that you can expect to be around the tree - these are exceptions to look for player buildings intersecting
    Natural Blocks:
    - 'minecraft:air'
    - 'minecraft:water'
    - 'minecraft:fire'
    - 'minecraft:snow'
    - 'minecraft:snow_block'
    - 'minecraft:stone'
    - 'minecraft:grass_block'
    - 'minecraft:dirt'
    - 'minecraft:coarse_dirt'
    - 'minecraft:sand'
    - 'minecraft:terracotta'
    - '*_terracotta'           # this will add all materials ending in '_terracotta'
    - 'minecraft:mycelium'
    - 'minecraft:podzol'
    - '*_sapling'
    - '*_leaves'
    - 'minecraft:dandelion'
    - '*_tulip'
    - 'minecraft:poppy'
    - '*_orchid'
    - 'minecraft:allium'
    - 'minecraft:azure-bluet'
    - 'minecraft:oxeye_daisy'
    - 'minecraft:lilac'
    - 'minecraft:grass'
    - 'minecraft:tall_grass'
    - 'minecraft:fern'
    - 'minecraft:dead_bush'
    - 'minecraft:sugar_cane'
    - '*_mushroom_block'
    - 'minecraft:mushroom_stem'
    - 'minecraft:melon'
    - 'minecraft:pumpkin'
    - 'minecraft:bee_nest'
    - 'minecraft:cococa'
    - 'minecraft:torch'
    - 'minecraft:rail'
    - 'minecraft:hopper'
    - 'minecraft:oak_sapling'
    - 'minecraft:birch_sapling'
    - 'minecraft:spruce_sapling'
    - 'minecraft:jungle_sapling'
    - 'minecraft:dark_oak_sapling'
    - 'minecraft:acacia_sapling'
    - 'minecraft:bamboo'
    - 'minecraft:vine'
    - 'minecraft:cave_air'
    - 'minecraft:void_air'
    Permission: treeassist.destroy.*
    # Sapling replant settings
    Replanting:
      # Main switch to deactivate sapling replanting
      Active: true
      # How long to wait before placing a sapling. Should stay above 0 because of bukkit event handling
      Delay: 1
      # The Dropped settings have to deal with automatically planting of sapling items, from throwing them and them dropping from leaves
      Dropped:
        Active: false
        Probability: 0.1
        Delay Ticks: 5
      # Even if something prevents sapling replacement or auto destruction, we will place a sapling
      Enforce: false
      # Prevent from breaking this type of sapling at all costs
      Force Protect: false
      # The material to place
      Material: minecraft:air
      # Tools are set in the tool list
      Requires Tools: true
      # Only place saplings when the bottom block was broken
      Only When Bottom Block Broken First: true
      # Replant when a tree block burns
      When Tree Burns Down: true
      # How long to protect saplings
      Protect For Seconds: 0
      # How long should saplings stay there before they can grow?
      Delay Growth Seconds: 0
    Tool List:
    - 'minecraft:diamond_axe'
    - 'minecraft:wooden_axe'
    - 'minecraft:golden_axe'
    - 'minecraft:iron_axe'
    - 'minecraft:stone_axe'
    # Main tree trunk settings
    Trunk:
      # Do we look for branches?
      Branch: false
      # Do we generate custom drops?
      Custom Drops: false
      # Can the trunk go diagonally?
      Diagonal: false
      # How high does it need to be to qualify as a tree?
      Minimum Height: 4
      # One of these materials needs to be part of the trunk for it to count as a trunk!
      Materials:
      - minecraft:bedrock
      # How thick is the trunk?
      Thickness: 1
      # Can the saplings be at different height?
      Uneven Bottom: false
    Version: 7.0