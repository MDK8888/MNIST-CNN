# MNIST-CNN
## Project Overview: 
This is my implementation of a Convolutional Neural Network(CNN), a Machine Learning Model which is used for image classification and forms the foundation for Modern Computer
Vision(CV). What sets CNNS apart from traditional Multilayer Perceptrons is their usage of Convolutional Filters. In inference, these filters contain different feature maps which
we use to scan over the image: interpreting our image as a grid of pixels, we take the element-wise product of our feature map with a region of our image, and store it in a 
product matrix. We then feed these product matrices element-wise into an Activation Function, and they are now ready for the next layer! We do this for all possible regions of our image and
all of our filters, with each distinct filter having its corresponding product matrix.

See the below gif for a visualization of the scanning/multiplication process, where the feature map is in dark blue, the image is light blue, and the product matrix is white:
![alt text](https://miro.medium.com/max/1400/1*Fw-ehcNBR9byHtho-Rxbtw.gif)

Once we have repeated this an arbitrary number of times, we reshape it into a single vector and feed it into a Multilayer Perceptron, calculate the loss function, and 
backpropagate it. 

## Implementation Details: 
**Final Accuracy**: 94.71%

**1st layer**: 6 5x5 Filters, ReLU Activation Function 

**2nd layer**: 12 6x5x5 Filters, ReLU Activation Function 

**3rd layer**: Fully Connected Layer, output of length of 136, ReLU Activation 

**4th layer**: Fully Connected Layer, output of length 10 for classification, Cross-Entropy Loss. 

