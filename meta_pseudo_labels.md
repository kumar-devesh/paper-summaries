# Meta Pseudo Labels
Hieu Pham, Zihang Dai, Qizhe Xie, Minh-Thang Luong, Quoc V. Le, **CVPR 2021**

## Summary

The paper presents Meta Pseudo Labels a semi supervised learning approch that achieves state of the art top-1 accuracy of
90.2% on ImageNet. Pseudo Labels work by having a pair of networks, a pretrained teacher network and a student network  where the teacher network
generates pseudo labels for unlabeled images. A drawback of this approach is that if the pseudo labels are inaccurate the student learns from inaccurate data.
Meta Pseudo Labels uses a meta learning approach observing how the student network performs on the labelled dataset and sending feedback signals to train the 
meta learner, the teacher network to generate better pseudo labels.

## Contributions

- Novel task of world to world translation problem from 
3D block world which can be intuitively constructed like in
minecraft to a realistic 3D world, the 3D extension to a 2D
image to image translation.


## Methodology

Pseudo Labels trains a student model to minimize the cross entropy loss for a pseudo target label produced by
a well trained teacher network. The optimal student parameters for this optimization problem depend on the teacher network parameters via the pseudo labels.
The optimal student parameters are function of the teacher parameters. The ultimate student loss on labelled data is also a function of the teacher parameters.
the loss of student network for the labelled dataset measures the performance of the teacher network in pseudo label generation and its gradient signals can be 
used as feedback to train the teacher network.

The student network still relies on the teacher network for training with the teacher parameters being optimized in an alternating optimization procedure between the student and teacher network update.
<!--- ![alt text](https://github.com/kumar-devesh/paper-summaries/blob/main/nerf%20eqn%20feature.PNG) --->

The teacher network is trained on auxilliary tasks, augmenting the teacher's training with a supervised learning objective - training on labelled data, 
a semi-supervised objective training the teacher on unlabelled data using unsupervised domain adaptation objective on random image augumentations. 

## Results

on imagenet 10%

## Our Two Cents
- The model is the state of the art in world to world translation task in the absence of the ground truth photorealistic images for the segmentation labels of the 3D world.
- There is a still a blocky appearance to the output images because of the domain shift in the training images of the spade model and the projected images from the 3D block
world









