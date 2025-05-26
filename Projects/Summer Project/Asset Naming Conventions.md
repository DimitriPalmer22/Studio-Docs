I've mainly been following this guide for naming assets and structuring the project: <https://github.com/Allar/ue5-style-guide/tree/v2?tab=readme-ov-file#structure-top-level>

- For specifics on what to name assets, scroll down to the section titled "1. Asset Naming Conventions" on this website. It's pretty extensive and should cover pretty much every type of asset you might create.

### Overview

- Asset names generally follow the following format:
	- `Prefix_BaseAssetName_Variant_Suffix`
- Some assets will have different prefixes and suffixes depending on the type of asset they are
- The Variant is optional if there is only one asset of that type

### What to name Assets

| Asset Type         | Prefix | Suffix    | Notes                                                                                                         |
| ------------------ | ------ | --------- | ------------------------------------------------------------------------------------------------------------- |
| Level / Map        |        |           | [Should be in a folder called Maps.](https://github.com/Allar/ue5-style-guide/tree/v2?tab=readme-ov-file#2.4) |
| Level (Persistent) |        | _P        |                                                                                                               |
| Level (Audio)      |        | _Audio    |                                                                                                               |
| Level (Lighting)   |        | _Lighting |                                                                                                               |
| Level (Geometry)   |        | _Geo      |                                                                                                               |
| Level (Gameplay)   |        | _Gameplay |                                                                                                               |
| Blueprint          | BP_    |           |                                                                                                               |
| Material           | M_     |           |                                                                                                               |
| Static Mesh        | S_     |           | Many use SM_. We use S_.                                                                                      |
| Skeletal Mesh      | SK_    |           |                                                                                                               |
| Texture            | T_     | _?        | See [Textures](https://github.com/Allar/ue5-style-guide/tree/v2?tab=readme-ov-file#anc-textures)              |
| Particle System    | PS_    |           |                                                                                                               |
| Widget Blueprint   | WBP_   |           |                                                                                                               |

| Asset Type (Textures)               | Prefix | Suffix | Notes                                                                                                                      |
| ----------------------------------- | ------ | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| Texture                             | T_     |        |                                                                                                                            |
| Texture (Diffuse/Albedo/Base Color) | T_     | _D     |                                                                                                                            |
| Texture (Normal)                    | T_     | _N     |                                                                                                                            |
| Texture (Roughness)                 | T_     | _R     |                                                                                                                            |
| Texture (Alpha/Opacity)             | T_     | _A     |                                                                                                                            |
| Texture (Ambient Occlusion)         | T_     | _O     |                                                                                                                            |
| Texture (Bump)                      | T_     | _B     |                                                                                                                            |
| Texture (Emissive)                  | T_     | _E     |                                                                                                                            |
| Texture (Mask)                      | T_     | _M     |                                                                                                                            |
| Texture (Specular)                  | T_     | _S     |                                                                                                                            |
| Texture (Metallic)                  | T_     | _M     |                                                                                                                            |
| Texture (Packed)                    | T_     | _*     | See notes below about [packing](https://github.com/Allar/ue5-style-guide/tree/v2?tab=readme-ov-file#anc-textures-packing). |
| Texture Cube                        | TC_    |        |                                                                                                                            |
| Media Texture                       | MT_    |        |                                                                                                                            |
| Render Target                       | RT_    |        |                                                                                                                            |
| Cube Render Target                  | RTC_   |        |                                                                                                                            |
| Texture Light Profile               | TLP    |        |                                                                                                                            |

#### Example

| Asset Type               | Asset Name   |
| ------------------------ | ------------ |
| Static Mesh of rock (01) | S_Rock_01    |
| Static Mesh of rock (02) | S_Rock_02    |
| Static Mesh of rock (03) | S_Rock_03    |
| Material                 | M_Rock       |
| Material Instance (Snow) | MI_Rock_Snow |

| Asset Type               | Asset Name   |
| ------------------------ | ------------ |
| Skeletal Mesh            | SK_Bob       |
| Material                 | M_Bob        |
| Texture (Diffuse/Albedo) | T_Bob_D      |
| Texture (Normal)         | T_Bob_N      |
| Texture (Evil Diffuse)   | T_Bob_Evil_D |
