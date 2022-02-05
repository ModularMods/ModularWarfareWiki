# Guns config files (.json)

## Starting with an example
```json
{
	"internalName":"prototype.ak47",
	"displayName":"AKM",
	"weaponType":"carbine",
	"extraLore": "The true legend AK47",
	"customFlashTexture":"prototype.advanced.flash",
	"gunDamage":9,
	"gunDamageHeadshotBonus":2,
	"roundsPerMin":350,
	"allowEmptyMagazines":true,
	"recoilPitch": 5.5,
	"recoilYaw":0.75,
	"randomRecoilPitch": 0.0,
	"randomRecoilYaw": 0.7,
	"bulletSpread":1.0,
	"accuracySneakFactor":0.5,
	"moveSpeedModifier":1.0,
	"allowSprintFiring":true,
	"fireModes":[
		"full",
		"semi"
	],
	"acceptedAmmo":[
		"prototype.ak47ammo"
	],
	"dropBulletCasing":true,
	"shellEjectOffsetNormal":{
		"x":-1.0,
		"y":0.0,
		"z":1.0
	},
	"shellEjectOffsetAiming":{
		"x":-0.2,
		"y":0.12,
		"z":0.5
	},
	"weaponSoundMap":{
		"weaponFire":[
			{
				"soundEvent":"weaponFire",
				"soundName":"prototype.ak47.shoot",
				"soundNameDistant":"prototype.ak47.shoot.distant",
				"soundRange":64,
				"soundMaxRange":96,
				"soundFadeMultiplier":1
			}
		],
		"weaponUnload":[
			{
				"soundEvent":"weaponReload",
				"soundName":"prototype.generic.reload"
			}
		],
		"weaponFireSuppressed":[
			{
				"soundEvent":"weaponFireSuppressed",
				"soundName":"prototype.ak47.shoot.sup",
				"soundRange":30,
				"soundMaxRange":50,
				"soundFadeMultiplier":1
			}
		]
	},
	"acceptedAttachments":{
		"barrel":[
			"prototype.ak47_suppressor"
		]
	},
	"modelSkins":[
		{
			"internalName":"prototype.ak47",
			"skinAsset":"prototype.ak47",
			"displayName":"Default"
		},
		{
			"internalName":"prototype.ak47.urban",
			"skinAsset":"prototype.ak47.urban",
			"displayName":"Urban"
		}
	]
}
```

## Default BaseType configuration
```java
	/**
	 * The internal name of your gun (important, it is recommended to name it 'contentpack-name.yourgunname')
	 */
	String internalName

	/**
	 * Max stack size
	 */
	Integer maxStackSize
	/**
	 * Weapon staticModel skins/textures
	 */
	SkinType[] modelSkins
	/**
	 * Used to generate .lang files automatically
	 */
	String displayName
	String iconName
```

## Gun stats
```java
	/**
	 * Weapon Classification for later use with default animations etc
	 */
	WeaponType weaponType
```

Possible values (String): `custom`, `pistol`, `mp`, `smg`, `carabine`, `rifle`, `ar`, `dmr`, `semisniper`, `boltsniper`, `shotgun`

```java
	/**
	 * The firing modes of the gun. SEMI, FULL, BURST
	 */
	WeaponFireMode[] fireModes
```

Possible values (String): `SEMI`, `FULL`, `BURST`

```java
	/**
	 * Damage inflicted per bullet. Multiplied by the bullet damage value.
	 */
	float gunDamage
```

Recommended values (Float): `10.0` `= 5 hearts per hit`

```java
	/**
	 * Bonus damage inflicted per bullet when headshot.
	 */
	public float gunDamageHeadshotBonus
```

Recommended values (Float): `2.0` `= 1 heart damage bonus`

```java
	/**
	 * The amount that bullets spread out when fired from this gun
	 */
	float bulletSpread
```

Recommended values (Float): `1.0` to `2.5`

```java
	/**
	 * The fire rate of the gun in RPM, 700 = MAX
	 */
	int roundsPerMin
```

Recommended values (Float): `300` - `500`

Extra info: `If your gun is semi-automatic like a shotgun, pistol you can lower this value to 100 - 250`

```java
	/**
	 * The number of bullets to fire per burst in burst mode
	 */
	int numBurstRounds = 3
```

## Gun recoil / accuracy mechanic

```java
	/**
	 * Base value for Upwards cursor/view recoil
	 */
	float recoilPitch = 10.0

	/**
	 * Base value for Left/Right cursor/view recoil
	 */
	float recoilYaw = 1.0
```

```java
	/**
	 * Random factor of the pitch recoil
	 */
	float randomRecoilPitch = 0.5

	/**
	 * Random factor of the yaw recoil
	 */
	float randomRecoilYaw = 0.5
```

Recommended values (Float): `0.0` - `1.0`

```java
	/**
	 * Factor of accuracy when sneaking
	 */
	float accuracySneakFactor = 0.75
```

Recommended values (Float): `0.0` - `1.0`

```java
	/**
	 * Factor of the recoil when aiming
	 */
	float recoilAimReducer = 0.7F;
```

Recommended values (Float): `0.0` - `1.0`

## Ammos / Magazines

```java
	/**
	 * Ammo types which can be used in the gun
	 */
	String[] acceptedAmmo;
```

- Examples:

	With only one compatible mag:
	```json
	    "acceptedAmmo": ["prototype.ak74uammo"],
	```

	With multiples compatible mags:
	```json
	    "acceptedAmmo": ["prototype.ak74uammo", "prototype.ak74ufastmag"],
	```

```java
	/**
	 * If true && != null, ammo moddel will be set by ammo type used. Used built-in ammo model by default
	 */
	boolean dynamicAmmo = false;
```

Extra info: `Set this to true if you want to render your custom ammo/magazine model on your gun when charged with it.`

```java
	/**
	 * The bullets internalName that is compatible with this gun
	 */
	String[] acceptedBullets
```

Extra info: `Can be useful for shotguns, to load gauge shell instead of magazines.`

## Reload

```java
	/**
	 * The time (in ticks) it takes to reload this gun
	 */
	int reloadTime = 40;
```

Recommended values (Integer): `40`

## Gun attachments

```java
	/**
	 * Attachment Types
	 */
	HashMap acceptedAttachments
```

- Examples:
	
	```json
	    "acceptedAttachments": {
	        "barrel": [ //Your attachment type
	            "prototype.ak47_suppressor", //Your first attachment internalName
	            "prototype.ak47_flashhider" //Your second attachment internalName
	        ],
	        "sight": [
	            "prototype.obzor_sight"
	        ],
	        "flashlight": [
	            "prototype.ak74u_flashlight"
	        ]
	    }
	```

	Attachments types name: `sight`, `slide`, `grip`, `flashlight`, `charm`, `skin`, `barrel`

	And add the internal name of the attachment compatible with your gun.

## Gun movements

```java
	/**
	 * Allow to shoot when sprinting
	 */
	boolean allowSprintFiring = true
```

```java
	/**
	 * Speed modifier when a player has a gun in their hand (0.0 - 1.0)
	 */
	float moveSpeedModifier = 1.0
```

Extra info: `Setting this parameter to 1.0 will not reduce the speed of the player`

## Gun shell casings

```json
//The position where the shell casings will spawn, do not touch
"shellEjectOffsetNormal": {
    "x": -1.0,
    "y": 0.0,
    "z": 1.0
},
"shellEjectOffsetAiming": {
    "x": -0.2,
    "y": 0.12,
    "z": 0.5
},
```

## Gun sounds

```java
	/**
	 * The sound json list of your gun
	 */
	HashMap weaponSoundMap
```

- Examples:
	
	```json
	"weaponSoundMap": {
	    "weaponFire": [
	        {
	            "soundEvent": "weaponFire",
	            "soundName": "prototype.ak47.shoot",
	            "soundNameDistant": "prototype.ak47.shoot.distant",
	            "soundRange": 64,
	            "soundMaxRange": 96,
	            "soundFadeMultiplier": 1
	        }
	    ],
	    "weaponUnload": [
	        {
	            "soundEvent": "weaponReload",
	            "soundName": "prototype.generic.reload"
	        }
	    ],
	    "weaponFireSuppressed": [
	        {
	            "soundEvent": "weaponFireSuppressed",
	            "soundName": "prototype.ak47.shoot.sup",
	            "soundRange": 30,
	            "soundMaxRange": 30,
	            "soundFadeMultiplier": 1
	        }
	    ]
	},
	```

	WeaponSoundType list:

	- weaponDryFire : The sound played upon dry firing

	- weaponFire: The sound played upon shooting

	- weaponFireSuppressed: The sound played upon shooting with a silencer

	- weaponFireLast: The sound to play upon shooting on last round

	- weaponReload: The sound to play upon reloading

	- weaponBolt: The sound to play when touching the bolt action

	- weaponBulletLoad: The sound to play upon load bullet

	- weaponLoad: The sound to play upon loading

	- weaponUnload: The sound to play upon unloading

	- weaponReloadEmpty: The sound to play upon reloading when empty

	- weaponCharge: The sound to play upon charging (ex: shotgun)

	- weaponModeSwitch: The sound to play upon switching fire modes


	The soundName the name of your sound located in `assets/modularwarfare/sounds.json`