# Depth-Estimation
This project is my own implementation of Unsupervised Monocular Depth Estimation with Left-Right Consistency [paper](https://arxiv.org/pdf/1609.03677.pdf) by C. Godard, O. M. Aodha and G. J. Brostow.

![result](https://user-images.githubusercontent.com/70597091/126903011-3624c264-d39f-4852-9a2c-1d512b34f2ed.gif)

# Overview

![Screenshot from 2021-07-25 20-11-08](https://user-images.githubusercontent.com/70597091/126903119-aee874e8-0ddf-42c9-ba16-48a1a31ecfd4.png)

The above picture shows the model used in this project. [EfficientNet B4](https://arxiv.org/pdf/1905.11946) model is used as a backbone for transfer learning which helps in reducing the training time.

![Screenshot from 2021-07-25 20-15-44](https://user-images.githubusercontent.com/70597091/126903262-58d7316d-0c6e-4c2a-98c2-e744efd23cea.png)

For training the model above loss function is used which is taken from the Left Right Consistency paper mentioned above. It also uses image resampling (bilinear sampler) introduced in the Spatial Transformer Network [paper](https://arxiv.org/pdf/1506.02025.pdf).

# Requirements
The model in this project was trained and tested on GPU (NVIDIA GTX 1650 4GB) powered laptop.

Some dependencies used in the project are:
1. Numpy v1.19.2
2. Tensorflow v2.3
3. Python v3.8.5
4. Jupyter Notbook v6.2.0
5. Matplotlib

# Training
For training model download the kitti stereo dataset from their [website](http://www.cvlibs.net/datasets/kitti/eval_scene_flow.php?benchmark=stereo) and place the left and right image in the same folder in which main file is. Then open the main file in Jupyter Notebook and run all the cells.

# Trying Out

If you only want to try out the model then download the weight from [here](https://drive.google.com/drive/folders/16yU6fTV4dI2PQgXt8uNQGHjxFHNstHxZ?usp=sharing). Put the weight in the same folder with main file then run all cells except the one which has ```NUM_EPOCHS=100``` at the starting.
