# Detecção de Diabetes com Machine Learning

## Objetivo
Este projeto tem como objetivo desenvolver e comparar modelos de aprendizado de máquina para prever a presença de diabetes a partir de dados clínicos e demográficos.

O foco principal é **maximizar o recall para a classe positiva** (diagnóstico de diabetes), garantindo que o maior número possível de casos seja identificado, sem perder a performance global do modelo.

---

## Dados Utilizados
- **Variáveis**:
  - `Nivel_HbA1c` — nível médio de glicose no sangue nos últimos 3 meses
  - `nivel_glicose_sangue` — glicose medida no momento
  - `Idade` — idade do paciente
  - `IMC` — índice de massa corporal
  - `Hipertensão`, `Doenca_cardiaca` — indicadores binários
  - `Gênero` — masculino/feminino
  - `Historico_fumante` — sim/não

---

##  Metodologia
1. **Pré-processamento**:
   - Tratamento de valores ausentes
   - Codificação de variáveis categóricas
   - Balanceamento da base usando `scale_pos_weight`

2. **Modelos testados**:
   - **XGBoost**
   - **Random Forest**
   - **Rede Neural (Keras/TensorFlow)**

3. **Métricas de avaliação**:
   - `Precision`, `Recall`, `F1-score`
   - `AUC ROC`
   - Matriz de confusão
   - Importância das variáveis (para modelos baseados em árvore)

---

## 📊 Resultados

### 🔹 XGBoost
Relatório de classificação - XGBoost
              precision    recall  f1-score   support

           0       0.99      0.90      0.94     17525
           1       0.48      0.92      0.63      1701

    accuracy                           0.90     19226
   macro avg       0.73      0.91      0.79     19226
weighted avg       0.95      0.90      0.92     19226

AUC ROC - XGBoost: 0.9778

### 🔹 Random Forest

Relatório de classificação - Random Forest
              precision    recall  f1-score   support

           0       0.99      0.90      0.94     17525
           1       0.46      0.90      0.61      1701

    accuracy                           0.90     19226
   macro avg       0.73      0.90      0.78     19226
weighted avg       0.94      0.90      0.91     19226

AUC ROC - Random Forest: 0.9726

---

## 📈 Comparação Geral
- Ambos os modelos tiveram **AUC ROC acima de 0.97**.
- O **XGBoost** apresentou **melhor recall** na classe positiva (identificação de casos de diabetes).
- A **Random Forest** teve performance próxima, mas com recall um pouco inferior.
