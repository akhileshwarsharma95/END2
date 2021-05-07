# Session 1 - Background & Very Basics- Assignment

# What is a neural network neuron?
A neuron in neural network, also called as preceptron, is an attempt to mathematically model actual biological neuron. In biological neurons, information travels through electrical signals and firing of neurons. The same is accomplished in preceptron by taking data (information) as input and the strength of signal is computed through multiplying certain weights with the input and passing the sum through an activation function. Activation function then decides how to pass that information further or wether to pass it or not by modulating the output.          
![image](https://user-images.githubusercontent.com/50059275/117373078-3af96280-aee8-11eb-8b9e-4c116777fe0f.png)


# What is the use of the learning rate?
Let's imagine ourselves standing at top of a hill and we want to climb down to the valley. As humans, we will be very easily be able to do it even without thinking much. But essentially,accompling it is a two-step process 1. Direction- In which direction to move and 
2. Distance- How much to move. When we initialize our parameters and want to find their estimates by optimizing a loss function, for example, the loss (or errors) are like us on top of the hill and we want them to come to the lowest point possible. So now, our errors too need a direction and magnitude to move. The direction to move is provided by the gradient of that loss function and the step size (also called learning rate) needs to be provided. It is usually a configureable hyperparameter. There is an impact of the choice of the learning rate on the training. Altough, there is not a mathematical way to determine value of learning rate, it 
is suggested to choose it optimally, not quite large or fast such that it misses the destination and not too small or slow that practically it is time consuming. Ofcourse, there are exceptions to it where people are using very high learning rates.
![image](https://user-images.githubusercontent.com/50059275/117377088-13a69380-aef0-11eb-962f-5f22e69fd51c.png)




# How are weights initialized?
Weights for a network are initialized randomly, generally from a normal distiribution. Weights can also be initialized from a constant values like 0s or 1s but it generally not considered as a good practice since, if all the wieghts are same, so will be their gradients and all weight updates would be similar preventing nuerons from learning. If weights are chosen to be too small or too large, we encounter problems of vanishing gradients or exploding gradients. That's why random initialization from a normal distribution is still a good method because, normal distbution has thin tails at extreme values, so unlikely to cause vanishing or exploding gradient problems. So, it is essential for efficient training the wieghts are initialized carefully.


# What is "loss" in a neural network?
In Supervised Learning paradigm, we provide neural networks with the input as well as the output. We are expecting neural network to learn this mapping from input to output. While training the network when it is still learning, it obviously makes some mistakes. The output thrown is not the desired output.This deviation of output of network and desired output is known as loss. It is expected loss to go down with increasing epochs. It is used to evaluate learning process of neural network.Depending on the problem or task at hand, they are various loss functions to choose from for example, mean-sqaured error or cross-entropy. 

# What is the "chain rule" in gradient flow?
Loss function in neural network is optimized with respect to individual wieghts of the network. The chnage in output of loss function is tried to be evaluated with respect
to every weight in the network. Now, it is a complex network (multivariable), there could be several interactions between different weights and variables. One cannot just
take a simple derivative. In order to understand the change in output with respect to a given weight it is understood first through change in output with respect to the contibution of all the weights and effect on contribution by this particluar weight. 
∂Output/∂wi=(∂Contribution1/∂wi)×(∂Output∂Contribution1)   




*Disclaimer: I do not own any of the images in this page. All the credit goes to owners of these.* 
