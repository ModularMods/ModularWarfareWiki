The configuration file of the mod is located in the directory: `.minecraft` -> `ModularWarfare` -> `mod_config.json`
![!](https://modularmods.net/docs/images/mod_config.png)

!!! info "General configuration"
- `customInventory`  
- Default value: `true`
- Info: `Enable/Disable the modded vanilla inventory, if disabled press the key B to open the modded inventory instead.`
- `prototype_pack_extraction`  
- Default value: `true`
- Info: `Auto extract the prototype content-pack from the .jar mod`
- `modified_pack_server_kick`  
- Default value: `true`
- Info: `Kick players that tries to shoot with a modified content-pack (different from the server)`
- `drop_extra_slots_on_death`
- Default value: `true`
- Info: `Force drops of the vests and backpack when a player die (can be useful for corpses mod)`


!!! info "Shots configuration"
- `client_sided_hit_registration`
- Default value: `true`
- Info: `Enable/Disable the client side hit registration, hits are more accurate but depend of the shooter's ping`
- `shot_break_glass`
- Default value: `false`
- Info: `Shots can break glass`
- `knockback_entity_damage`
- Default value: `false`
- Info: `Apply knockback to entities that receives shots`

!!! info "Gun configuration"
- `guns_interaction_hand`
- Default value: `true`
- Info: `Enable/Disable interactions when holding a gun (can open door, chest ...)`


!!! info "Drops configuration"
- `advanced_drops_models`
- Default value: `true`
- Info: `Enable/Disable 3D models for entities drops items`
- `drops_despawn_time`
- Default value: `120`
- Info: `3D models clear drop cooldown (seconds)`
- `advanced_drops_models_everything`
- Default value: `false`
- Info: `Apply 3D models drops for all items (Minecraft, ModularWarfare and others mods).`

!!! info "HUD configuration"
- `hitmarkers`
- Default value: `true`
- Info: `Enable/Disable hitmarkers`
- `dynamic_crosshair`
- Default value: `true`
- Info: `Enable/Disable moving crosshair depending of the player's motion`
- `ammo_count`
- Default value: `true`
- Info: `Enable/Disable ammo count on the right bottom side of the window`
- `snap_fade_hit`
- Default value: `true`
- Info: `Enable/Disable the dark bullet snap texture around the window when receiving hits`

!!! info "Walk sounds configuration"
- `walk_sounds`
- Default value: `true`
- Info: `Enable/Disable custom walks sounds`
- `volume`
- Default value: `0.3`
- Info: `Change the volume of the steps sounds`

!!! info "Walk sounds configuration"
- `casings_drops`
- Default value: `true`
- Info: `Enable/Disable the casings ejection when shooting`
- `despawn_time`
- Default value: `10`
- Info: `Despawn time (seconds)`

!!! info "Killfeed configuration"
- `enableKillFeed`
- Default value: `true`
- Info: `Enable/Disable the killfeed HUD`
- `sendDefaultKillMessage`
- Default value: `false`
- Info: `Disable/Enable the vanilla players kills`
- `messageDuration`
- Default value: `10`
- Info: `Message duration (seconds)`
- `messageList`
- Default value: `(Strings list)`
- Info: `Lists of all message that will be sent randomly (variables: {killer}, {victim})`

!!! info "Important configuration"
- `model_optimization`
- Default value: `true`
- Info: `Enable/Disable the models optimization (can be useful to disable this if you have an old computer or a Mac)`
- `debug_hits_message`
- Default value: `false`
- Info: `Print debugs shoots informations for shots in the console`
- `dev_mode`
- Default value: `true`
- Info: `Ignore this`
- `version`
- Info: `Ignore this`