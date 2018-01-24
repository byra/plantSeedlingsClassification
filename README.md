# Using Neural Networks to do classification of plant seedlings

Agriculture is the art and science of cultivating the soil, growing crops and raising livestock. Agriculture is the backbone of every country’s economy and development. In the current modern society, it is our duty and concern to give importance to agriculture and its improvement as the nature resources are diminishing day to day. Researchers in modern agriculture are using machine learning algorithms at greater scale and helping make more accurate, real-time predictions. Modern agriculture has the potential to discover even more ways to achieve higher productions, conserve water, use nutrients and energy more efficiently, and adapt to climate change.

One major problem faced in agriculture production is the effect of weeds on the plant growth. According to the WEED SCIENCE SOCIETY OF AMERICA, on an annual basis, potential loss in value for corn is $27 billion and for soybean is $16 billion based on data from 2007 to 2013. Overall, average % yield loss with no weed control in corn is 52% and soybean is 49.5%. The impact of weeds on the agriculture production is very high in terms of crop yield and quality, which must be controlled at the seedling stage.

Our motivation and interest in challenging this task is the thought, where we can draw a line between plant seedlings and weed seedlings. This approach can make any machinery to easily detect the weed and remove it effectively without disturbing the plants growth leading to increased productivity.

# Problem Statement
Humans while cultivating can easily recognize plant vs weed but it is attached with lot of human work power, so making machines to learn these techniques we can save time and cost. The ability to differentiate weed from plant so effectively can mean better crop yields and better stewardship of the environment. The problem is to create a classifier which can determine a plant species from a photo.

# Datasets and Inputs

Dataset is obtained from:https://www.kaggle.com/c/plant-seedlings-classification

The dataset comprises 12 plant species:
1)Black-grass                                 	7) Loose Silky-bent
2)Charlock			8) Maize
3)Cleavers			9) Scentless Mayweed
4)Common Chickweed		10) Shepherds Purse
5)Common wheat		11) Small-flowered Cranesbill
6)Fat Hen			12) Sugar beet
File descriptions
train.csv - the training set, with plant species organized by folder
test.csv - the test set, you need to predict the species of each image.

# Solution Statement
As we know one of the major applications of Convolutional Neural Networks is image classification. Using CNN approach, we would build a classifier where we will first consider that all images are in fixed size by doing resizing. As the computer interprets every image as 3dimensional array, my design of CNN architecture would be to taking the image array and making it much deeper when it is tall or wide with the use of convolutional layers to make layers deeper and max pooling layers to decrease the spatial dimensions. As there are 12 species my output layer would have 12 nodes. We will use keras to build using relu activation function.  	  

# Benchmark Model
we will develop a CNN classifier which will give high F1 score and try to reduce the type 2 error because if the model predicts a plant as weed machine will remove the plant which is loss.we will build a confusion matrix which will give the differences between the predicted class and true class among the 12 species .

	        Weed	Not weed
Weed	    Correct	Type1
Not weed  Type2	Correct

# Evaluation Metrices
As this project data is considered from the Kaggle, F1 score can be considered as an evaluation metric. we will consider F1 score on my testing dataset. Higher the F1 score better the model

# Project Design
We would load all the 12 plant species images and see how images will be loaded, resize all images into fixed size if they are in different sizes. Next, we will add convolutional and max pooling layers to build CNN with 12 output nodes and check how accurately the model is classifying the plant images using confusion matrix.
Tools: Python,Jupyter notebook,pandas,numpy,keras,tensorflow,seaborn and will add if any libraries that I will use.


References
[1] Kaggle 
https://www.kaggle.com/c/plant-seedlings-classification
[2] weed science society of America
http://wssa.net/wssa/weed/croploss/
[3] Agricultural Crop Yield Prediction Using Artificial Neural Network Approach
http://cweteseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.429.1195&rep=rep1&type=pdf
 
 




### Building a Image Classifier capable of determining a plant's species among 12 different species from a photo.
####points discussing
###1)Approach
####2)Supervised or unsupervised classification
####3)Are there any algorithms for image classification other than neural nerworks
####4)Tensorflow basics
###5)weekend work to do
