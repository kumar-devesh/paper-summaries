# GANcraft: Unsupervised 3D Neural Rendering of Minecraft Worlds
Zekun Hao, Arun Mallya, Serge Belongie, Ming-Yu Liu

## Summary
The paper presents **GANCraft** a neural rendering based unsupervised approach to perform a world to world 
translation task which is the 3D equivalent for an image to image translation. A 3D block world input which is stored 
in the weights of a neural network and differnt views of this scene are rendered as photorealistic, view consistent 
(when viewed from different camera positions) images using volumetric rendering techniques (rendering of 3D world as 2D images).

## Contributions
- Using neural rendering techniques to make the images view consistent and the GAN architecture for translating these sematically 
labelled block world views into photorealistic rendered images.

- Unsupervised learning technique in contrast to prior methods based on neural radiance fields that require ground truth images 
to estimate the volumetric density and view dependent color.
