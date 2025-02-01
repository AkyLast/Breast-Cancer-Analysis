# Análise de Câncer de Mama com K-Nearest Neighbors (KNN)

## Sobre o Projeto

Este projeto tem como objetivo realizar a análise de dados relacionados ao câncer de mama, utilizando técnicas de aprendizado de máquina para classificar os dados em benignos ou malignos. O algoritmo escolhido foi o K-Nearest Neighbors (KNN), que é conhecido por sua simplicidade e eficácia em problemas de classificação.

## O Dataset

Os dados utilizados neste projeto foram extraídos de exames relacionados ao câncer de mama. O conjunto de dados é composto por diversas características que descrevem propriedades físicas e químicas de células tumorais, como:

- Raio médio
- Textura média
- Suavidade média
- Simetria média
- Dimensão fractal média

O dataset pois possui uma distribuição balanceada entre as classes (benigno e maligno) e fornece informações claras sobre as características mais relevantes para o diagnóstico.

## Etapas do Projeto

### 1. Exploração de Dados

Os dados foram analisados para identificar correlações entre as características e a classificação das células. Foi utilizada uma matriz de correlação para visualizar as relações mais significativas e remover atributos redundantes ou irrelevantes.

### 2. Divisão dos Dados

Os dados foram divididos em conjuntos de treinamento e teste utilizando a função `train_test_split`. Uma parte dos dados foi reservada para validação, garantindo a avaliação justa do modelo.

### 3. Normalização e Escalonamento

Para melhorar a performance do algoritmo KNN, as características foram normalizadas utilizando `StandardScaler`, garantindo que todas as variáveis tivessem a mesma escala e influências iguais no cálculo da distância.

### 4. Treinamento do Modelo

O modelo KNN foi treinado com diferentes valores de vizinhos (`k`) para identificar o parâmetro ótimo que maximiza a acurácia do modelo.

### 5. Avaliação

Foram calculadas métricas como:

- Acurácia
- Relatório de classificação (precisão, recall e F1-score)

### 6. Visualização de Resultados

Gráficos foram gerados para ilustrar a performance do modelo com diferentes valores de `k` e a influência do escalonamento e da remoção de atributos menos correlacionados.

## Conclusão

Este projeto demonstra como o uso de técnicas de pré-processamento, como normalização e seleção de atributos, pode melhorar significativamente a performance de algoritmos simples como o KNN. Além disso, destaca a importância de avaliar diferentes configurações para encontrar o modelo mais eficiente para os dados analisados.

## Requisitos

- Python 3.9+
- Bibliotecas:
  - pandas
  - matplotlib
  - scikit-learn

## Como Executar

1. Certifique-se de que todas as dependências estão instaladas.
2. Execute o código em um ambiente como Jupyter Notebook ou diretamente em Python.
3. Analise os resultados gerados e visualize os gráficos para interpretação dos dados.

## Conclusão

Este projeto demonstra como técnicas de aprendizado de máquina podem ser aplicadas em dados médicos para apoiar diagnósticos e decisões clínicas. A análise cuidadosa dos dados e o uso de métodos estatísticos robustos são essenciais para alcançar resultados confiáveis. O mesmo foi desenvolvido com foco em aplicações práticas de aprendizado de máquina na área de saúde.
