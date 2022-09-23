# vit_cifar10

This example implements the Vision Transformer (ViT) model by Alexey Dosovitskiy et al. for image classification, and demonstrates it on the CIFAR-10 dataset. The ViT model applies the Transformer architecture with self-attention to sequences of image patches, without using convolution layers.

![image](https://github.com/ajiehung/vit_cifar10/blob/main/images/vit_model.png)

When Using cifar10 dataset,the image shape are (32,32) with 50000 train images and 10000 test images.

And we set the patches with 8 by image size is 32
    image_size = 32 
	patch_size = 8
So we can see each paych have (8,8) and get 4x4 = 16 patches

original cifar10 image
![image](https://github.com/ajiehung/vit_cifar10/blob/main/images/original_img.png)

patches cifar image
![image](https://github.com/ajiehung/vit_cifar10/blob/main/images/patches_img.png)
