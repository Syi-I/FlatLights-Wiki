| Prismatic Chestplate | ![](https://github.com/Syi-I/FlatLights/blob/gear_beta/src/main/resources/assets/flatlights/textures/item/prismatic_chestplate.png) |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Craftable            | Yes                                                                                                                                 |
| Stackable            | No                                                                                                                                  |
| Creative Tab         | Flat Lights                                                                                                                         |
| Item ID              | `flatlights:prismatic_chestplate`                                                                                                   |

The prismatic chestplate is an armor piece.

## Appearance
The prismatic chestplate is an off-white color with yellow and blue highlights spanning across the chest diagonally, and also on the shoulders. There are gray and white hand coverings attached on the arms of the chestplate, as well as a gray spine on the back of the chestplate.

[[images/screenshots/prismatic_armor.png]]  
_The prismatic armor pieces on armor stands_

## Obtaining
The prismatic chestplate can be crafted in a [Spectralizer](Spectralizer) using 1 [prismatic chestplate core](Prismatic-Chestplate-Core), 1 netherite ingot, 2 nether stars, and 2 [prisma nuclei](Prisma-Nucleus). This outputs 1 prismatic chestplate. Prismatic chestplates can also be found in the `Flat Lights` creative tab, or obtained through the `/give` command.

[[images/recipes/prismatic_chestplate.png]]  
*The crafting recipe for a prismatic chestplate, using a Spectralizer*

## Usage
The prismatic chestplate is armor that the player can wear, providing protection levels that are higher than the netherite equivalent. Prismatic chestplates provide `+12 Armor`, `+5 Armor Toughness`, and `+2.5 Knockback Resistance` when worn in the appropriate slot. Wearing the chestplate also provides creative style flight capabilities. The flight option can be disabled in the config options.

### Damage Reduction
Prismatic armor provides extra damage reduction when the wearer hits a certain threshold of armor points. Once the player has a combined total of armor points above 20 points, or full diamond armor, any armor points above 20 will add +5% damage reduction. The damage calculation looks like this: 

`armor_total = player_armor - 20 > 0 ? player_armor - 20 : 0`   
`reduction_ratio = min(armor_total * 0.05, config_reduction_cap)`   
`new_dmg = base_dmg * (1 - reduction_ratio)`

Wearing a full set of prismatic armor will provide 30 armor points, so 10 extra points above diamond armor. The player does not have to wear a full set of prismatic armor for the damage reduction to work, any combination of armor that provides more than 20 points of armor can be used, meaning players can reach high amounts of reduction. This reduction has a limited amount that can accumulate though, shown in the armor pieces' tooltips, and by default is set to 25% extra damage reduction. This can be set from 0-100% in the config options to balance the effect as needed. While players only need to wear a single piece of prismatic armor to trigger the damage reduction effect, there is also a config option to enable 'multilayered reduction', which applies the reduction effect once per piece of prismatic armor worn instead of just one single time. For example, if a player is wearing a full set of prismatic armor, the damage calculation seen above will be performed 4 times in a row. The damage calculation would then look like this:

`armor_total = player_armor - 20 > 0 ? player_armor - 20 : 0`   
`reduction_ratio = min(armor_total * 0.05, config_reduction_cap)`   
`first_reduction = base_dmg * (1 - reduction_ratio)`    
`second_reduction = first_reduction * (1 - reduction_ratio)`     
`third_reduction = second_reduction * (1 - reduction_ratio)`     
`final_dmg = third_reduction * (1 - reduction_ratio)`

This is significantly more potent protection, but could be balanced around having a low reduction cap set in the configs so players would have to choose between multilayered reduction or higher armor from external armor choices and only one instance of damage reduction.

### Set Effect
Wearing a full set of prismatic armor gives the wearer the `Saturation` effect while worn.

The prismatic chestplate can be enchanted via an enchanting table, or by combining it with enchanted books in an anvil. It is unbreakable, so it cannot be repaired in an anvil.

There are no crafting uses for the prismatic chestplate.
