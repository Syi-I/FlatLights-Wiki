| Bleed             | <img src="https://github.com/Syi-I/FlatLights/blob/gear_beta/src/main/resources/assets/flatlights/textures/mob_effect/bleed.png" width="64" alt=""/> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color             | <img src="images/misc/bleed_particle.png" width="16" alt=""/> #9386280                                                                               |
| Type              | Negative                                                                                                                                             |
| Max Natural Level | 5, with config option                                                                                                                                |
| ID                | `flatlights:bleed`                                                                                                                                   |

## Description
Bleed is a negative potion effect that applies a damage over time (DoT) effect to entities. Every 2 seconds that passes while the Bleed effect is active, the effected target receives a percent of its max health as damage. The percentage of health increases with the level of the effect by +3%, so the damage calculation is as follows:

`dmg = target_max_health * (0.03 * potion_level)`

## Sources
Bleed can only be applied normally through the [Bleeding Edge](Bleeding-Edge) enchantment, for 30 seconds upon being hit by a weapon with the Bleeding Edge enchantment applied to it. The only other source would be using commands.