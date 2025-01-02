# Projeto de Classificação com K-Nearest Neighbors (KNN)

Este projeto utiliza o algoritmo de K-Nearest Neighbors (KNN) para classificação de dados. O modelo é treinado com um conjunto de dados escalado e avaliado em um conjunto de teste para medir a precisão e a qualidade da classificação.

## Estrutura do Projeto

- **model**: O modelo de classificação KNeighborsClassifier.
- **X_train**: Conjunto de dados de treinamento.
- **y_train**: Rótulos do conjunto de dados de treinamento.
- **X_train_scaled**: Conjunto de dados de treinamento escalonado.
- **X_trainNotLig**: Conjunto de dados de treino sem dados com baixo nível de correlação.
- **y_train_notLig**: Rótulos do conjunto de dados de treinamento.
- **accuracy_score**: Função utilizada para calcular a precisão do modelo com base nas previsões realizadas.

## Como Executar

1. Certifique-se de ter as bibliotecas necessárias instaladas. Você pode instalar as dependências com o seguinte comando:
    ```bash
    pip install -r requirements.txt
    ```

2. Execute o script para treinar o modelo e avaliar a precisão:
    ```python
    from sklearn.neighbors import KNeighborsClassifier
    from sklearn.metrics import accuracy_score, classification_report

    # Inicializa o modelo KNN com 6 vizinhos
    model = KNeighborsClassifier(n_neighbors = 6)
    
    # Treinamento do modelo
    model.fit(X_trainNotLig_scaled, y_train_notLig)
    
    # Previsões no conjunto de teste
    y_pred = model.predict(X_testNotLig_scaled)
    
    # Calculando a precisão
    accuracy = accuracy_score(y_test_notLig, y_pred) * 100
    print(f"Acc: {accuracy:.2f}%")
    
    # Relatório de classificação
    print("\n", classification_report(y_test_notLig, y_pred))
    ```

## Resultados

Obs.: A escolha do "KNeighborsClassifier(n_neighbors = 6)" do "n_neighbors" igual a 6 foi devido a análise gráfico que mostrava que utilizando entre 1 e 9 o nível de acurácia era o melhor dentre os treinamentos. Usando o conjunto de dados que era escalonado e sem correlação de baixo nível.

Após a execução do código, o modelo imprime a precisão do modelo e um relatório de classificação com as métricas de desempenho como precisão, recall e F1-score.

Exemplo de saída:

```
Acc: 100.00%

               precision    recall  f1-score   support

           0       1.00      1.00      1.00        43
           1       1.00      1.00      1.00        71

    accuracy                           1.00       114
   macro avg       1.00      1.00      1.00       114
weighted avg       1.00      1.00      1.00       114
```


## Dependências

Este projeto requer as seguintes bibliotecas Python:

- `scikit-learn`
- `numpy`
- `pandas`
