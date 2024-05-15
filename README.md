# Introduction
This machine learnig model generates fashion! Implementing and training a Generative adversarial network on the Fashion MNIST dataset to generate the articles of clothing.GANs are generative models that create new data instances that resemble your training data

![Image](https://miro.medium.com/v2/resize:fit:1400/1*s1P6dOC7YWqQnV-7QENVfg.png)

Here is an example of faces that are not in fact real people but rather genrated by a GAN!


# Architecture
![GAN](https://i0.wp.com/semiengineering.com/wp-content/uploads/nn3.png?fit=756%2C558&ssl=1)
GAN architecture consistes of two neural networks,The discriminator and the generator.

## Discriminator
![Discrminator](https://www.google.com/url?sa=i&url=https%3A%2F%2Ftowardsdatascience.com%2Fgan-ways-to-improve-gan-performance-acf37f9f59b&psig=AOvVaw1Ge6J4vKpHXBq8zpwsErlO&ust=1715849764495000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCLj9oNCkj4YDFQAAAAAdAAAAABAE)

An artificial neural network called a discriminator model is used in GANs to differentiate between generated and actual input.The primary goal of the discriminator is to improve the quality of the generated data by providing feedback to the generator.During training, the discriminator aims to become proficient at distinguishing between real and fake data.

## Generator
![Generator](https://www.google.com/url?sa=i&url=https%3A%2F%2Ftowardsdatascience.com%2Fdcgans-deep-convolutional-generative-adversarial-networks-c7f392c2c8f8&psig=AOvVaw2mP2Fj-Ogn1EcBcCKq6kZA&ust=1715849706976000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCOip4bSkj4YDFQAAAAAdAAAAABAE)
The generator is a neural network that takes in random noise and tries to produce samples that are indistinguishable from real data.Training a GAN involves optimizing both the generator and the discriminator simultaneously in a minimax game framework. As the generator improves at generating realistic samples, the discriminator also gets better at distinguishing real from fake samples. This dynamic interplay between the two components leads to the generator learning to produce increasingly convincing synthetic data.
This minimax game is the reason why the loss curve of GANs is typically zigzag instead of the conventional decreasing curve.

# This Model
This model aims to generate new fashion articles by generating instances of the fashion MNIST dataset. I have used a simple vanilla neural network to implement both the Genrator and discrimintor. 20000 epochs were trained for the final model.

The HDF5 files are provided in the repository for further generation of images

![OUTPUT](https://www.innodeed.com/wp-content/uploads/2022/09/code-output4-328x231.png)

# Future scope
-> Using more layers in the neural network(Which can cause vanishing/exploding gardient problem)

-> Training more epochs(Might not necesarrily lead to improvement)

# Further reading
[Original research paper](https://arxiv.org/abs/1406.2661)
