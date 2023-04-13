# ChildrenHeightPred

I have used a deep learning approach to solve the problem. Specifically, used a feedforward neural network with four layers - one input layer with 9 nodes, two
hidden layers with 32 and 64 nodes respectively, and one output layer with a single node.

The Rectified Linear Unit (ReLU) activation function is used for the hidden layers, and no activation function is used for the output layer since the problem is
a regression problem. The model is trained using the mean squared error (MSE) loss function and optimized using the Adam optimizer with a learning rate of 0.01
and weight decay of 0.001. A dropout layer with a dropout rate of 0.5 is also used for regularization to prevent overfitting.

The model is trained for 500 epochs, with a batch size of 32. During training, the model parameters are updated using backpropagation and the optimizer. At the
end of each epoch, the training loss is computed and printed. Finally, the trained model is used to make predictions on the training data, and the predicted 
heights are printed for each child in the dataset. 

From the given dataset, I identified that there were multiple input features available, but after analyzing them, I found that only 9 coordinates were 
significant for predicting the height of the child. Out of these 9 coordinates, I specifically chose the y-coordinates as they have a more significant impact on
determining the height of the child, whereas the x-coordinates do not play a major role in this prediction task.

In summary, I have used a feedforward neural network with four layers, ReLU activation function, dropout regularization, and the Adam optimizer to solve the
problem of predicting the height of children from depthmap images and corresponding pose key points.
