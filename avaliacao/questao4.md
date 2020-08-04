## 4. [2 pontos] Explique resumidamente:
    a. O que são Árvores de Decisão e como os dados são divididos em cada nó da árvore?

    b. Quais suas vantagens e desvantagens?

RESPOSTA
=======================

A)

A árvore de decisão particiona o espaço de busca de um determinado problema levando em consideração os valores dos atributos até chegar na decisão desejada, a decisão é tomada através do caminhamento do nó raiz até o nó folha. Os dados podem ser divididos usando os critérios de ganho de informação e taxa de ganho (Encontra a melhor divisão usando a informação que foi “ganha”) ou usando a impureza de Gini (escolhe o atributo que diminui a impureza, depois a base de dados vai ser subdividida baseado nos valores possíveis e o cálculo começa para cada sub-árvore).

B)

As árvores são considerados algoritmos gulosos, pois toma a melhor decisão para aquele ponto, no entanto não é necessariamente a melhor decisão. Outra desvantagem é que vai ter overfit, no caso tendo um erro na base de treinamento ela poderá ser igual a zero, já no caso da base de teste ela irá aumentar depois de um certo tempo. Como vantagens, ela é fácil de compreender, podem ser utilizadas com ou sem dados concretos.
