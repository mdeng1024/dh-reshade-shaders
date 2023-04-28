# dh-reshade-shaders
Shaders for ReShade injector

## DH_UBER_RT
This shader is an All-in-one "Screen Space Ray Tracing" shader.
It produce Global Illumination, Ambiant Occlusion and Reflections in a highly customizable little package.

[Comparison](https://imgsli.com/MTc0MzY1)

Global Illumination layer:
![DH_UBER_RT_GI](screenshots/dh_uber_rt/1-dh_uber_rt-GI.jpg?raw=true "DH_UBER_RT GI")
Ambiant Occlusion layer:
![DH_UBER_RT_AO](screenshots/dh_uber_rt/2-dh_uber_rt-AO.jpg?raw=true "DH_UBER_RT AO")
Reflection layer:
![DH_UBER_RT_SSR](screenshots/dh_uber_rt/3-dh_uber_rt-SSR.jpg?raw=true "DH_UBER_RT SSR")
Everything applied:
![DH_UBER_RT_ON](screenshots/dh_uber_rt/4-dh_uber_rt-on.jpg?raw=true "DH_UBER_RT ON")


## DH_Lain
This shader tries to reproduce the design of the shadows from the Anime "Serial Experiment Lain".

For example :
### Half-life
![DH_Lain](screenshots/dh_lain/hl_original.png?raw=true "DH_Lain")
![DH_Lain](screenshots/dh_lain/hl_lain.png?raw=true "DH_Lain")



## DH_Anime
This shader can be used to create drawing/anime/manga effects :
- lining
- shading
- saturation

For example :
![Skyrim - DH_Anime](screenshots/dh_anime/TESV%202019-11-05%2013-54-50.png?raw=true "Skyrim - DH_Anime")
![Skyrim - DH_Anime](screenshots/dh_anime/TESV%202019-11-05%2013-55-17.png?raw=true "Skyrim - DH_Anime")
![Skyrim - DH_Anime](screenshots/dh_anime/TESV%202019-11-05%2013-56-34.png?raw=true "Skyrim - DH_Anime")
![Skyrim - DH_Anime](screenshots/dh_anime/TESV%202019-11-05%2013-57-14.png?raw=true "Skyrim - DH_Anime")


## DH_Undither
This shader reduces dithering.
It doesn't use Depth Buffer so it can be used with DosBox in old games.

For example :
### Little Big Adventure 2
![DH_Undither](screenshots/dh_undither/dh_undither1.png?raw=true "DH_Undither")
![DH_Undither](screenshots/dh_undither/dh_undither2.png?raw=true "DH_Undither")


## DH_Uniformity_correction
This shader tries to correct screen uniformity and/or DSE (Dirty Screen Effect)

### HOW TO

1. Run a game with ReShade and the shader enabled, check "Solid color", set "Correction" to 0 and set "Brightness" to a value that shows imperfections the best

2. Take a photo of the screen in the dark before correction
![Photo of the screen before correction](screenshots/dh_uniformity_correction/0_without_correction.jpg?raw=true "Photo of the screen before correction")

3. From this, create a texture of the defects by cropping and spreading histogram in a image editor (like Photoshop or Paint.net)
![Defects of the screen](screenshots/dh_uniformity_correction/1_dh_uniformity_correction.jpg?raw=true "Defects of the screen")
Save this file in Textures folder with the name "dh_uniformity_correction.bmp"

4. Restart the game with the new texture and increase "Correction" until you don't see imperfections anymore. Finally uncheck "Solid color"
No correction test (photo and amplified contrasts for visibility):
![photo](screenshots/dh_uniformity_correction/2_without_correction_test.jpg?raw=true "photo")
![amplified contrasts for visibility](screenshots/dh_uniformity_correction/2_without_correction_test_amplified.jpg?raw=true "amplified contrasts for visibility")

Correction set to 0.20 :
![photo](screenshots/dh_uniformity_correction/3_correction_20.jpg?raw=true "photo")
![amplified contrasts for visibility](screenshots/dh_uniformity_correction/3_correction_20-amplified.jpg?raw=true "amplified contrasts for visibility")

Correction set to 0.25 :
![photo](screenshots/dh_uniformity_correction/4_correction_25.jpg?raw=true "photo")
![amplified contrasts for visibility](screenshots/dh_uniformity_correction/4_correction_25-amplified.jpg?raw=true "amplified contrasts for visibility")

5. ????

6. Profit !

### Example on a TV subject to DSE
![DSE_correction_OFF](screenshots/dh_uniformity_correction/DSE_paperben_uniformity-correction-off.jpg?raw=true "DSE_correction_OFF")
![DSE_correction_ON](screenshots/dh_uniformity_correction/DSE_paperben_uniformity-correction-on.jpg?raw=true "DSE_correction_ON")
Credits to *paperben*.


