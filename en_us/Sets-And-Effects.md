This is a list of all curio sets and curio set effects added by Flat Lights, with descriptions.

## Curio Sets
### Dragon's Final Test
A basic curio set that provides well-rounded stat bonuses for combat and survival. This set does not focus on any one aspect in particular, adding a lot of weaker stat buffs rather than a few stronger ones.

### On the Forgotten Shore
A curio set based around movement and survivability, with a focus on adding buffs that benefit water traversal and combat.

### Radiance of the False Sun
A curio set focusing on the player's damage and healing abilities, with improved damage towards targets that take fire or lava damage.

## Curio Set Effects
### Erosion Aura
This set effect projects an aura around the wearer that deals [entangled](Damage-Sources#entangled) damage to any entities with less max health than the wearer. The damage dealt is determined by the difference between the wearer's max health and the target's max health, and modified by a percent of how close the target is to the wearer. The resulting damage calculation is as follows:

`total_effect_radius = min(6 + growth_progress, 32)`    
`percentMod = 1 - (distance_from_player / total_effect_radius)`     
`damage = max(player_max_health - target_max_health, 0) * percentMod`

The default base radius of 6 can be changed in the config options, and `growth_progress` is 0 if the curio is not a growth tier. The damage scales higher if the target is closer to the wearer.

[[images/screenshots/erosion_aura_indicator.png]]   
_Erosion aura effect indicator, toggled off (left) vs toggled on (right)_

### Domain of Still Waters
This set effect provides a damage increase when the player or target is in water, or if it is raining. By default, it is a 3x damage increase but this value can be changed in the config options. Also, if the target is in water, or it is raining, then the `slowness` effect is applied to the target. The level of slowness is determined by the distance to the wearer, going from `slowness 1` up to `slowness 4` depending on how close the target is relative to the wearer.

`total_effect_radius = min(16 + growth_progress, 32)`    
`percent_distance = 1 - (distance_from_player / total_effect_radius)` 

| percent_distance | Slowness Level |
|------------------|----------------|
| < 0.25           | 1              |
| \>= 0.25         | 2              |
| \>= 0.5          | 3              |
| \>= 0.75         | 4              |

The default base radius of 16 can be changed in the config options, and `growth_progress` is 0 if the curio is not a growth tier.

### Rising Heat
This set effect provides a damage increase to targets that are burning. Targets that are burning take 75% increased damage from any form of damage the wearer inflicts. It also makes targets that are both nearby and burning take more damage from fire and lava sources. The damage increase for targets that take fire or lava damage is a flat 3 bonus damage.

`total_effect_radius = min(8 + growth_progress, 32)`    

The default base radius of 8 can be changed in the config options, and `growth_progress` is 0 if the curio is not a growth tier.

[[images/screenshots/rising_heat_effect.png]]   
_A creeper that has the Rising Heat effect_
