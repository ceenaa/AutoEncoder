# Image Compression Autoencoder
This repository contains an implementation of an Autoencoder for image compression using the MNIST dataset. The autoencoder is built using PyTorch and demonstrates how to encode images into a lower-dimensional representation and then decode them back to their original form.

# Overview
Autoencoders are a type of neural network used to learn efficient codings of input data. The model consists of two main parts:

* Encoder: Compresses the input image into a lower-dimensional latent representation.
* Decoder: Reconstructs the original image from the compressed latent representation.
In this project, the autoencoder is trained on the MNIST dataset, which consists of handwritten digit images. The goal is to compress these images while retaining as much information as possible for accurate reconstruction.

![image](https://github.com/user-attachments/assets/fb93cd9d-a141-4b9a-a9b6-5fb591d30a1b)


# Model Architecture
The autoencoder is composed of convolutional layers for both the encoder and decoder. Below is a brief overview of the architecture:

* Encoder
The `encoder` compresses a `1x28x28` input image down to a `64x1x1` latent space representation.
It uses four convolutional layers with ReLU activations.
* Decoder
The `decoder` reconstructs the `64x1x1` latent space back to the original `1x28x28` image.
It uses four transpose convolutional layers with ReLU activations.
* Loss Function
The model is trained using Mean Squared Error (MSE) loss, which measures the difference between the input image and its reconstruction.

# Usage
### Training
To train the autoencoder on the MNIST dataset:

1. Ensure that the dataset is downloaded by PyTorch.
2. The model is trained for 15 epochs by default, with a batch size of 32. The training loop calculates the loss and updates the model weights.
Visualizing Reconstruction
Before training, the model is used to visualize the reconstruction of the first 10 images from the MNIST dataset. This allows you to see how well an untrained model performs.

# Results
After training, the model should be able to reconstruct the input images with minimal loss. The difference between the original images and their reconstructions can be observed to evaluate the model's performance.

### Before training
![image](https://github.com/user-attachments/assets/4316a9a6-9e3c-4fff-93ae-ea883eaa1220)

### After only 15 epoch
![image](https://github.com/user-attachments/assets/d14b7469-d635-4ece-9ebd-a8ae170dc1ab)

