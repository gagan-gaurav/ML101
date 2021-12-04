---
description: All About Support Vector Machines.
---

# SVM

* Data is mapped to a new high-dimensional representation where the decision boundary is a hyperplane.&#x20;
* A Good Decision boundary maximizes the distance between the hyperplane and the closest data point from each class.&#x20;
* Kernel Function:- Maps two data points in your initial space to the distance between these points in your largest representation space. Some examples of kernel Function include Polynomial Kernel, RBF kernel, Sigmoid Kernel.
* The Vectors on the decision boundary are called the support vectors.

![](<.gitbook/assets/image (5).png>)

$$
Margin Size : 2/||w||
$$

![Cost Function for the SVM(along with Hinge Loss)](<.gitbook/assets/WhatsApp Image 2021-09-14 at 10.44.52.jpeg>)

![Gradients of the Above Cost Function](<.gitbook/assets/WhatsApp Image 2021-09-14 at 10.46.15.jpeg>)

![Gradients](<.gitbook/assets/WhatsApp Image 2021-09-14 at 10.46.34.jpeg>)

Head over to this [Link](https://github.com/RheagalFire/Scratch-Implementations/blob/master/Support%20Vector%20Machines%20\(SVM\).ipynb) for Scratch Implementation of SVM.

### Hard Margin SVM

Minimize ||W|| and yi(wxi-b)>=1 for i\<n

### Soft Margin SVM&#x20;

![](<.gitbook/assets/image (6).png>)

### Advantages

1. SVM is more effective in high-dimensional spaces.
2. SVM is relatively memory efficient.
3. SVM’s are very good when we have no idea about the data.
4. Works well with even unstructured and semi-structured data like text, Images, and trees.
5. The kernel trick is the real strength of SVM. With an appropriate kernel function, we can solve any complex problem.
6. SVM models have generalization in practice, the risk of over-fitting is less in SVM.

### Disadvantages

1. More Training Time is required for the larger dataset.
2. It is difficult to choose a good kernel function.
3. The SVM hyperparameters are Cost -C and gamma. It is not that easy to fine-tune these hyper-parameters. It is hard to visualize their impact.
