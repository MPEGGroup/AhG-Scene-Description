# AhG Scene Description

This repository collects relevant examples of scene description
tools and application in the context of the AhG on Scene Description.


## Relevant links

These is an unsorted list of tools, libraries and specifications relevant to the topic of scene descriptions.
Further work is needed to organize this list and differentiate them by functionalities.

- https://immersive-web.github.io/webxr/
- http://www.openscenegraph.org/
- https://aframe.io/
- https://www.babylonjs.com/
- https://threejs.org/
- https://aws.amazon.com/sumerian/

## Examples

### 360 video background

#### A-Frame

Demo: https://aframe-360-video-example.glitch.me/

```html
<!-- Specify our scene. -->
<a-scene>
  <!-- The original example also has this 180 degree rotation, to appear to be going forward. -->
  <a-videosphere rotation="0 180 0" src="#video" 
                 play-on-window-click
                 play-on-vrdisplayactivate-or-enter-vr>
  </a-videosphere>
  
  ...

  <!-- Wait for the video to load. -->
  <a-assets>
    <!-- Single source video. -->
    <video id="video" style="display:none" 
           autoplay loop crossorigin="anonymous" playsinline webkit-playsinline>
      <!-- MP4 video source. -->
      <source type="video/mp4"
           src="https://ucarecdn.com/fadab25d-0b3a-45f7-8ef5-85318e92a261/" />
    </video>
  </a-assets>
</a-scene>
```

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
