# GANcraft: Unsupervised 3D Neural Rendering of Minecraft Worlds
Zekun Hao, Arun Mallya, Serge Belongie, Ming-Yu Liu

## Summary

This paper presents **GANcraft** a volumetric rendering (rendering of 3D world as 2D images) based approch to model a 3D
block world scene with semantic labels and render view consistent (when viewed from different camera positions) 
photorealistic images. In the absence of the paired training data,
an image to image translation model is used for generating pseudo ground truth labels 
to generate a photorealistic 3D block world.

![alt text](https://github.com/kumar-devesh/paper-summaries/blob/main/pseudo%20gt.PNG)

## Contributions

- Novel task of world to world translation problem from 
3D block world which can be intuitively constructed like in
minecraft to a realistic 3D world, the 3D extension to a 2D
image to image translation.

- Framework to train neural renderers in the absence of ground 
truth data for the realistic world to be rendered using pseudo 
ground truth labels.

- Training neural rendering architecture with adversarial losses 
and conditioning on the style image, extending 3D neural rendering
methods.

## Model

![alt text](https://github.com/kumar-devesh/paper-summaries/blob/main/overview.PNG)

GANs can successfuly map images from one 
domain to the other, without paired data but for different views 
from the same scene images generated are not consistent and 
there is a flickering problem. Neural rendering techniques solve this problem of
view consistency but cannot handle the minecraft and real
domain gap.

The model takes as input a 3D block world for which a voxel bounded 
radiance field is learned. Instead of a view dependent colour as in 
neural rendering the network outputs image features which is passed 
into a cnn renderer which converts per pixel feature map to an image.
The model is then trained on the adversarial and
perceptual losses for the generated image and the pseudo ground truth 
labels. Vertices of each voxel are assigned feature vectors which are shared 
across advacent voxels ensuring that there are no inconsistencies in 
the output.

![alt text](https://github.com/kumar-devesh/paper-summaries/blob/main/nerf%20eqn%20feature.PNG)

## Our Two Cents

