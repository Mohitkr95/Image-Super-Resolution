# IMAGE SUPER RESOLUTION

![](https://raw.githubusercontent.com/Mohitkr95/Image-Super-Resolution/master/Images/teaser%20(1).png)

The project is inspired and learned from the Course **Learn Machine Learning By Building Projects** on [Eduonix](https://www.eduonix.com/learn-machine-learning-by-building-projects)

The goal of super-resolution (SR) is to recover a high-resolution image from a low-resolution input, or as they might say on any modern crime show, enhance!
The authors of the SRCNN describe their network, pointing out the equivalence of their method to the sparse-coding method4, which is a widely used learning method for image SR. This is an important and educational aspect of their work, because it shows how example-based learning methods can be adapted and generalized to CNN models.
The SRCNN consists of the following operations1:
1. Preprocessing: Up-scales LR image to desired HR size.
2. Feature extraction: Extracts a set of feature maps from the up-scaled LR image.
3. Non-linear mapping: Maps the feature maps representing LR to HR patches.
4. Reconstruction: Produces the HR image from HR patches.

![](https://raw.githubusercontent.com/Mohitkr95/Image-Super-Resolution/master/Images/0_slDQDolF8CGteF4R.png)

To accomplish this goal, we will be deploying the super-resolution convolution neural network (SRCNN) using Keras. This network was published in the paper, “Image Super-Resolution Using Deep Convolutional Networks” by Chao Dong, et al. in 2014. You can read the full paper at https://arxiv.org/abs/1501.00092.

As the title suggests, the SRCNN is a deep convolutional neural network that learns the end-to-end mapping of low-resolution to high-resolution images. As a result, we can use it to improve the image quality of low-resolution images. To evaluate the performance of this network, we will be using three image quality metrics: peak signal to noise ratio (PSNR), mean squared error (MSE), and the structural similarity (SSIM) index.

In brief, with better SR approach, we can get a better quality of a larger image even we only get a small image originally.

![](https://raw.githubusercontent.com/Mohitkr95/Image-Super-Resolution/master/Images/1_FzN1KFBv_q0IramC4nxHRw.png)

Furthermore, we will be using OpenCV, the Open Source Computer Vision Library. OpenCV was originally developed by Intel and is used for many real-time computer vision applications. In this particular project, we will be using it to pre and post process our images. As you will see later, we will frequently be converting our images back and forth between the RGB, BGR, and YCrCb color spaces. This is necessary because the SRCNN network was trained on the luminance (Y) channel in the YCrCb color space.

## The SRCNN Network

![](https://raw.githubusercontent.com/Mohitkr95/Image-Super-Resolution/master/Images/1_mZJO-i6ImYyXHorv4H1q_Q.png)
