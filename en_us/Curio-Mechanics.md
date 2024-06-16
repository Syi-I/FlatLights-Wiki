Flat Lights requires the mod [Curios v4.1.0.0](https://www.curseforge.com/minecraft/mc-mods/curios/files/4419403) or above to be installed.

## Overview
The curios that Flat Lights adds can be found in the loot chests of most generated structures. When first found, curios start off unrolled. When a player uses the curio for the first time it will roll a random [tier](#tiers). While the curios all share the same sprites, the curios' [sets](#sets) are predetermined as they are actually different items. All curios from Flat Lights have a set, [set effect](#set-effects), and tier, and have a certain slot type that they belong to.

## Obtaining
Every curio has a chance to generate in the chests of basically any generated structure, such as but not limited to basic dungeons, strongholds, or desert temples. The chance of finding any one of the curios is equal, so finding one complete set may be difficult. Each chest has a chance of generating 1-3 curios.

| Total Curios | Drop Chance |
|:------------:|:-----------:|
|      1       |     85%     |
|      2       |     50%     |
|      3       |     30%     |

There is also an increased chance for more curios generating, depending on the structure and dimension.

|  Location   | Total Drop Chance Increase |
|:-----------:|:--------------------------:|
| Strongholds |            10%             |
|   Nether    |            15%             |
|     End     |            25%             |

## Tiers
The curios from Flat Lights all have a tier which determines the [stat bonus multiplier](#tier-stat-differences) that gets applied to the bonus stats of a curio, and can also sometimes get applied to a curio's set effect depending on the actual effect. The tiers, roll chance, and stat multipliers are as follows:

|    Tier    | Drop Chance | Stat Multiplier  |
|:----------:|:-----------:|:----------------:|
|   Common   |     45%     |        1x        |
|    Rare    |     30%     |       1.5x       |
|    Epic    |     15%     |        2x        |
| Legendary  |     9%      |       2.5x       |
|   Growth   |     1%      |       2.5x       |

### Tier Stat Differences
The tier `Stat Multiplier` changes the value of stats that the curio provides as a bonus when worn. As an example, let's say a player has a `Common` tier curio that provides `+4 Armor` and `+6 Max Health`. If the player had an `Epic` tier version of this curio, the stat increase would instead be `+8 Armor` and `+12 Max Health` when worn. This means a player would typically want to wear only their highest tier curios. The drawback to only picking the highest tier curios is that the player may not have a matching curio [set](#sets), which would prevent the player from using any [set effects](#set-effects). The player will thus have a choice between having high raw stat bonuses, or being able to use the powerful set effects that wearing a curio set can provide, unless the player is very lucky and happens to have a matching set of high tier curios.

#### Growth Tier
The growth tier curios are extremely rare, and have a capped amount of growth that the player can increase progression of. Growth progress is achieved simply by killing any mobs, and more progress is gained depending on the max health of the creature slain. The minimum growth progress gained for killing a mob is 1 point, otherwise progress is equal to `max(round(mob_max_health / 20)), 1)`, or how many times more health the mob has compared to the player's base health.  Increasing the growth progress of growth tier curios will slowly increase the stats of the curio, growing by `0.01 * growthProgress`. By default, the growth of curios is capped to 1000, which usually translates to `+10` stat points per stat compared to the same curio if it was `Legendary` tier. This cap cannot be changed currently, but there are plans for a config option. In some cases, the growth progress can also increase the set effect potency or range of the curio. This only makes a difference on the [cube](#light-cubes) curios though, as on the backend only the cube slot holds the functionality of the set effects.

## Sets
Every curio from Flat Lights has a set that it is a part of, and this set of curios will have an associated [set effect](#set-effects) that can be triggered when a Light Cube, Light Prism, and Light Sphere of the same set are worn together in the appropriate slots. The Set of the curio is predetermined and cannot be changed through any means.

[List of curio sets](Sets-And-Effects#Curio-Sets)

## Set Effects
Every curio from Flat Lights has a set effect, which can be triggered when a player wears a matching set of a Light Cube, Light Prism, and Light Sphere. The Set Effect can be triggered only if the player's curios are all part of the same [set](#sets), and the effect can be toggled on and off using a set keybind (Default: V). Do note that you cannot trigger a Set Effect unless the curios are in the custom [Light Cube/Light Prism/Light Sphere](#slot-types) curio slots. The system will not check generic Curio slots.

[List of curio set effects](Sets-And-Effects#Curio-Set-Effects)

## Slot Types
Curios that are added by Flat Lights are categorized into three custom added slot types: Light Cubes, Light Prisms, and Light Spheres. The player will get one of each slot type by default, and curios are balanced around this number of slots. Functionality of the [set effect](#set-effects) also depends on this number of slots, and only the first curio found in each slot type will count towards the various bonuses that can be acquired. Keep this in mind before deciding to add more of these slot types.

### Light Cubes
Light Cubes generally give stat buffs for a player's movement and survivability in some way, shape, or form. Usually, you will find stat increases for armor, armor toughness, or max health. On occasion, they can also give stat buffs for movement speed or swim speed. 

### Light Prisms
Light Prisms focus on offensive stats for players. This means increases to a player's attack, attack speed, and on occasion can increase the attack reach of a player. Increasing the attack reach is done using the vanilla `Reach` attribute, so any other methods of increasing this stat will also increase the attack reach of the player.

### Light Spheres
Light Spheres do not have any particular focus, but generally give increases to a special, custom attribute, and can also apply constant potion effects to the player. Potion effects will be beneficial to the player, providing things like `Night Vision` or `Fire Resistance`.

## Custom Stats
Flat Lights adds custom attributes that the player can gain through the added curios. For now, the only means of increasing these stats is through wearing the custom curios, but there is potential for this to change in the future.

### Dodge Chance %
Dodge Chance % gives the player the chance to dodge attacks entirely. The higher the Dodge Chance % of the player, the higher the chance to not take damage from an instance of damage.

### XP Boost
XP Boost increases the amount of XP that a player gains from picking up an XP orb. When a player's XP changes, a flat amount is added to the base amount of XP that the player would have gained. The amount gained is equivalent to the total XP Boost stat that the player has.

### Healing Boost
Healing Boost increases the amount of health gained whenever the player heals. When the player heals, the amount healed is increased by a flat amount. The amount healed is equivalent to the total Healing Boost stat the player has.

### Bonus Loot Rolls
Bonus Loot Rolls increases the number of times that the loot increases by when the Bonus Loot Rolls effect triggers. The amount of loot that drops is multiplied by the total of the player's Bonus Loot Rolls stat. For example, let's say a player has `+3 Bonus Loot Rolls` from the Light Sphere that they have equipped and the player kills a pig, which happens to drop 2 raw pork chops. When the `Bonus Loot Rolls` effect triggers, the player receives 8 total raw pork chops instead, as they had 3 bonus loot rolls which gave 6 extra raw pork chops. The max number of rolls a player can get total can be capped in the config options.

### Bonus Loot Roll Chance %
Bonus Loot Roll Chance % increases the chance that the `Bonus Loot Rolls` effect triggers. The higher the Bonus Loot Roll Chance %, the higher the chance of triggering the effect. The max chance can be capped in the config options.

