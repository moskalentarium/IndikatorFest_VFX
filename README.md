# IndikatorFest
- [Materials](#materials)
  - [MM_Surge](#mm_surge)
  - [MM_SimpleGlow](#mm_simpleglow)
  - [MM_SolidColor](#mm_solidcolor)
- [VFX](#vfx)
  - [Start](#start)
  - [Vertical_lines](#vertical_lines)
  - [Fontain](#fontain)
  - [Glow](#glow)
  - [Spiral](#spiral)
## Materials
### MM_Surge

![Unreal_Surge](https://github.com/WhateversStudio/IndikatorFest_VFX_README/assets/36862146/1b531638-a099-4fb5-9777-0c6dfc93dded)
![Unity_Surge](https://github.com/WhateversStudio/IndikatorFest_VFX_README/assets/36862146/10af29bd-ca60-49bd-a0e0-6ca1d3592250)

<details>

Translucent Unlit / Sprite Unlit Shader Graph

![Surge_Shader](https://github.com/WhateversStudio/IndikatorFest_VFX_README/assets/36862146/3f0b4bed-6a6d-4761-911e-675ad7eb021d)

#### Output Color
<!--
![Surge_Color_UV](https://github.com/moskalentarium/IndikatorFest/assets/36862146/32d570b2-b6f0-4e75-a324-f55c47bb1f4d)

![Surge_Color_UV-Scale](https://github.com/moskalentarium/IndikatorFest/assets/36862146/fb7c768b-6870-4d83-91ae-1edb3ce56aa0)

![Surge_Color_Texture](https://github.com/moskalentarium/IndikatorFest/assets/36862146/80a35c72-7cf1-440e-bed5-de4938122eb9)

![Surge_Color_Texture-Rerout](https://github.com/moskalentarium/IndikatorFest/assets/36862146/a48e8b65-a8e3-40e2-b1fb-e4674dd9cf2c)
-->
Curve Atlas Row Parameter: Мы хотим создать свой градиент из кривый внутри движка - мы создаем ColorCurve. Чтобы градиент/кривую конвертировать в текстуру - мы создаем CurveAtlas. Этот атлас может в себе хранить множество кривых, мы ограничимся одной. Теперь, чтобы атлас использовать в материале, мы используем нод Curve Atlas Row Parameter. Сначала добавляем атлас, потом кривую
Sample Gradient
![Surge_Color_CurveAtlasRowParam](https://github.com/WhateversStudio/IndikatorFest_VFX_README/assets/36862146/708a0872-01b0-41ce-ab40-c7101cb4ced7)<!--
![Surge_Color_Output-Rerout](https://github.com/moskalentarium/IndikatorFest/assets/36862146/ce4a5af7-94f2-4085-8133-c12dc5f5b626)
-->
![Surge_Color_frame](https://github.com/WhateversStudio/IndikatorFest_VFX_README/assets/36862146/b726cf59-fb2f-4006-96e3-3e3f309ebdfc)
![Unity_OutputColor](https://github.com/WhateversStudio/IndikatorFest_VFX_README/assets/36862146/4887bf0d-4869-4e12-9d4e-263a9c032a0b)

#### UV Mask
<!--
![Surge_Mask_R](https://github.com/moskalentarium/IndikatorFest/assets/36862146/1c818a75-b99b-4f18-b5e0-db44a7524720)

![Surge_Mask_Subtract](https://github.com/moskalentarium/IndikatorFest/assets/36862146/601deddc-cce3-438b-9e74-05edc04f0f07)

![Surge_Mask_Abs](https://github.com/moskalentarium/IndikatorFest/assets/36862146/7f765ff8-05d8-477c-8346-4f0bf33ad22b)

![Surge_Mask_OneMinus](https://github.com/moskalentarium/IndikatorFest/assets/36862146/dba2c8bd-01be-4ece-b0a9-050324787e71)

![Surge_Mask_PowerSaturate](https://github.com/moskalentarium/IndikatorFest/assets/36862146/271e2acb-45a4-4f8e-a929-6eff04789059)

![Surge_Mask_Border](https://github.com/moskalentarium/IndikatorFest/assets/36862146/9f5af124-f547-4ba8-8685-e74940f6db41)

![Surge_Mask_U-and-V](https://github.com/moskalentarium/IndikatorFest/assets/36862146/a2b45686-6e42-4540-8ccc-beafd7f9bfb8)
-->
Component Mask / Split
One Minus / Invert Colors
![Surge_Mask_Combine](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/06ff597e-e967-4a20-ae46-bb5e9efcba9a)

![Unity_UV-Mult](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/f884a04a-f5d5-461e-8bd0-bba1d0e3bda2)

#### Texture Mask
<!--
![Surge_TextureMask_UV](https://github.com/moskalentarium/IndikatorFest/assets/36862146/a10c9e2a-10d5-4d49-9653-72bf685361d2)
-->
![Surge_TextureMask_DynamicParam](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/52c7cfe6-2445-4468-9017-5786c218c82b)
<!--
![Surge_TextureMask_DynamCombRerout](https://github.com/moskalentarium/IndikatorFest/assets/36862146/aeeef4ca-a45d-4f76-979f-10a5cdecf675)

![Surge_TextureMask_UV-Add](https://github.com/moskalentarium/IndikatorFest/assets/36862146/c8c868cc-4d41-460b-81da-0978709c008f)

![Surge_TextureMask_TextAdj](https://github.com/moskalentarium/IndikatorFest/assets/36862146/880e606b-29b1-48b6-a401-a43ff42b3f68)

![Surge_TextureMask_Smoothstep](https://github.com/moskalentarium/IndikatorFest/assets/36862146/67feaa1d-6447-4701-a6d7-8ff33877c3fa)

![Surge_TextureMask_Saturate](https://github.com/moskalentarium/IndikatorFest/assets/36862146/e43fb1f7-5150-4012-a418-ee2a4da2c45a)
-->
Lerp vs SmoothStep: первый проводит линейную интерполяцию, второй - по кривой
![Surge_TextureMask_Border](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/e2a745d2-9e61-4d66-ab0f-f59e60f45c2a)

![Unity_Texture-Mask](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/523d5806-c4cc-45c4-8ddc-e14e77c37b48)

#### Combining
<!--
![Surge_Comb_Mult](https://github.com/moskalentarium/IndikatorFest/assets/36862146/9bf2a4aa-e527-4782-a88f-3fb4f09ae011)
-->
![Surge_Comb_16SatMult](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/daa92b0f-c256-4504-84a3-f0a0dd2272a5)

![Unity_Comb1](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/b3127a5b-f36a-4dee-9d78-cb8949abf743)

<!--
![Surge_Fresnel_Base](https://github.com/moskalentarium/IndikatorFest/assets/36862146/cfd16be3-a758-40da-b036-e54985302cb7)

![Surge_Fresnel_OneMinus](https://github.com/moskalentarium/IndikatorFest/assets/36862146/0ba8c1c8-af1e-4a7e-b4f5-aa5f6ef492fe)

![Surge_Fresnel_Power](https://github.com/moskalentarium/IndikatorFest/assets/36862146/3ed8899f-72df-495f-bfd3-92ad37b5c38d)
-->
![Surge_Comb_Fresnel](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/b9478383-d9be-40ab-b536-8bed234f9b74)

![Unity_fresnel](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/b1003ffc-5109-4657-802c-62c81c658ee3)
<!--
![Surge_Comb_Depth](https://github.com/moskalentarium/IndikatorFest/assets/36862146/1cfb5a7d-b0e1-43f1-82c7-316fe586a828)

![Surge_Shader_EmissOpacity](https://github.com/moskalentarium/IndikatorFest/assets/36862146/9070b98e-000d-4d7a-82c2-145ab5dc7e6d)

![Surge_Refr_Lerp](https://github.com/moskalentarium/IndikatorFest/assets/36862146/5c50c5b7-0e8c-4895-8f81-755ffe9b8867)
-->
Depth Fade: когда полупрозрачный объект пересекается с другим объектом - между ними появляется резкий переход. Depth Fade маска, которая смотрит вглубь объекта и позволяет смягчить швы или менять параметры в зависимости от грубины

Refraction / IOR

![Surge_Refr_Refr](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/8b80aa78-31d9-4e6e-bb25-4a50062c39f9)

</details>

### MM_SimpleGlow

<details>
  
<!--
![Glow_RadialExpon](https://github.com/moskalentarium/IndikatorFest/assets/36862146/95ab6ed0-2e67-42a4-95cc-22bbdecee7fd)
-->
![RadialGradient](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/e4cc7c6d-7d1c-4bec-ae2a-1bed8742a900)
<!--
![Glow_Emissive](https://github.com/moskalentarium/IndikatorFest/assets/36862146/19a0535d-5f8e-4240-9b27-68055d647369)
![Glow_Opacity](https://github.com/moskalentarium/IndikatorFest/assets/36862146/20f8a326-d9a8-4a7e-acb3-08bcedb9f059)
-->
![SimpleGlow](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/99bd428d-6afb-43f9-91cc-7264bc4ef20a)

![SimpleGlowUnity](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/8747cc5c-08f7-4479-ae2a-0cc79546a221)

</details>

### MM_SolidColor

<details>

![SolidColor](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/82427d5b-f787-449e-bb73-7c78449fbd94)

</details>

[Back to top](#indikatorfest)
## VFX

[Back to top](#indikatorfest)

### Start

<details>
  
Интерфейс Niagara:
- Слева сам эффект
- В центре находится рабочая область со столбиками эмиттеров
- Справа - детали и пункты выбранной ноды частиц
- Внизу настройки воспроизведения

Остальное пока не нужно и не важно)
![Niagara1](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/3a5e67b9-705c-47ee-adb1-8a511f9f0d65)

Настройки системы (распространяются на все эмиттеры)

![Niagara2](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/9ea61d6f-5f5b-414a-9e0d-377739603f05)

</details>

### Vertical_lines

<details>
  
Стартанем с дефолтного эмиттера фонтана. К нему сделаем материал Solid Color. Посмотрим, как задается цвет в эмиттере

![Niagara3](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/d24d93cc-92ba-4413-b7ab-f45472ecf9cf)

Настройки 1

![Niagara4](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/bf87aa11-b5ff-4893-92f8-3fd609cba098)

Solid Color

![Niagara5](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/6cfc6ba3-3311-44bb-b2de-ac69b3094ab6)

Настройки 2

![Niagara6](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/b5d70911-66f3-4ff8-aa2b-ffc056c6da41)

Sptite render

![Niagara7](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/c4bf8dff-7143-4470-b83b-924874e7fee8)

</details>

### Fontain
Частички кружащиеся

<details>

Настройки 1
![Niagara8](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/77342e73-1cfe-451d-abe7-6d15aefa1663)

Настройки 2
![Niagara9](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/eca920f0-2f17-40f3-9bcf-716669ce40d4)

Sptite render

![Niagara10](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/a49c5ba2-b83b-4c54-9be2-ff4a8fadb793)

</details>

### Glow

<details>

Настройки 1

![Niagara11](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/d559d787-ce73-4da4-9258-9e3c3f569c17)

Настройки 2

![Niagara12](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/eb136138-4bc3-455a-a837-e13062a2e949)

</details>

### Spiral
Это у нас мэш-партикл

![Niagara13](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/fc25ba8c-ff32-47cd-9141-ffd9cf598422)

<details>

Настройки 1

![Niagara14](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/25cceda3-da55-4b64-a2ea-bd235f425afa)

Настройки 2

![Niagara15](https://github.com/moskalentarium/IndikatorFest_VFX/assets/36862146/6802505f-ef91-4a4a-ab18-820cfb220755)

</details>
