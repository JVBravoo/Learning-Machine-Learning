## 1. [2 pontos] Sobre o k-Means, explique com suas palavras:

    a. Qual a representação do modelo treinado?
    Em outras palavras: o que o algoritmo armazena após o treinamento?

    b. Como é definido o melhor valor de k?

    c. Considerando um modelo k-Means já treinado e um exemplo de teste, como este exemplo é associado a um dos k grupos?

RESPOSTA
=======================

A)

Após o treinamento o K-means armazena os centróides do algoritmo e agrupa os centróides mais próximos em grupos.

B)

É necessário calcular a maior distância entre os agrupamentos de um mesmo cluster, depois procurar pelo melhor K usando o método do cotovelo (elbow), continuar executando e incrementando clusters até o ganho de K não ser mais necessário

C)

Na letra B) foi explicado que ele calculará a menor distância entre os agrupamentos, nesse caso da letra C, ele vai procurar a menor distância entre os K grupos de um cluster para poder saber de qual grupo aquele centróide pertence.
