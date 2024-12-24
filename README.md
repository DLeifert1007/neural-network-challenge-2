# neural-network-challenge-2

I have been tasked with creating a neural network that HR can use to predict whether employees are likely to leave the company. Additionally, HR believes that some employees may be better suited to other departments, so I will also predict the department that best fits each employee. These two columns should be predicted using a branched neural network.


Part 1: Preprocessing

Part 2: Create, Compile, and Train the Model

Part 3: Summary

# Summary

In the provided space below, briefly answer the following questions.

**1. Is accuracy the best metric to use on this data? Why or why not?**

Accuracy is a very common metric to use on data for multiple reasons. For one, it is a simple metric to communicate the model's performance. However, whether or not accuracy is the best metric for the data in this assignment is debatable. For the y_df column attrition, we are working with binary data. Binary data is great with accuracy metircs as the classification task is straight forward. We do not however know how well balanced this binary data is which is why I note this as debatable. I can however, see how well the accuracy score performed with a score of 0.807, and this leads me to believe that the accuracy metric for the attrition column is a great choice. Now for the department predictions we are less confident in this choice as the score was only a 0.5 and the data was not binary. Without knowing exactly how balanced or unbalanced the y_df department column is, we can only glean that the low score in the accuracy metric is due to a possible inbalance in the data and therefor indicating the model had low accuracy.

**2. What activation functions did you choose for your output layers, and why?**

The output layers in both of the attrition output as well as the department output were working off of a hidden layer activation relu function and the output layers for both were sigmoid. Activation relu, or rectified linear unit, handles any negative input by putting out a zero in its place and is typically used in the hidden layers of neural networks. Now the activation function that was chosen for the output layers was the sigmoid funciton. For binary classification tasks this is ideal, and for attrition this was the best choice. Sigmoid outputs numbers into either a zero or a one, this is ideal also for binary as our attrition data is. In the deparment branch sigmoid has a smooth gradient which works well with training data because they aid in stable and efficient models. 

**3. Can you name a few ways that this model might be improved?**

 A few ways that this model might be improved is to change the output layer from sigmoid function to softmax in order to better work with the non-binary data of the department column. Softmax can handle multiple classes as well as better probability distribution across all classes. Another way that this model might be improved is by increasing model complexity. So for example, we could add hidden layers and move up from 32 to 64. We could also try different activation functions. Another option to improve our model would be in preprocessing, we could work to make sure our data is balanced and make improvements on the unbalance such as oversampling or undersampling. I can not elaborate on the best methods in which to handle the inbalance because I have not analyzed the balance or unbalance of the data to decide the best plan. 
