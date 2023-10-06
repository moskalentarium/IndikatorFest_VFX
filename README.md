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

![Unreal_Surge](https://github.com/moskalentarium/IndikatorFest/assets/36862146/960af760-2965-4003-afec-965911d8fec5)

![Unity_Surge](https://github.com/moskalentarium/IndikatorFest/assets/36862146/b67cc3f3-c70f-4b36-8926-9f5eddbea099)

<details>

Translucent Unlit / Sprite Unlit Shader Graph

![Surge_Shader](https://github.com/moskalentarium/IndikatorFest/assets/36862146/3974a39c-5f47-415c-8af2-59f6880a789c)

#### Output Color
<!--
![Surge_Color_UV](https://github.com/moskalentarium/IndikatorFest/assets/36862146/32d570b2-b6f0-4e75-a324-f55c47bb1f4d)

![Surge_Color_UV-Scale](https://github.com/moskalentarium/IndikatorFest/assets/36862146/fb7c768b-6870-4d83-91ae-1edb3ce56aa0)

![Surge_Color_Texture](https://github.com/moskalentarium/IndikatorFest/assets/36862146/80a35c72-7cf1-440e-bed5-de4938122eb9)

![Surge_Color_Texture-Rerout](https://github.com/moskalentarium/IndikatorFest/assets/36862146/a48e8b65-a8e3-40e2-b1fb-e4674dd9cf2c)
-->
Curve Atlas Row Parameter: Мы хотим создать свой градиент из кривый внутри движка - мы создаем ColorCurve. Чтобы градиент/кривую конвертировать в текстуру - мы создаем CurveAtlas. Этот атлас может в себе хранить множество кривых, мы ограничимся одной. Теперь, чтобы атлас использовать в материале, мы используем нод Curve Atlas Row Parameter. Сначала добавляем атлас, потом кривую
Sample Gradient
![Surge_Color_CurveAtlasRowParam](https://github.com/moskalentarium/IndikatorFest/assets/36862146/aad7af0b-b245-48e4-9451-ab1252fc89e3)
<!--
![Surge_Color_Output-Rerout](https://github.com/moskalentarium/IndikatorFest/assets/36862146/ce4a5af7-94f2-4085-8133-c12dc5f5b626)
-->
![Surge_Color_frame](https://github.com/moskalentarium/IndikatorFest/assets/36862146/b8d625f3-6c77-489a-823a-3856baa8bfeb)

![Unity_OutputColor](https://github.com/moskalentarium/IndikatorFest/assets/36862146/897fb9e0-e9f7-4487-92d6-6b8ce3f794d9)

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
![Surge_Mask_Combine](https://github.com/moskalentarium/IndikatorFest/assets/36862146/dd3b210f-9e0e-46d3-91dc-03fa01e53984)

![Unity_UV-Mult](https://github.com/moskalentarium/IndikatorFest/assets/36862146/4839a0aa-88b3-4f52-ac8d-1aa99e074587)

#### Texture Mask
<!--
![Surge_TextureMask_UV](https://github.com/moskalentarium/IndikatorFest/assets/36862146/a10c9e2a-10d5-4d49-9653-72bf685361d2)
-->
![Surge_TextureMask_DynamicParam](https://github.com/moskalentarium/IndikatorFest/assets/36862146/0c66b029-3748-4e9d-a3e3-e369f9db3199)
<!--
![Surge_TextureMask_DynamCombRerout](https://github.com/moskalentarium/IndikatorFest/assets/36862146/aeeef4ca-a45d-4f76-979f-10a5cdecf675)

![Surge_TextureMask_UV-Add](https://github.com/moskalentarium/IndikatorFest/assets/36862146/c8c868cc-4d41-460b-81da-0978709c008f)

![Surge_TextureMask_TextAdj](https://github.com/moskalentarium/IndikatorFest/assets/36862146/880e606b-29b1-48b6-a401-a43ff42b3f68)

![Surge_TextureMask_Smoothstep](https://github.com/moskalentarium/IndikatorFest/assets/36862146/67feaa1d-6447-4701-a6d7-8ff33877c3fa)

![Surge_TextureMask_Saturate](https://github.com/moskalentarium/IndikatorFest/assets/36862146/e43fb1f7-5150-4012-a418-ee2a4da2c45a)
-->
Lerp vs SmoothStep: первый проводит линейную интерполяцию, второй - по кривой
![Surge_TextureMask_Border](https://github.com/moskalentarium/IndikatorFest/assets/36862146/145c3a19-e839-4d37-885f-d353d4fa4930)

![Unity_Texture-Mask](https://github.com/moskalentarium/IndikatorFest/assets/36862146/11a88716-553d-4b26-9428-f8d445d41329)

#### Combining
<!--
![Surge_Comb_Mult](https://github.com/moskalentarium/IndikatorFest/assets/36862146/9bf2a4aa-e527-4782-a88f-3fb4f09ae011)
-->
![Surge_Comb_16SatMult](https://github.com/moskalentarium/IndikatorFest/assets/36862146/2fda9784-86b9-484c-937d-43a2ba641366)

![Unity_Comb1](https://github.com/moskalentarium/IndikatorFest/assets/36862146/ac0b8a8c-6feb-495c-b1c7-86e0ac0087f1)
<!--
![Surge_Fresnel_Base](https://github.com/moskalentarium/IndikatorFest/assets/36862146/cfd16be3-a758-40da-b036-e54985302cb7)

![Surge_Fresnel_OneMinus](https://github.com/moskalentarium/IndikatorFest/assets/36862146/0ba8c1c8-af1e-4a7e-b4f5-aa5f6ef492fe)

![Surge_Fresnel_Power](https://github.com/moskalentarium/IndikatorFest/assets/36862146/3ed8899f-72df-495f-bfd3-92ad37b5c38d)
-->
![Surge_Comb_Fresnel](https://github.com/moskalentarium/IndikatorFest/assets/36862146/5442759c-26e1-4737-aa0c-fdcf51be3aca)

![Unity_fresnel](https://github.com/moskalentarium/IndikatorFest/assets/36862146/76effad6-6888-4605-96b7-599bc3f17b09)
<!--
![Surge_Comb_Depth](https://github.com/moskalentarium/IndikatorFest/assets/36862146/1cfb5a7d-b0e1-43f1-82c7-316fe586a828)

![Surge_Shader_EmissOpacity](https://github.com/moskalentarium/IndikatorFest/assets/36862146/9070b98e-000d-4d7a-82c2-145ab5dc7e6d)

![Surge_Refr_Lerp](https://github.com/moskalentarium/IndikatorFest/assets/36862146/5c50c5b7-0e8c-4895-8f81-755ffe9b8867)
-->
Depth Fade: когда полупрозрачный объект пересекается с другим объектом - между ними появляется резкий переход. Depth Fade маска, которая смотрит вглубь объекта и позволяет смягчить швы или менять параметры в зависимости от грубины

Refraction / IOR

![Surge_Refr_Refr](https://github.com/moskalentarium/IndikatorFest/assets/36862146/e2b1121d-0687-4a95-b930-3288763e91a2)


</details>

### MM_SimpleGlow

<details>
  
<!--
![Glow_RadialExpon](https://github.com/moskalentarium/IndikatorFest/assets/36862146/95ab6ed0-2e67-42a4-95cc-22bbdecee7fd)
-->
![Glow_Radial](https://github.com/moskalentarium/IndikatorFest/assets/36862146/df88e336-151c-40bc-874e-da61c9d7e680)
<!--
![Glow_Emissive](https://github.com/moskalentarium/IndikatorFest/assets/36862146/19a0535d-5f8e-4240-9b27-68055d647369)
![Glow_Opacity](https://github.com/moskalentarium/IndikatorFest/assets/36862146/20f8a326-d9a8-4a7e-acb3-08bcedb9f059)
-->
![Glow_Final](https://github.com/moskalentarium/IndikatorFest/assets/36862146/6f8e3e6e-d26d-41cc-be53-25e6b747dfa8)

![Unity_SimpleGlow](https://github.com/moskalentarium/IndikatorFest/assets/36862146/f5e5d8d6-6b50-4f2d-a41f-728f17a376b4)

</details>

### MM_SolidColor

<details>

![FlatColor](https://github.com/moskalentarium/IndikatorFest/assets/36862146/cf339e5b-b260-459f-8fc9-e2db40b2515d)

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
![2023-10-03 18_07_05-Window](https://github.com/moskalentarium/IndikatorFest/assets/143734540/4c4b3a01-6767-4156-ac93-368570add53f)

Настройки системы (распространяются на все эмиттеры)

![2023-10-06 15_27_10-NS_Super-Dupper](https://github.com/moskalentarium/IndikatorFest/assets/143734540/7ba817fb-aeca-42b5-92fa-1397662e40d8)

</details>

### Vertical_lines

<details>
  
Стартанем с дефолтного эмиттера фонтана. К нему сделаем материал Solid Color. Посмотрим, как задается цвет в эмиттере
![2023-10-06 15_20_36-](https://github.com/moskalentarium/IndikatorFest/assets/143734540/10dafc12-9083-45b1-99af-8598dbdf582d)

Настройки 1

![2023-10-06 15_32_17-Window copy](https://github.com/moskalentarium/IndikatorFest/assets/143734540/a7963877-4463-47c4-bacc-ce7449471baa)

Solid Color

![2023-10-06 15_43_13-MM_FlatColor](https://github.com/moskalentarium/IndikatorFest/assets/143734540/6445b5fc-7488-4e73-9f63-054be9db42ba)

Настройки 2

![2023-10-06 15_44_37-Window copy](https://github.com/moskalentarium/IndikatorFest/assets/143734540/6f0c263e-ed23-44f1-88f0-9e46b9a415c8)

Sptite render

![2023-10-06 15_48_54-Window](https://github.com/moskalentarium/IndikatorFest/assets/143734540/c84b2407-1180-430c-903d-0f7349ddc5c9)

</details>

### Fontain
Частички кружащиеся

<details>

Настройки 1
![2023-10-06 15_32_17-Window copy](https://github.com/moskalentarium/IndikatorFest/assets/143734540/eae44978-78e1-4da3-ad6c-8bfa141d3543)

Настройки 2
![2023-10-06 15_f32_17-Window copy](https://github.com/moskalentarium/IndikatorFest/assets/143734540/e650c32b-3c55-44dd-a9d4-1302aa36b958)

Sptite render

![2023-10-06 16_38_00-Window](https://github.com/moskalentarium/IndikatorFest/assets/143734540/6c842ec3-65a0-4b7f-9a84-7060c0e77792)

</details>

### Glow

<details>

Настройки 1

![ррукр](https://github.com/moskalentarium/IndikatorFest/assets/143734540/c7ae3f42-272d-47b3-b5c3-0218622f0ece)

Настройки 2
![2023-10-06 15_32_17-мcopy](https://github.com/moskalentarium/IndikatorFest/assets/143734540/8821ce88-11ca-46a2-9455-49921f865fc6)


</details>

### Spiral
Это у нас мэш-партикл

![2023-10-06 17_31_51-Window](https://github.com/moskalentarium/IndikatorFest/assets/143734540/c6cc1164-16c2-4d13-b13a-92d695dac28a)

<details>

Настройки 1
![2023-10-06 15_32_17-Window copyккр](https://github.com/moskalentarium/IndikatorFest/assets/143734540/b298f325-be1d-47a8-9fa1-60e1c70e092a)

Настройки 2
![2023-10-06 15_32_17-Wрерindow copy](https://github.com/moskalentarium/IndikatorFest/assets/143734540/273aa7d7-3eab-4b11-892d-91e7b61316f1)

</details>
