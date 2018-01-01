# fashion-mnist

I created this algorithm and trained it to recognize clothing from images provided by Zalando (a fashion company). I used a dataset 55,000 training examples and 10,000 test examples. It classifies clothing to ten categories, ranging from t-shirts, trousers, pullovers, dresses, coats,sandals, shirts, sneakers, bags, and ankle boots.

![network structure](https://github.com/KingArthurZ3/fashion-mnist/blob/master/resources/data_set_image.png "network_structure")

Each of the photos are in the form of a 1D Numpy array with 784 elements.

## Parts of my Neural Network

1. **Establish network parameters**
2. **Initialize placeholders**
3. **Initialize parameters**
4. **Forward propagation**
5. **Compute cost**
6. **Backpropagation**
7. **Combining everything**

![network structure](https://github.com/KingArthurZ3/fashion-mnist/blob/master/resources/network_structure.png "network_structure")

My neural network (as shown above)has two hidden layers with 128 hidden units in each. Each of these hidden layers
compute a linear function, which takes in the input image (a NumPy Array) and parameters from my dictionary (which contains weights and biases for each layer). Then, I pass the output into a ReLU activation function. Finally, I use a softmax function to process the output from my network and create 10 outputs (1 for each output class).

## Forward Propagation

![forward propagation](https://github.com/KingArthurZ3/fashion-mnist/blob/master/resources/forward_propagation.png "forward_propagation")

For each of these hidden layers I used forward propagation, a technique that helps make a prediction based
on an input form a given image.  

## Backpropagation

Along with this, I also used backpropagation, with Adam regression, in order to
adjust the weights and biases based on the cost of the previous computation.

## Combining Everything

I combined everything in my **model()** function, which create placeholders, initializes parameters, carries out forward prop and backpropagation, and graphs the cost decrease over time. I also print out hyperparameter values like:

1. **learning_rate** (learning rate optimization)
2. **num_epochs** (# of epochs of the optimization loop)
3. **minibatch_size** (size of each minibatch)

Each epoch, my network trains sequentially on minibatches, saves the parameters, and calculates the model’s accuracies on the training and test sets.

![cost-function](https://github.com/KingArthurZ3/fashion-mnist/blob/master/resources/costs.png "cost_function")

Finally, as shown by my cost function, my model correctly classifies these clothing types with approximately an
**89.35% accuracy**, not state-of-the-art, but definitely passable for my purposes.

Github repository for this project: https://github.com/KingArthurZ3/fashion-mnist
