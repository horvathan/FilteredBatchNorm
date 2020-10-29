# FilteredBatchNorm
Filtered Batch Normalization


This repository contains code for our [Filtered Batch Normalization paper](https://arxiv.org/pdf/2010.08251.pdf)  

## Summary
It is a common assumption that the activation of different layers in neural networks follow Gaussian distribution. This distribution can be transformed using normalization techniques, such as batch-normalization, increasing convergence speed and improving accuracy. In our paper we demonstrated, that activations do not necessarily follow Gaussian distribution in all layers. Neurons in deeper layers are more selective and specific which can result extremely large, outofdistribution activations. We demonstrated that one can create more consistent mean and variance values for batch normalization during training by filtering out these activations which can further improve convergence speed and yield higher validation accuracy.

The distribution of the activations after normalization (before applying the beta and gamma parameters) in VGG16 is depicted below:
![alt text](https://raw.githubusercontent.com/horvathan/FilteredBatchNorm/main/activation_dsitributions.png)

As it can be seen, the activations closer of the logit layers contain extreme outliers, which is required to ensure sparse and clearly distinguishable activations in the logit layers.
  
