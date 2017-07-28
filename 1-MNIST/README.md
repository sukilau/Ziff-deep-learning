Submission to [Challenge #1](https://github.com/ziff/internship2017/issues/2)

# Submission to Challenge Task 1: Improve accuracy with GridSearch
 
 
## Challenge
* Demonstrate an understanding of hyperparameter optimization using sklearn GridSearch on a convolutional deep net against a simplified MNIST digit recognition by improving out-of-sample accuracy above 0.98398.
 
 
## What's in my submission

*mnist-gridsearch.ipynb*

* In this notebook, I use Keras wrapper to implement scikit-learn's GridSearch API for hyperparameter tuning of convnet. Next, I visualize the performance of GridSearch by looking into its confusion matrix, ROC curve and precision-recall curve using scikit-plot. The best parameter set gives test accuracy of 0.99757.  

*mnist-visualization.ipynb*

* In this notebook, I first visualize the training performance of the convnet by looking into the model accuracy and loss function as epoch increases. Next, I dive into deep learning visualization by extracting the weights and activations in the two hidden convolution layers.

[A Walkthrough of Convolutional Neural Network — Hyperparameter Tuning](https://medium.com/towards-data-science/a-walkthrough-of-convolutional-neural-network-7f474f91d7bd) 

* My blog post discussing convnet, how to tune hyperparamter and visualize deep neural net.

 
## Improvement on Accuracy

* The following combination of parameters gives the best result on test accuracy of 0.99757.
 
 | Hyperparameter                 | Value                                                | 
 | ------------------------------ |-----------------------------------------------------:|
 | no. of neurons                 | 32 (1st conv), 64 (2nd conv), 128 (fully connecetd)  | 
 | convolutional filter size      | 5x5                                                  |
 | batch size                     | 64                                                   |
 | no. of epochs                  | 20                                                   |
 | weight initialization          | uniform                                              |
 | activation function            | ReLu                                                 |
 | optimizer                      | Adam                                                 |
 | dropout                        | 0.25 (fully-connected), 0.5 (output layer)           |

 
## References

* [Deep Learning by Ian Goodfellow, Yoshua Bengio and Aaron Courville](http://www.deeplearningbook.org/)
* [Practical recommendations for gradient-based training of deep architectures by Yoshua Bengio](https://arxiv.org/abs/1206.5533)
* [Random Search for Hyper-Parameter Optimization](http://www.jmlr.org/papers/volume13/bergstra12a/bergstra12a.pdf)
* [Convolutional Neural Networks: Architectures, Convolution / Pooling Layers](http://cs231n.github.io/convolutional-networks/)
* [Understanding and Visualizing Convolutional Neural Networks](http://cs231n.github.io/understanding-cnn/)
* [Understanding Neural Networks Through Deep Visualization](http://yosinski.com/deepvis)
* [Understanding Convolutions](http://colah.github.io/posts/2014-07-Understanding-Convolutions/)
* [How to Grid Search Hyperparameters for Deep Learning Models in Python With Keras](http://machinelearningmastery.com/grid-search-hyperparameters-deep-learning-models-python-keras/)
 
 
