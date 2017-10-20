# Theory and applications of marker-based augmented reality

definition: AR, in computer programming, a process of combining 
            or 'augmenting' video or photographic displays by overlaying
            the images with useful computer-generated data
    - real time system

## Terminology

        |----------------mixed-reality----------------|
        |                                             |
    |_____________________________________________________|
      real        augmented        augmented      virtual
      env.        reality           virtuality     env.

|--------|  |-------|  |-------------------------------------------|
| camera |->| image |->|          Computer                         |
|--------|  |-------|  | |------------------|  |-----------------| | 
                       | | capturing module |->| tracking module | |
                       | |------------------|  |-----------------| |
                       |          |                    |           |
                       |          |                    |           |
                       |         \|/                  \|/          |
                       |    |--------------------------------|     |
                       |    |      rendering module          |     |
                       |    |--------------------------------|     |
                       |                   /|\                     |
                       |                    |                      |
                       |        |--------------------|             |
                       |        | virtual components |             |
                       |        |--------------------|             |
                       ---------------------------------------------
                                                         |
                                                        \|/
                                    |---------|  |-----------------|
                                    | display |<-| augmented image |
                                    |---------|  |-----------------|


NOTE: **the tracking** module is the heart of the augmented reality system 
    since it calculates the relative pose of the camera in real time. 

**pose** (def): six degrees of freedom (DOF) position, the 3D location and 3D 
    orientation of an object

**The rendering module**: draw the virtual image on top of the camera image.
The trick in augmented reality is to use a virtual camera identical to the 
system's real camera. This way the virtual objects in the scene are projcted
in the same way as real objects and the result is convincing. To be able to mimic
the real camera, the system needs to know the optical characteristics of the camera.
The process of identifying these characteristics is called **camera calibration**.