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

<img width="457" height="218" alt="image" src="https://github.com/user-attachments/assets/129fdc94-191e-4eee-b182-acfc09f36ae2" />


### 🔹 Random Forest

<img width="457" height="218" alt="image" src="https://github.com/user-attachments/assets/50816b22-6d5f-4f3f-933c-fa9dfe8fc632" />

---

## 📈 Comparação Geral
- Ambos os modelos tiveram **AUC ROC acima de 0.97**.
- O **XGBoost** apresentou **melhor recall** na classe positiva (identificação de casos de diabetes).
- A **Random Forest** teve performance próxima, mas com recall um pouco inferior.
