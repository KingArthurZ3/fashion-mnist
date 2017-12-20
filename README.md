# fashion-mnist

I created this algorithm and trained to recognize clothing from images provided by Zalando.There are
ten categories, ranging from t-shirts, trousers, pullovers, dresses, coats,sandals, shirts,
sneakers, bags, and ankle boots.

I used tensorflow libraries to aid in calculating the cost functions, softmax, and forward propagation.

[[fashion-mnist/resources/network_structure.png]]

My neural network (as shown above)has two hidden layers with 128 hidden units in each. Each of these hidden layers
compute a linear function, which is then passed into a ReLU activation function. Finally, I use a softmax to process
output from my network and create 10 outputs (1 for each output class).

[[fashion-mnist/resources/forward_propagation.png]]

For each of these hidden layers I used forward propagation, a technique that helps make a prediction based
on an input form a given image. Along with this, I also used backpropagation, with Adam regression, in order to
adjust the weights and biases based on the cost of the previous computation.

[[fashion-mnist/resources/costs.png]]

Finally, as shown by my cost function, my model correctly classifies these clothing types with approximately an
89.35% accuracy, not state-of-the-art, but definitely passable for most commercial purposes.