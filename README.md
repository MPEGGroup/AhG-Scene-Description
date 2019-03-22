# AhG Scene Description

This repository collects relevant examples of scene description
tools and application in the context of the AhG on Scene Description.


## Relevant links

These is an unsorted list of tools, libraries and specifications relevant to the topic of scene descriptions.
Further work is needed to organize this list and differentiate them by functionalities.

- [W3C Immersvive Web](https://www.w3.org/immersive-web/)
- [WebXR](https://immersive-web.github.io/webxr/)
- [Open Scene Graph](http://www.openscenegraph.org/)
- [A-Frame](https://aframe.io/)
- [babylon.JS](https://www.babylonjs.com/)
- [three.js](https://threejs.org/)
- [Amazon Sumerian](https://aws.amazon.com/sumerian/)

## Examples

### 360 video background

#### A-Frame

[Demo](https://mpeggroup.github.io/AhG-Scene-Description/examples/360_video_background/aframe-mp4.html)
[Code](https://github.com/MPEGGroup/AhG-Scene-Description/blob/master/examples/360_video_background/aframe-mp4.html)

Syntax:

```html
<!-- Description of the scene -->
<a-scene>
  <!-- The scene has one asset which is the 360 ERP background video -->
  <a-assets>
    <video id="videoBackground" autoplay loop crossorigin="anonymous">
      <source src="https://ucarecdn.com/fadab25d-0b3a-45f7-8ef5-85318e92a261/"></source>
    </video>
  </a-assets>

  <!-- The scene has one sphere as background and the texture links to the declared video asset -->
  <a-videosphere src="#videoBackground" rotation="0 180 0"></a-videosphere>
</a-scene>
```

### 2D video texture

#### A-Frame

[Demo](https://mpeggroup.github.io/AhG-Scene-Description/examples/2D_video_texture/aframe-mp4.html)
[Code](https://github.com/MPEGGroup/AhG-Scene-Description/blob/master/examples/2D_video_texture/aframe-mp4.html)

Syntax:

```html
<!-- Description of the scene -->
<a-scene>
  <!-- The scene has one asset which is a 2D video -->
  <a-assets>
    <video id="video" autoplay loop crossorigin="anonymous" src="http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4">
    </video>
  </a-assets>
  
  <!-- Declare a plane whose texture is the video frames -->
  <a-video src="#video" width="16" height="9" position="0 0 -10"></a-video>
</a-scene>
```

### 2D video texture with a 360 picture background

#### A-Frame

[Demo](https://mpeggroup.github.io/AhG-Scene-Description/examples/2D_video_texture_with_360_picture_background/aframe-mp4-jpeg.html)
[Code](https://github.com/MPEGGroup/AhG-Scene-Description/blob/master/examples/2D_video_texture_with_360_picture_background/aframe-mp4-jpeg.html)

Syntax:

```html
<!-- Description of the scene -->
<a-scene>
  <!-- Declare a backgound picture of the scene -->
  <a-sky src="../../assets/SMKver2-0011104.jpg" rotation="0 -130 0"></a-sky>
  <!-- The scene has one asset which is a 2D video -->
  <a-assets>
    <video id="video" autoplay loop crossorigin="anonymous" src="http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4">
    </video>
  </a-assets>
      
  <!-- Declare a plane whose texture is copied from the video frames -->
  <a-video src="#video" width="16" height="9" position="9.5 3 -10" rotation="0 -36 -0.5" scale="1.3 1.75 1"></a-video>
</a-scene>

### 2D video texture on 3D object

#### A-Frame

[Demo](https://mpeggroup.github.io/AhG-Scene-Description/examples/2D_video_texture_on_3D_object/aframe-mp4.html)
[Code](https://github.com/MPEGGroup/AhG-Scene-Description/blob/master/examples/2D_video_texture_on_3D_object/aframe-mp4.html)

Syntax:

```html
<!-- Description of the scene -->
<a-scene>
  <!-- The scene has one asset which is a 2D video -->
  <a-assets>
    <video id="video" autoplay loop crossorigin="anonymous" src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4" muted>
    </video>
  </a-assets>
      
  <!-- Declare a backgound colour of the scene (optional, just to have a better constrast with the video) -->
  <a-sky color="#6EBAA7"></a-sky>
      
  <!-- Declare a box whose texture is copied from the video frames -->
  <a-box src="#video" width="16" height="9" position="0 0 -10"></a-box>
</a-scene>
```

Credits 360 picture: https://www.flickr.com/photos/peterleth/ [creative commons](https://creativecommons.org/licenses/by/2.0/)

## Mandates
### From MPEG #125

1.	Select and document set of existing external scene description formats to be used as reference for MPEG-I system design
2.	Refine the requirements in N17747 based on the findings in mandate 1
3.	Identify relevant MPEG standardization aspects based on the above two findings 
4.	Integrate Audio requirements on Scene Graph


### From MPEG #124

1. Select and document set of existing external scene description formats to be used as reference for MPEG-I system design
2. Refine the requirements in N17747 based on the findings in mandate 1
3. Identify relevant MPEG standardization aspects based on the above two findings
