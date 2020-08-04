# pca-lda-computervision-doubledomino
## Utilize a base MNIST ou LFW para entender como PCA e LDA podem ser utilizados como features para reconhecimento de caracteres manuscritos

## 1. Carregue a base LFW
#### from sklearn.datasets import fetch_openml
#### X, y = fetch_openml('mnist_784', version=1, return_X_y=True)

## 2. PCA
### Aplique PCA avaliando o número de componentes necessários
### Visualize as imagens associadas com os primeiros componentes
#### pca.components_[i].reshape()
### Exiba a variância cumulativa
### Compare as imagens de entrada com as imagens reconstruídas
#### pca.transform e pca.inverse_transform

## 3. LDA
### Aplique LDA nos dados originais
### Exiba a projeção dos dados nos Discriminantes Lineares
### Exiba a taxa de variância acumulada

## 4. Classificador
### Aplique um classificador de sua escolha nas features obtidas por LDA e PCA
### Compare os dois métodos e resultados

## Nota: Caso deseje trabalhar com reconhecimento de faces ao invés de reconhecimento de caracteres manuscritos, pode-se utilizar a base LFW
#### faces = [sklearn.datasets] fetch_lfw_people(min_faces_per_person=60)

pca-lda-computervision-doubledomino created by GitHub Classroom
