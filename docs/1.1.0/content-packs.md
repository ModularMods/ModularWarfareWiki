### File type
A content-packs can be a:

- directory

- .zip `(with an optional password protection)`

- .jar 

![!](https://modularwarfare.com/docs/images/content-packs.png)

### Structure
Each directory in a content-pack correspond of a type (excepted: `/obj/` and `/assets/`)
![!](https://modularwarfare.com/docs/images/structure.png)

For example inside the folder type [guns]:
![!](https://modularmods.net/docs/images/structure-2.png) 

We have a `.json` config file for each guns. These files contains for example the `gunDamage`, `fireModes`, `weaponType` and plenty of others parameters to make your guns unique.

!!! info "Notice `/render/` folder in the types [ammo], [armors], [guns], [backpacks] and [bullets]"
	These folders contains all the client-side render parameters of each items type, some are optional like [ammo] and [bullets]. 

	Example inside the `/render/` folder in [guns]
	![!](https://modularwarfare.com/docs/images/structure-3.png) 


### Shortcuts
No needs to restart Minecraft if you want to modify a parameter ! Shortcuts exists.
!!! info "Important ingame shortcuts to help content-pack creators"
  - `F9` to reload .obj models + render.json files
  - `F10`+ `SNEAK` to reload only configurations json
  - `F9`+ `SNEAK` to reload the resource-packs (sounds, textures, items)