# Generative-Adversarial-Networks-GANs-

## Introduction
Yann LeCun described it as “the most interesting idea in the last 10 years in Machine Learning”. And, indeed, Generative Adversarial Networks (GANs for short) have had a huge success since they were introduced in 2014 by Ian J. Goodfellow and co-authors. 
Generative Adversarial Networks belong to the set of generative models. It means that they are able to produce / to generate new content. Naturally, this ability to generate new content makes GANs look a little bit “magic”, at least at first sight. 

## Generative models

We try to generate very complex random variables ... 

Suppose that we are interested in generating black and white square images of dogs with a size of n by n pixels. We can reshape each data as a N=nxn dimensional vector (by stacking columns on top of each others) such that an image of dog can then be represented by a vector. However, it doesn’t mean that all vectors represent a dog once shaped back to a square! So, we can say that the N dimensional vectors that effectively give something that look like a dog are distributed according to a very specific probability distribution over the entire N dimensional vector space (some points of that space are very likely to represent dogs whereas it is highly unlikely for some others). In the same spirit, there exists, over this N dimensional vector space, probability distributions for images of cats, birds and so on.

__Then, the problem of generating a new image of dog is equivalent to the problem of generating a new vector following the “dog probability distribution” over the N dimensional vector space. So we are, in fact, facing a problem of generating a random variable with respect to a specific probability distribution.__

## Generative Matching Networks

So our problem of generating a new image of dog can be rephrased into a problem of generating a random vector in the N dimensional vector space that follows the “dog probability distribution” and we have suggested to use a transform method, with a neural network to model the transform function. 
Now, we still need to train (optimise) the network to express the right transform function. For this there can be two different training methods: a direct one and an indirect one. The direct training method consists in comparing the true and the generated probability distributions and backpropagating the difference (the error) through the network. This is the idea that rules Generative Matching Networks (GMNs). For the indirect training method, we do not directly compare the true and generated distributions. Instead, we train the generative network by making these two distributions go through a downstream task chosen such that the optimisation process of the generative network with respect to the downstream task will enforce the generated distribution to be close to the true distribution. This last idea is the one behind Generative Adversarial Networks (GANs). 
