# Guns models (.obj)

!!! info
    ModularWarfare provide a strong .obj renderer designed to be easy to add your own gun models without restarting Minecraft.

    The software Blender is advised to setup your gun models correctly.

    [Download Blender here](https://www.blender.org/download/)

    [Download the AK47 sample file here](https://modularmods.net/files/ak47.obj)

## Starting with an example

- Open Blender and import the .obj sample file
![!](https://modularmods.net/docs/images/ak47.png)

Each parts of the gun have a specific object name on Blender.

![!](https://modularmods.net/docs/images/ak47-2.png)

![!](https://modularmods.net/docs/images/ak47-3.png)

!!! info
	Each objects child must have the same name of his parent object.
	![!](https://modularmods.net/docs/images/ak47-4.png)

!!! info
	Parts name:

	- gunModel

	- slideModel

	- ammoModel

	- flashModel

	- defaultScopeModel

	- defaultBarrelModel

	- defaultStockModel

	- defaultGripModel

	- defaultGadgetModel

	- boltModel

	- pumpModel

	- chargeModel

	- triggerModel 

## OBJ Structure

Here we have an object with the name flashModel.

Having a correct object name from the list above allows the mod to animate certain parts of your models. 
```
o flashModel
v 12.327478 -2.216826 -0.897541
v 12.327477 2.202816 3.522110
v 12.327478 2.202822 -0.897538
v 12.327477 -2.216830 3.522105
vt 0.999900 0.000100
vt 0.000100 0.999900
vt 0.000100 0.000100
vt 0.999900 0.999900
vn -1.0000 -0.0000 -0.0000
usemtl (null).002
s off
f 2296/2951/2269 2297/2952/2269 2298/2953/2269
f 2296/2951/2269 2299/2954/2269 2297/2952/2269
```

## Create/Setup your gun models

First, import your model in the existing project with the ak47 in Blender, and try to place the sight in the same position that the sample object.

- Setup the correct size/position of a gun model

	Press `S` to scale the model

	Press `R` to rotate the model + [`X`, `Y`, `Z`]
	![!](https://modularmods.net/docs/images/ak47-5.png)

- Align sight via blender

	![!](https://modularmods.net/docs/images/ak47-6.png)

## Textures

!!! failure
	Warning, you can have only one texture for a gun model.
	This means that the .mtl file is not necessary.

Example of an UV map for the MP40, it only use one texture for the whole gun.
![!](https://modularmods.net/docs/images/texture1.png)

Note: The flashModel need this type of UV, that take the whole texture range. Because when rendered, it will not use the gun texture but the flash textures instead.
You can take the flashModel from the ak47 sample file.
![!](https://modularmods.net/docs/images/texture2.png)


To understand how to make your UV mappings I recommend you this video: [https://www.youtube.com/watch?v=Bh0YV-Y_qHY](https://www.youtube.com/watch?v=Bh0YV-Y_qHY)

## Finally

Your gun model is ready now, export your .obj and select this export parameter on blender.

!!! failure
	Triangulate faces need to be checked !
![!](https://modularmods.net/docs/images/texture3.png)

