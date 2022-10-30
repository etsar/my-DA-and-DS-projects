# Customers' age recognition by photo
## Goal
The supermarket chain "Good Seed" wants to explore whether Data Science can help them adhere to alcohol laws by making sure they do not sell alcohol to people underage.
Their shops are equipped with cameras in the checkout area which are triggered when a person is buying alcohol.
Computer vision methods can be used to determine age of a person from a photo.
<br>The task then is to build and evaluate a model for verifying approximate person's age by photo.
## Data
We have a set of photos of people with their age:
- `file_name` - name of the image with a person on it,
- `real_age` - age of the person.
## Libraries used
Keras, Matplotlib, NumPy, pandas, Seaborn, TensorFlow

## Conclusion
Before training the model, we analyzed the set of photos of people with their age, and performed unification of the image size. 
Beyond that, we performed a slight augmentation in the form of a horizontal reflection, that allowed us to increase the sample by 2 times. 
Moreover, the images obtained in this way are indistinguishable from the real ones. 
<br>Since the age verification is a regression task, we decided to use MAE as a quality metric, and MSE as a loss function, since, as a rule, such neural networks train faster than with a MAE loss function. 
We decided to use the network architecture based on ResNet with the ReLU activation function so that there are no negative age values.
<br>Then we built and trained a convolutional neural network on the dataset with photographs of people, and achieved the required MAE value on the test sample (according to the task, the MAE on the test sample should be no more than 8).
<br>Based on the goals of implementation of a computer vision system for processing customer photos and the resulting quality of the neural network, 
we can make the following conclusions:
- with the quality achieved, it can be difficult to control the conscientiousness of cashiers when selling alcohol. See ideas of quality improvement below;
- it is quite possible to analyze purchases and offer products of interest to buyers of a specific age group, given the possible error of 6.4 years, it should not be critical.

**Ideas of model quality improvement:**
1. The quality of the input data: re-evaluate the age from the photo.
2. Error analysis: for example, the model makes a lot of mistakes in the segment of the elderly, but it works almost perfectly with young people. Then understand what ages it would be good to add to the sample of photos for additional training.
3. In addition, study the distribution of the target. It is possible that the sample was not randomly drawn (small bimodality is visible), see which age groups are underrepresented in order to add them to the sample later.
