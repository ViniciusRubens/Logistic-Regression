# Logistic Regression

## Binary Classification

The __*Logistic Regression*__ is a binary classification algorithm, imagine, for example, that we have an image, and in this image is present the figure of a cat, and our intention as developers of *machine learning* is to perform the learning of our computer to recognize the figure of the cat. This way, if yes or no, our result can be given as value 1 or 0.

<p align="center">
    ![Binary Classification with cats and dogs](https://github.com/ViniciusRubens/Logistic-Regression/blob/main/Images/Fig1.png)
</p>

Let's take as an example a variable Y as output, this variable will receive these values confirming whether or not there is a cat in the image. For this we should keep in mind that the computer will store an image as an matrix of three layers corresponding to the colors red, green and blue, or more popularly known as __RGB__. In addition, each image has a size, depending on how many pixels our camera can capture, and finally, each of the values of our matrix will represent the intensity of a color, composing the image we see.

So, the main idea is to create a vector with the characteristics of our image, called Vector feature, and this vector will be composed of the values of each pixel and we will use it as input for our Logistic Regression. 

In the first part of my code you can see the stage of image processing. Through a database of images, they are standardized to a certain size according to the need of the problem, and converted to grayscale, a factor that would not compromise our analysis, because it is a binary classification, to be remodeled soon after, where each column will correspond to the pixels of each image.

O resultado dessa etapa é a criação dos nossos dados de treinamento, ou seja, o processamento das imagens de gatos e cachorros. Para o primeiro denomina-se um valor 0, enquanto que para os cachorros denomina-se um valor 1. Logo após isso, é necessário que se misture todos os valores de píxel das nossas imagens com suas demarcações para enfim criarmos as nossas matrizes de entrada e de saída, onde o conjunto dos valores de píxeis de uma imagem de gato, por exemplo, será uma entrada associada ao valor 0 na saída, e assim por diante.

Na *Logistic Regression* dado um vetor de característica x como entrada, queremos uma saída que prevê a imagem que está sendo mostrada, ou seja, o nosso objetivo é que ao testarmos uma imagem de gato, após o treino, o computador saiba reconhecer uma imagem de gato e indique como resultado o valor 0 na saída y.

Como o respectivo trabalho apresentado aqui, é baseado em uma classificação binária, os valores possíveis para a saída serão 1 ou 0, o que nos faz buscar uma função cuja saída varie entre 0 e 1, o que seria perfeito para nosso problema, e nesse caso a Função Sigmoide é a melhor escolha.

Como nossa função trabalhará com valores entre 0 e 1, precisamos executar uma normalização dos nossos dados de entrada, pois os valores de píxeis podem variar de 0 até 255. 

É importante salientar que esse projeto se trata de um aprendizado na área de *Machine Learning*, mesmo tendo o conhecimento de Frameworks que realizam esse tipo de processo muito mais rapidamente e com maior facilidade, a intenção desse trabalho é proporcionar um conhecimento mais aprofundado sobre o funcionamento do aprendizado de máquina. Certo disso, observa-se que foi realizado uma função responsável pelo cálculo da sigmoide, seguido das definições dos nossos parâmetros W e b que serão base para nossa regressão logística encontrar os padrões correstos nas diferentes imagens que faça com que ela atinja os resultdos corretos na saída.



