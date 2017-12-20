# fashion-mnist

I created this algorithm and trained it to recognize clothing from images provided by Zalando (a fashion company).
It classifies clothing to ten categories, ranging from t-shirts, trousers, pullovers, dresses, coats,sandals, shirts,
sneakers, bags, and ankle boots.

I used tensorflow libraries to aid in calculating the cost functions, softmax, and forward propagation.

![network structure](https://github.com/KingArthurZ3/fashion-mnist/blob/master/resources/network_structure.png "network_structure")

My neural network (as shown above)has two hidden layers with 128 hidden units in each. Each of these hidden layers
compute a linear function, which is then passed into a ReLU activation function. Finally, I use a softmax to process
output from my network and create 10 outputs (1 for each output class).

![forward propagation](https://github.com/KingArthurZ3/fashion-mnist/blob/master/resources/forward_propagation.png "forward_propagation")

For each of these hidden layers I used forward propagation, a technique that helps make a prediction based
on an input form a given image. Along with this, I also used backpropagation, with Adam regression, in order to
adjust the weights and biases based on the cost of the previous computation.

![cost-function](https://github.com/KingArthurZ3/fashion-mnist/blob/master/resources/costs.png "cost_function")

Finally, as shown by my cost function, my model correctly classifies these clothing types with approximately an
89.35% accuracy, not state-of-the-art, but definitely passable for most commercial purposes.

