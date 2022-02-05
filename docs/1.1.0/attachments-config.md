# Guns config files (.json)

## Starting with examples

Mono. AK Suppressor
```json
{
	"displayName": "Mono. AK Suppressor",
	"internalName": "prototype.ak47_suppressor",
	"attachmentType": "barrel",
	"modelSkins": [
		{
			"skinAsset": "prototype.ak47_suppressor",
			"displayName": "AK47 Suppressor - Default"
		}
	],
	"barrel": {
		"isSuppressor": true,
		"hideFlash": true
	}
}
```

Holo Sight/Scope

```scopeType: reddot, 2x, 4x, 8x, 15x, default```

```customOverlayTexture: prototype.holo_sight, prototype.scope2x, prototype.scope4x, prototype.scope8x, prototype.scope15x```

```json
{
	"displayName": "Holo Sight",
	"internalName": "prototype.holo_sight",
	"attachmentType": "sight",
	"modelSkins": [
		{
			"skinAsset": "prototype.holo_sight",
			"displayName": "Holo Sight - Default"
		}
	],
	"sight": {
		"scopeType": "2x",
		"customOverlayTexture": "prototype.holo_sight"
	}
}
```

Ergonomic Foregrip
```json
{
	"displayName": "Ergonomic Foregrip",
	"internalName": "prototype.ergo_foregrip",
	"attachmentType": "grip",
	"modelSkins": [
		{
			"skinAsset": "prototype.ergo_foregrip",
			"displayName": "Ergonomic Foregrip - Default"
		}
	],
	"grip": {
		"recoilPitchFactor": 0.5,
		"recoilYawFactor": 0.5
	}
}
```


## Attachment Types

!!! info 
	- `sight` 
		- Info: `For sight/scopes attachment
		- Require: The section `sight` -> `scopeType, sensitivityScopeFactor` parameters.
	- `barrel`
		- Info: `For flash hiders, suppressor.`
	- `slide`  
		- Info: `Slides attachment.`
	- `grip`  
		- Info: `For grips attachments, allow to reduce the recoil.`
		- Require: The section `grip` -> `recoilPitchFactor, recoilYawFactor` parameters.
	- `flashlight`  
		- Info: `If a flashlight is applied on the gun, press H to enable the flash.`
	- `charm`  
		- Info: `Add a custom charm, to make your gun badass`

## Attachment Render Config

Long scope render config (prototype.long_scope.render.json)

You can configure the FOV zoom of a scope, the mouse sensitivity and the rectile scale.
```json
{
	"modelFileName": "long_scope.obj",
	"extra": {
		"modelScale": 1.0
	},
	"sight": {
		"fovZoom": 14.0,
		"mouseSensitivityFactor": 0.5,
		"rectileScale": 1.75
	}
}
```

Ergonomic Foregrip (prototype.long_scope.render.json)

You can configure the translation of the left arm when a grip is applied as an attachment
```json
{
	"modelFileName": "ergo_foregrip.obj",
	"extra": {
		"modelScale": 1.0
	},
	"grip": {
		"leftArmOffset": {
			"x": 0.0,
			"y": -0.018,
			"z": 0.0
		}
	}
}
```
Enjoy
![!](https://modularmods.net/docs/images/ergo_long_scope.png)