# Guns render files (.render.json)

Render files are located in `content-pack` -> `guns` -> `render` -> `yourgun.render.json`

It allows to setup the client rendering parameters of your guns, such as arms position, aim position, attachments positions, model scale.
![!](https://modularmods.net/docs/images/render-1.png)

### Shortcuts
No needs to restart Minecraft if you want to modify a parameter ! Shortcuts exists.
!!! info "Important ingame shortcuts to help content-pack creators"
- `F9` to reload .obj models + render.json files
- `F10`+ `SNEAK` to reload only configurations json
- `F9`+ `SNEAK` to reload the resource-packs (sounds, textures, items)

### Attachments parameters (positionPointMap)
Important, for the attachments parameters there is `positionPointMap` which contains one (x,y,z) for the translation/position and the second (x,y,z) for the rotation in degree.
As an instance, my MP5 will setup the `prototype.docter_sight_mini` (internalName of my attachment) to the position -3, -0.2, 0.02 and no rotations angle.
```json
"attachments": {
    "positionPointMap": {
        "prototype.docter_sight_mini": [
            {
            "x": -3.0,
            "y": -0.2,
            "z": 0.02
            },
            {
            "x": 0.0,
            "y": 0.0,
            "z": 0.0
            }
        ],
        "prototype.my_other_attachment": [
          {
            "x": -1.0,
            "y": -0.1,
            "z": 0.01
          },
          {
            "x": 20.0,
            "y": 0.0,
            "z": 0.0
          }
        ]
    }
}
```
### Attachments parameters (aimPointMap)
The second important parameter for the attachments is `aimPointMap` which will translate/rotate the whole gun when the attachment is applied.
It can help if to center the scope attachment when aiming.
```json
"attachments": {
    "aimPointMap": {
    "prototype.docter_sight_mini": [
        {
        "x": 0.0,
        "y": -0.15,
        "z": 0.0
        },
        {
        "x": 0.0,
        "y": 0.0,
        "z": 0.5
        }
    ]
}
```

### Example MP5 render config (prototype.mp5.render.json)

```json
{
  "modelFileName": "mp5.obj",
  "arms": {
    "leftHandAmmo": true,
    "actionArm": "Left",
    "leftArm": {
      "armScale": {
        "x": 0.7,
        "y": 1.0,
        "z": 0.7
      },
      "armPos": {
        "x": -0.15,
        "y": -0.9,
        "z": 0.1
      },
      "armRot": {
        "x": 65.0,
        "y": 32.0,
        "z": -46.0
      },
      "armReloadPos": {
        "x": -0.35,
        "y": -1.0,
        "z": 0.1
      },
      "armReloadRot": {
        "x": 35.0,
        "y": 0.0,
        "z": -25.0
      }
    },
    "rightArm": {
      "armScale": {
        "x": 0.7,
        "y": 1.0,
        "z": 0.7
      },
      "armPos": {
        "x": 0.21,
        "y": -0.71,
        "z": 0.0
      },
      "armRot": {
        "x": 0.0,
        "y": 0.0,
        "z": -90.0
      },
      "armReloadPos": {
        "x": 0.21,
        "y": -0.71,
        "z": 0.0
      },
      "armReloadRot": {
        "x": 0.0,
        "y": 0.0,
        "z": -90.0
      },
      "armChargePos": {
        "x": 0.47,
        "y": -0.39,
        "z": 0.14
      },
      "armChargeRot": {
        "x": 0.0,
        "y": 0.0,
        "z": -90.0
      }
    }
  },
  "sprint": {
    "sprintRotate": {
      "x": 10.0,
      "y": 30.0,
      "z": 0.0
    },
    "sprintTranslate": {
      "x": 1.05,
      "y": -0.05,
      "z": -0.7
    }
  },
  "thirdPerson": {
    "thirdPersonOffset": {
      "x": 0.0,
      "y": -0.15,
      "z": 0.0
    },
    "backPersonOffset": {
      "x": 0.0,
      "y": 0.0,
      "z": 0.0
    },
    "thirdPersonScale": 1.0
  },
  "aim": {
    "rotateHipPosition": {
      "x": 0.0,
      "y": 0.0,
      "z": 0.0
    },
    "translateHipPosition": {
      "x": 0.0,
      "y": 0.0,
      "z": 0.0
    },
    "rotateAimPosition": {
      "x": 0.0,
      "y": 0.07,
      "z": 0.3
    },
    "translateAimPosition": {
      "x": 0.15,
      "y": 0.01,
      "z": 0.00045
    }
  },
  "attachments": {
    "positionPointMap": {
      "prototype.docter_sight_mini": [
        {
          "x": -3.0,
          "y": -0.2,
          "z": 0.02
        },
        {
          "x": 0.0,
          "y": 0.0,
          "z": 0.0
        }
      ]
    },
    "aimPointMap": {
      "prototype.docter_sight_mini": [
        {
          "x": 0.0,
          "y": -0.15,
          "z": 0.0
        },
        {
          "x": 0.0,
          "y": 0.0,
          "z": 0.5
        }
      ]
    }
  },
  "itemFrame": {
    "translate": {
      "x": 5.5,
      "y": 0.0,
      "z": 0.0
    }
  },
  "extra": {
    "translateAll": {
      "x": 0.0,
      "y": 0.0,
      "z": 0.0
    },
    "modelScale": 1.2,
    "reloadAnimation": "pistol",
    "gunOffsetScoping": 0.0,
    "crouchZoom": -0.04,
    "adsSpeed": 0.07,
    "gunSlideDistance": 0.1,
    "modelRecoilBackwards": 0.05,
    "modelRecoilUpwards": 0.05,
    "modelRecoilShake":  0.05
  }
}
```