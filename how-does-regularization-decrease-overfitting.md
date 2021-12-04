# How does Regularization decrease overfitting?

### L2 Regularization&#x20;

The primary reason overfitting happens is because the model learns even the tiniest details present in the data. So after learning all the possible patterns it can find, the model tends to perform extremely well on the training set but fails to produce good results on the dev and test sets. It falls apart when faced with previously unseen data.

One way to prevent overfitting is to reduce the complexity of the model. This is exactly what regularization does! If we set the regularization parameter (ƛ) to a large value, the decay in the weights during gradient descent update will be more. Hence, the weights of most of the hidden units will be close to zero.

Since the weights are negligible, the model will not learn much from these units.This will end up making the network simpler and thus reduce overfitting

### Dropout Regularization

The model will randomly remove 50% of the units from each layer and we finally end up with a much simpler network.

### Other Regularization Methods

Apart from L2 regularization and dropout, there are a few other techniques that can be used to reduce overfitting.

1. **Data Augmentation:** Suppose we are building an image classification model and are lacking the requisite data due to various reasons. In such cases, we can use data augmentation, i.e., applying some changes such as flipping the image, taking random crops of the image, randomly rotating images, etc. These can potentially help us get more training data and hence reduce overfitting.
2. **Early Stopping:** Stop before Accuracy Decay or Loss starts to rise.&#x20;
3.

\


