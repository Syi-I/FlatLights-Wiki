| Entangled         | <img src="https://github.com/Syi-I/FlatLights/blob/gear_beta/src/main/resources/assets/flatlights/textures/mob_effect/entangled.png" width="64" alt=""/>                                                                       |
|-------------------|----------------------------------------------------------------------------|
| Color             | <img src="images/misc/entangled_particle.png" width="16" alt=""/> #9386280 |
| Type              | Negative                                                                   |
| Max Natural Level | 5                                                                          |
| ID                | `flatlights:entangled`                                                     |

## Description
Entangled is a negative potion effect that deals a percentage of the target's max health as damage once the effect expires. The percentage of health increases with the level of the effect by +10%, so the damage calculation is as follows:

`expiring_dmg = target_max_health * (0.1 * potion_level)`

Also, when entities are under the Entangled effect, if another entity nearby is Entangled and takes damage, all mobs that are Entangled will receive the same amount of damage in the form of [entangled](Damage-Sources#entangled) damage. By default, the range of Entangled's damage effect is 16 blocks, but this can be changed in the config options.

## Sources
Entangled can only be applied normally through the [Quantum Strike](Quantum-Strike) enchantment, for 30 seconds upon being hit by a weapon with the Quantum Strike enchantment applied to it. The only other source would be using commands.