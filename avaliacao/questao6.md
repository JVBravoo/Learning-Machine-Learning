## 6. [2 pontos] Sobre Random Forests, explique:
    a. O que são Random Forests?

    b. Como este modelo é treinado de forma que não gere uma mesma árvore sempre?

    c. Considerando o trade-off Bias-Variance, qual problema este modelo diminui e como isto é alcançado?

RESPOSTA
=======================

A)

É um método de ensemble learning para classificação, regressão e utiliza árvores de decisão para weak learner, que treina cada árvore com um subconjunto da base de treino.

B)

Utilizando Bootstrap ele gera amostras diferentes dos dados de forma aleatória, dessa forma, garantindo que o modelo não irá gerar a mesma árvore sempre.

C)

Ele diminui o problema de overfitting e underfitting, usando bootstrap, pois faz com que ele treine cada modelo de forma independente.
