# Pixel2Pixel

Official PyTorch implementation of ["Pixel2Pixel: A Pixelwise Approach for Zero-shot Single Image Denoising"](https://ieeexplore.ieee.org/document/10908805) in TPAMI 2025.

## Abstract
We propose Pixel2Pixel, a novel zero-shot image denoising framework that leverages the non-local self-similarity of images to generate a large number of training samples using only the input noisy image. This framework employs a compact convolutional neural network architecture to achieve high-quality image denoising. Given a single observed noisy image, we first aim to obtain multiple images with different noise versions. We ensure that the content remains as consistent as possible with the true signal of the noisy image while keeping the noise independent. Specifically, we construct a \emph{pixel bank} tensor, where each pixel consists of the most similar pixels from the non-local region of the noisy image. Then, multiple training samples, also known as \emph{pseudo instances}, can be derived from the pixel bank by randomly pixel sampling. By harnessing pixel-wise random sampling, Pixel2Pixel generates a large number of training pseudo instances, thus avoiding reliance on specific training data. In addition, this non-local pixel selection and random sampling strategy helps to break down the spatial correlation of real-world noise as well. Since the proposed method does not require accurate priors on the noise distribution and clean training images, it is suitable for a wide range of noise types and different noise levels, exhibiting strong generalization ability, especially in real noisy scenes. Extensive experiments across various noise types show that Pixel2Pixel outperforms existing methods.


---

## Setup

### Requirements

Our experiments are done with:

- python = 3.8.13
- pytorch = 1.11.0+cu113
- numpy = 1.21.5
- scikit-image = 0.19.2


## For Evaluation

* For evaluation on synthetic noise, run ``Pixel2Pixel_syn.py`` 

* For evaluation on real-world images, run ``Pixel2Pixel_real.py``

## Citations

  @article{ma2025pixel2pixel,
  title={Pixel2Pixel: A Pixelwise Approach for Zero-Shot Single Image Denoising},
  author={Ma, Qing and Jiang, Junjun and Zhou, Xiong and Liang, Pengwei and Liu, Xianming and Ma, Jiayi},
  journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year={2025},
  publisher={IEEE}
}
