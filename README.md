# vit_cifar10

This example implements the Vision Transformer (ViT) model by Alexey Dosovitskiy et al(https://arxiv.org/abs/2010.11929). for image classification, and demonstrates it on the CIFAR-10 dataset. The ViT model applies the Transformer architecture with self-attention to sequences of image patches, without using convolution layers.

![image](https://github.com/ajiehung/vit_cifar10/blob/main/images/vit_model.png)

Note that, it is mentioned in the paper that ViTs are data-hungry architectures and the performance of ViTs even using a relatively large dataset like ImageNet without strong regularization yields accuracy a few percentages below ResNet.

When Using cifar10 dataset,the image shape are (32,32) with 50000 train images and 10000 test images.


We split the image into fixed-size image patches, linearly embed and add positional information to each patch, and feed the resulting vector sequence to a standard Transformer encoder
And we set the patches with 8 by image size is 32
    image_size = 32 
	patch_size = 8
So we can see each paych have (8,8) and get 4x4 = 16 patches

**original cifar10 image and patches cifar image**

![image](https://github.com/ajiehung/vit_cifar10/blob/main/images/original_img.png)![image](https://github.com/ajiehung/vit_cifar10/blob/main/images/patches_img.png)


After 100 num epochs training, the result show below.

Accuracy
That is, when predicting a picture, the result with the greatest probability is the correct answer, which is regarded as correct.

![image](https://github.com/ajiehung/vit_cifar10/blob/main/images/model acc.png)
![image](https://github.com/ajiehung/vit_cifar10/blob/main/images/model loss.png)


Top-5 accuracy
When predicting a picture, the top five results after the probability order contain the correct answer, which is regarded as correct.

![image](https://github.com/ajiehung/vit_cifar10/blob/main/images/top-5 acc.png)