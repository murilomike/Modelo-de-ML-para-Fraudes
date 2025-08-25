# Modelo-de-ML-para-Fraudes

# 🔍 Prevendo Fraudes com Regressão Logística

Este projeto simula uma entrevista técnica para uma vaga de Cientista de Dados. O objetivo é construir um modelo de Machine Learning capaz de prever fraudes com base em variáveis explicativas. A abordagem principal utiliza **regressão logística** com técnicas de **balanceamento de classes** e **validação cruzada**.

---

## 📁 Estrutura do Projeto

- `Introdução`: Contextualização do problema e definição da variável alvo (`fraud`)
- `Pré-processamento`: Verificação de nulos, separação entre treino e teste, escalonamento
- `Balanceamento`: Aplicação de SMOTE para equilibrar as classes
- `Modelagem`: Regressão logística com validação cruzada
- `Avaliação`: Métricas como ROC AUC, precisão, recall e F1-score
- `Conclusão`: Interpretação dos resultados e próximos passos

---

## 📊 Dataset

- Fonte: `fraud_dataset.csv`
- Variável alvo: `fraud` (0 = não fraude, 1 = fraude)
- Total de registros: 1.000.000
- Após divisão:
  - Treino: 800.000 registros
  - Teste: 200.000 registros

---

## ⚙️ Técnicas Utilizadas

- **Holdout**: Separação entre treino e teste com `train_test_split`
- **StandardScaler**: Escalonamento dos dados para evitar distorções
- **SMOTE**: Oversampling da classe minoritária para balanceamento
- **StratifiedKFold**: Validação cruzada estratificada
- **Regressão Logística**: Modelo base para classificação binária
- **Métricas**: `classification_report`, `roc_auc_score`, `cross_val_score`

---

## 📈 Resultados

### Validação Cruzada (ROC AUC):
- Média: `0.9792`

### Teste Final:
- ROC AUC: `0.9430`
- Acurácia: `93%`

### Relatório de Classificação:

| Classe | Precision | Recall | F1-score | Suporte |
|--------|-----------|--------|----------|---------|
| 0 (não fraude) | 1.00 | 0.93 | 0.96 | 182.519 |
| 1 (fraude)     | 0.58 | 0.95 | 0.72 | 17.481  |

---

## 📌 Conclusão

O modelo se mostrou eficaz em detectar fraudes, com **alta taxa de recall para a classe 1**, o que é desejável em cenários onde é melhor errar por excesso (falsos positivos) do que deixar fraudes passarem despercebidas. A precisão da classe 1 ainda pode ser otimizada com ajustes de threshold ou modelos mais robustos.

---

## 🚀 Próximos Passos

- Testar modelos como Random Forest, XGBoost e LightGBM
- Ajustar o threshold de decisão para melhorar a precisão da classe 1
- Aplicar técnicas de feature engineering para enriquecer os dados
- Avaliar com métricas como Precision-Recall Curve e matriz de confusão visual

---

## 🧠 Autor

**Murilo Mike**  
Projeto desenvolvido como parte de estudos em Ciência de Dados e entrevistas técnicas.

