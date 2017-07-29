# Convolutional Neural Network trained on CIFAR-10 - Learning Rate Schedule and Adaptive Learning


## What is in this repo

*CIFAR10-lrate.ipynb*

* In this notebook, I use LearningRateScheduler in Keras to create common learning rate decay schedules such as time-based decay, step decay and exponential decay. This method can be generalised to create any custom schedules. I also compare the  the perfromance with adaptive gradient descent algorithms, including Adagrad, Adadelta, RMSprop and Adam.

* My blog post discussing how to use Keras LearningRateScheduler to create custom learning rate schedules and compare the perfromance with adaptive gradient descent algorithms : [Image Augmentation for Deep Learning — Histogram Equalization](https://medium.com/towards-data-science/image-augmentation-for-deep-learning-histogram-equalization-a71387f609b2)

![plot](/3-CIFAR10-lrate/compare-accuracy.jpg)

