# Says One Neuron To Another
## By Ronald Moore and Austin Adams
  
### *Purpose*
The purpose of this project is to understand the underlying mathematics of neural networks.

### *Data*
The datasets used for this project can be located in the 'Data' subfolder of this repository
#### Zoo Dataset
The zoo classification dataset looks at the features of different animals and their given animal classes (mammal, bird, reptile, fish, amphibian, bug and invertebrate)

Some interesting features include:
* hair
* feathers
* eggs
* milk
* fins
* legs
* tail
#### Mushroom Dataset
The mushroom classification dataset looks at different features of both poisonous (p) and edible (e) mushrooms

Some interesting features include:
* cap shape
* cap surface
* bruises
* odor
* ring number
* ring type
* gill color

### *Neural Network Implementation*
Both of the neural networks are multilayer perceptrons (MLPs). Each network consists of an input layer, a hidden layer, and an output layer.

#### Input Layers
The width of the input layer was chosen to match the number of features for each dataset. For the zoo dataset, the input layer was given a width of 16, since it has 16 features. The mushroom dataset has 22 features, so the input layer width is of size 22.
#### Hidden Layers
For both datsets, the hidden layer width was arbitrarily set to size 20.
#### Output Layers
Both datasets are looking to solve classification problems. Therefore, the width of the output layer was set to match the number of possible classes for a given observation. For the zoo dataset, the output layer width was set to size 7, since its network is attempting to correctly classify an animal to its given class (mammal, bird, reptile, fish, amphibian, bug, invertebrate). As for the mushroom dataset, the output layer width was set to size 1, since the network is trying to predict whether a given mushroom is edible (e) or poisonous (p).
#### Activation functions
For both networks, the rectified linear unit (ReLU) was chosen as the activation functions for the hidden layer. ReLUs perform fast calculations and are known to avoid the vanish gradient problem that occurs with logistic sigmoid activation functions.

The activation functions for the output layers differ since the neural networks are trying to solve different types of classification problems. For the zoo dataset, the softmax activation function was chosen for the output layer. This is because softmax functions output probablistic distributions for a given set of classes, which is useful for multiclass classification problems. For the mushroom dataset, the logistic sigmoid activation function was chosen for the output layer. This is because sigmoid functions output an integer between 0 and 1, which is useful for binary classification problems.
#### Training and Testing
Roughly 80% of the data was used to train the model, while the other 20% was used for testing. Both models were then trained for a length of 10000 epochs.
### *Discussion*
The neural network model for the zoo dataset had an accuracy of 80%. This model  finished training much faster than the model used for the mushroom dataset because the computations for the derivative of the ReLU activation function are much quicker than those for the derivative of the sigmoid activation function.

The neural network model for the mushroom dataset had an accuracy of about 69%. However, it also had a precision score of 69%, a true positive rate of 100%, and a true negavitve rate of 0%. This means that the network only predicted that a mushroom would be poisonous. Since 69% of the test data samples were poisonous mushrooms, the network achieved an accuracy of 69%. However, if the distribution of the test data was different, then the accuracy of the neural network would have significantly changed. Perhaps a more robust network could be made by adding another hidden layer or changing the width of the hidden layer.

### *References*
https://stackabuse.com/creating-a-neural-network-from-scratch-in-python/

https://towardsdatascience.com/how-to-build-your-own-neural-network-from-scratch-in-python-68998a08e4f6

https://beckernick.github.io/neural-network-scratch/

https://ml-cheatsheet.readthedocs.io/en/latest/backpropagation.html
