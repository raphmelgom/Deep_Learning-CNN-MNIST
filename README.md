# Deep_Learning-CNN-MNIST

Neste código, primeiro carregamos o conjunto de dados MNIST usando a função load_data() do Keras. Em seguida, normalizamos os dados de entrada dividindo cada pixel por 255.0, para que eles fiquem na faixa entre 0 e 1.

Em seguida, definimos a arquitetura do modelo. Começamos com uma camada de entrada para receber as imagens em escala de cinza de 28x28 pixels. Em seguida, remodelamos as imagens para terem a forma (28, 28, 1) e aplicamos uma camada de convolução com 32 filtros e tamanho de kernel 3x3, seguida por uma camada de pooling máxima 2x2 para reduzir a dimensionalidade das características. Em seguida, achatamos as características em um vetor e passamos por duas camadas densas (fully-connected), com funções de ativação ReLU, antes de sair na camada de saída com uma função de ativação Softmax para obter as previsões de classe.

Em seguida, compilamos o modelo com o otimizador "adam" e a função de perda "sparse_categorical_crossentropy", que é adequada para problemas de classificação com várias classes. Também definimos a métrica de avaliação para a precisão (accuracy).

Em seguida, treinamos o modelo por 10 épocas, com uma divisão de validação de 20% para monitorar a precisão e a perda em um conjunto de dados separado. Finalmente, avaliamos o modelo no conjunto de testes e imprimimos a perda e a precisão obtidas. Este modelo deve alcançar uma precisão de teste superior a 98%.
