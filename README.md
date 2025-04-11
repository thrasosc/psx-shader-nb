# PSX Shader NB

This shader pack is a fork of ckosmic's [Minecraft PSX Shader](https://github.com/ckosmic/minecraft-psx) that mimics the look and feel of PlayStation 1 graphics.

## Changes in this Fork

### Modified

Changed vertex transformation to eliminate the bouncing effect when moving.

### Technical Details

The following files were modified:

- `shaders/gbuffers_entities.vsh`
- `shaders/gbuffers_hand.vsh`
- `shaders/gbuffers_basic.vsh`
- `shaders/gbuffers_armor_glint.vsh`

Changed the vertex transformation from:

```glsl
vec4 position4 = mat4(gl_ModelViewMatrix) * vec4(gl_Vertex) + gl_ModelViewMatrix[3].xyzw;
```

to standard transformation:

```glsl
vec4 position4 = gl_ModelViewMatrix * vec4(gl_Vertex);
```

## Installation

Place this shader pack in your Minecraft `shaderpacks` folder.

This shader pack works with both [OptiFine](https://optifine.net/) and [Iris](https://irisshaders.net/).

## Credits

- Original shader by ckosmic
- Iris compatibility by Karen/あけみ (akemin_dayo)

## License

Licensed under the [MIT License](https://choosealicense.com/licenses/mit/).
