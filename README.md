# 3D web player (gltf, glb, ..) *LinksPlayer (three.js based)

### Usage: 
```
<iframe src="LinksPlayer.htm?id=1" allowfullscreen></iframe>
```
Example: https://3d-modellers.com/

Player automatically adapts to any 3D model. No input parameters needed.

Prepare model using https://github.com/AnalyticalGraphicsInc/gltf-pipeline

## V 1.1 (June 28 2019) : Exported camera support; load time and performance improvements

### Roadmap:
* Cinema4d-like navigation
* Adopt .basis image format (50% complete)
* Windows application for 3D model preparation (using gltf-pipeline) and setting player attributes.
* Advanced Cinema4D-like camera navigation
* VR AR support
* Set markers and links on 3D model

If you need additional features for $ - contact me mozg4D@gmail.com

## Cinema4D + Redshift workflow:

![Cinema4D workflow](https://github.com/mozg4D/gltf-web-player/blob/master/cinema4d_2.jpg)

* make your 3D model
* find "Bake Object..." comand in "Customize Commands"
* select objects that you want to bake and execute "Bake Objects..." command
* In "Bake Object" window deselect "illuminate" option, select desired texture resulution, set pixel border to 8 and supersampling to 1
"Bake Object" will unwrap UV's for you, press "bake" button
* Create "Redshift BakeSet" object
* Add objects that you want to bake with global illumination to "Redshift BakeSet" --> Objects
* Set desired resolution and bake

You can use Cinema4D "Bake object" comand with "illuminate" option on and skip redshift baker

## Exporting GLTF:

Use this amazing GLTF exporter by [BASEL_ABU-SINNI](https://labs.maxon.net/?p=3360/)

![Cinema4D workflow](https://github.com/mozg4D/gltf-web-player/blob/master/cinema4d_1.jpg)

* turn on "Color" channel and set it's brightness to 0
* turn on "Luminance" channel and set it's texture to recently baked one
* turn on "Reflectance" channel and set reflection and specular strenghts to 0
* Add camera (to overwrite default view angle in GLTF player)
* (7) export with "export camera" and "export to binary" options on in "GLTF export options" window

* You must export fully baked scene. Web 3D player does not have light sources, nor it provedes environment maps due to peformance and load tilme issues

If you've done everything correctly, scene in web player should look EXACTLY as in cinema4D:

![Cinema4D workflow](https://github.com/mozg4D/gltf-web-player/blob/master/result.jpg)

To speed up the development of player feel free to donate some) or to upvote features you need the most)
https://www.paypal.me/mozg4d
