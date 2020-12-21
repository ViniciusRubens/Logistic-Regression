# Logistic Regression

## Binary Classification

The __*Logistic Regression*__ is a binary classification algorithm, imagine, for example, that we have an image, and in this image is present the figure of a cat, and our intention as developers of *machine learning* is to perform the learning of our computer to recognize the figure of the cat. This way, if yes or no, our result can be given as value 1 or 0.

![Binary Classification with cats and dogs](https://github.com/ViniciusRubens/Logistic-Regression/blob/main/Images/Fig1.png)

Let's take as an example a variable Y as output, this variable will receive these values confirming whether or not there is a cat in the image. For this we should keep in mind that the computer will store an image as an matrix of three layers corresponding to the colors red, green and blue, or more popularly known as __RGB__. In addition, each image has a size, depending on how many pixels our camera can capture, and finally, each of the values of our matrix will represent the intensity of a color, composing the image we see.

So, the main idea is to create a vector with the characteristics of our image, called Vector feature, and this vector will be composed of the values of each pixel and we will use it as input for our *Logistic Regression*. 

![Reshape Feature Vector](https://github.com/ViniciusRubens/Logistic-Regression/blob/main/Images/Fig2.png)

In the first part of my code you can see the stage of image processing. Through a database of images, they are standardized to a certain size according to the need of the problem, and converted to grayscale, a factor that would not compromise our analysis, because it is a binary classification, to be remodeled soon after, where each column will correspond to the pixels of each image.

The result of this step is the creation of our training data. After that, it is necessary to mix all the input and output values to finally create our matrices.

In *Logistic Regression* we want an output that forecasts the image being shown from our input x. Our goal is that when we test a cat image, after training, the computer knows how to recognize a cat image and indicate as a result the value 0 in the output y. This work is based on a binary classification and the possible values for the output are 1 or 0, which makes us look for a function whose output varies between 0 and 1. One solution to our problem is the use of the Sigmoid Function.

![Sigmoid Function](https://github.com/ViniciusRubens/Logistic-Regression/blob/main/Images/Fig3.png)

The sigmoid function will work with values between 0 and 1, it is convenient to perform a normalization of our input data, because the values of pixels can vary from 0 to 255. 

Note: It is important to point out that this project is a learning in the area of *Machine Learning*, even having the knowledge of Frameworks that perform this type of process much more quickly and easily, the intention of this work is to provide a deeper knowledge about the functioning of *Machine Learning*. 

The continuation of the project shows that a function was made for the calculation of sigmoid, followed by the initializations of our W and b parameters that will be the basis for our logistic regression to find the correct patterns in the different inputs you make to achieve accurate results in the output.

![W and b parameters](https://github.com/ViniciusRubens/Logistic-Regression/blob/main/Images/Fig4.png)

