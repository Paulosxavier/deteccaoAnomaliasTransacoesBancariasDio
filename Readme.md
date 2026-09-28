Detecção de Anomalias em Transações Bancárias usando Python
Este projeto implementa técnicas de Machine Learning para identificar transações fraudulentas em dados bancários.
O notebook foi desenvolvido em Google Colab e utiliza bibliotecas como pandas, scikit-learn, xgboost, matplotlib e shap.
Estrutura do Notebook
Preparação dos Dados
Carregamento da base creditcard.csv (dataset público do TensorFlow).
Criação de variáveis derivadas (Amount_log, Amount_scaled).
Divisão em treino e teste com train_test_split.
Modelos Treinados
Regressão Logística com pipeline de normalização.
Random Forest com ajuste de parâmetros e métricas adicionais.
XGBoost com ajuste de hiperparâmetros via GridSearchCV.
Avaliação dos Modelos
classification_report (Precision, Recall, F1-score).
Curvas ROC e Precision-Recall.
Métrica Average Precision (AP) para dados desbalanceados.
Explicabilidade
Importância das variáveis.
Valores SHAP para justificar decisões do modelo.

Melhorias Implementadas
RandomForestClassifier

Ajustado para usar mais árvores (n_estimators=200) e profundidade dinâmica (max_depth=None).

Avaliação com ROC-AUC, Precision-Recall Curve e Average Precision (AP).

Uso de predict_proba para permitir ajuste de threshold.

XGBoost - Ajuste de Hiperparâmetros

Grid expandido com parâmetros adicionais:

max_depth, n_estimators, learning_rate, subsample, colsample_bytree.

Otimização com recall como métrica principal.

Validação cruzada (cv=3) para maior robustez.

Threshold Automático

Implementado cálculo do melhor threshold com base no F1-score.

Permite equilibrar Recall e Precision de forma dinâmica
