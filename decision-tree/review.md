1,5 de 2

train_test_split(df1, y, test_size=0.30, random_state=2)
- Divisão inicial para treino e teste nas duas práticas deve considerar shufle = false visto que se trata de suma série temporal.

Comparação entre RandomForest e Árvore não pode ser feita utilizando uma RandomForest com uma árvore apenas, visto que RandomForest utiliza amostragem das features e dos exemplos.
Tanto que o resultado da Árvore deu bem diferente do resultado da RandomForest com uma árvore apenas.
