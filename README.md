# Logistic Regression

## Uma Rede Neural como regressão logística

### Binary Classification

A __*Logistic Regression*__ é um algoritmo de classificação binária, imagina, por exemplo, que temos uma imagem, e nesta imagem está presente a figura de um gato, e nosso ituito como desenvolvedores de *machine learning* é realizar o aprendizado do nosso computador para que ele reconheça se a imagem mostrada é ou não de um gato. Dessa forma, caso afirmativo, o nosso resultado pode ser dado como valor 1, de `True`; assim como o valor 0, de `False`.

Vamos tomar como exemplo uma variável Y como saída, que receberá esses valores confirmando se existe ou não um gato na imagem. Para isso, devemos ter em mente que como toda imagem, o computador a armazenará como uma matriz de três camadas correspondentes às cores vermelho, verde e azul, ou mais popularmente conhecido como __RGB__ (*Red, Green and Blue*). Além disso, cada imagem tem uma tamanho, dependendo da quantidade de píxeis que nossa câmera consegue capturar, e por fim, cada um dos valores de nossa matriz representará a intensidade de determinada cor em sua respectiva camada para aquele píxel, compondo, assim, a imagem que está diante de nossos olhos.

Sendo assim, a ideia principal é conseguirmos criar um vetor com as características da nossa imagem, chamado de *feature Vector*, e esse vetor será composto dos valores de cada píxel e o utilizaremos como entrada para nossa *Logistic Regression*.  

Na primeira parte do meu código é possivel visualizar a etapa do processamento das imagens, que através de um banco de dados, de imagens diferentes uma das outras, e separadas manualmente em pastas específicas, (de acordo com a precisão do usuário em diferenciar imagens de gatos ou não, um fator que pode ser referenciado em análises mais precisas de Visão computacional denominado de *Bayes Human Error*), elas são padronizadas para um tamanho determinado de acordo com a necessidade, e convertidas para escala de cinza, fator que não iria comprometer a nossa análise, pois se trata de uma classificação binária.

O resultado dessa etapa é a criação dos nossos dados de treinamento, ou seja, o processamento das imagens de gatos e cachorros. Para o primeiro denomina-se um valor 0, enquanto que para os cachorros denomina-se um valor 1. Logo após isso, é necessário que se misture todos os valores de píxel das nossas imagens com suas demarcações para enfim criarmos as nossas matrizes de entrada e de saída, onde o conjunto dos valores de píxeis de uma imagem de gato, por exemplo, será uma entrada associada ao valor 0 na saída, e assim por diante.

Na *Logistic Regression* dado um vetor de característica x como entrada, queremos uma saída que prevê a imagem que está sendo mostrada, ou seja, o nosso objetivo é que ao testarmos uma imagem de gato, após o treino, o computador saiba reconhecer uma imagem de gato e indique como resultado o valor 0 na saída y.

Como o respectivo trabalho apresentado aqui, é baseado em uma classificação binária, os valores possíveis para a saída serão 1 ou 0, o que nos faz buscar uma função cuja saída varie entre 0 e 1, o que seria perfeito para nosso problema, e nesse caso a Função Sigmoide é a melhor escolha.

Como nossa função trabalhará com valores entre 0 e 1, precisamos executar uma normalização dos nossos dados de entrada, pois os valores de píxeis podem variar de 0 até 255. 

É importante salientar que esse projeto se trata de um aprendizado na área de *Machine Learning*, mesmo tendo o conhecimento de Frameworks que realizam esse tipo de processo muito mais rapidamente e com maior facilidade, a intenção desse trabalho é proporcionar um conhecimento mais aprofundado sobre o funcionamento do aprendizado de máquina. Certo disso, observa-se que foi realizado uma função responsável pelo cálculo da sigmoide, seguido das definições dos nossos parâmetros W e b que serão base para nossa regressão logística encontrar os padrões correstos nas diferentes imagens que faça com que ela atinja os resultdos corretos na saída.



