# EIACD Assignment 2 (2024/2025)

**Autores:** Afonso Santos (202406585), David Pereira (202405163), Xavier Teixeira (202406657)

## Objetivo
O objetivo deste trabalho é desenvolver um sistema de machine learning capaz de **prever se um estudante será aprovado ou reprovado no exame final**. A antecipação destes resultados permite identificar alunos em risco e possibilita intervenções pedagógicas direcionadas.

## Dados
- **Fonte:** UCI Student Performance Dataset  https://archive.ics.uci.edu/dataset/320/student+performance
- **Ficheiro:** `student-data.csv`
- **Registos:** 395 estudantes
- **Atributos:** 31 variáveis (demográficas, socioeconómicas, comportamentais e de desempenho)
- **Variável alvo:** `passed` (binário: 'yes' para aprovado, 'no' para reprovado)

## Pipeline do Projeto
O notebook `eiacd_assignment2_adhx.ipynb` segue as seguintes etapas:
1. **Exploração e análise dos dados**
2. **Pré-processamento** (limpeza, encoding, normalização)
3. **Engenharia de features** (criação de novas variáveis)
4. **Balanceamento de classes** (SMOTE, Random Over/Under Sampling)
5. **Modelação** (treino e avaliação de modelos)
6. **Avaliação e interpretação dos resultados**

## Modelos de Machine Learning Utilizados
- Regressão Logística
- Árvore de Decisão
- Random Forest
- Support Vector Machine (SVM)

## Métricas de Avaliação
- **Accuracy**
- **Precision**
- **Recall** (com foco na classe minoritária: reprovados)
- **F1-Score**
- **ROC AUC**

## Principais Resultados
- O **cenário ótimo** (engenharia de features + balanceamento de classes) produziu os melhores resultados para identificar alunos reprovados.
- O **SVM** destacou-se, atingindo um **Recall_0 de 0.74** (identificando 74% dos alunos reprovados).
- O **Random Under Sampling** foi a técnica de balanceamento mais eficaz neste contexto.

## Como Executar
1. Certifique-se de ter o Python 3.13+ instalado.
2. Instale as dependências (veja abaixo).
3. Abra o notebook `eiacd_assignment2_adhx.ipynb` no Jupyter Notebook ou Google Colab.
4. Execute as células sequencialmente.

### Dependências
- pandas == 2.2.3
- numpy == 2.1.3
- scikit-learn == 1.6.1
- matplotlib == 3.10.0
- seaborn == 0.13.2
- imbalanced-learn == 0.13.0
- scipy == 1.15.2

Instale com:
```bash
pip install pandas==2.2.3 numpy==2.1.3 scikit-learn==1.6.1 matplotlib==3.10.0 seaborn==0.13.2 imbalanced-learn==0.13.0 scipy==1.15.2
```

## Estrutura dos Ficheiros
- `eiacd_assignment2_adhx.ipynb`: Notebook principal com todo o pipeline e análise.
- `student-data.csv`: Ficheiro de dados utilizado.

## Observações Finais
- O foco do trabalho foi maximizar a identificação de alunos em risco de reprovação, privilegiando métricas de Recall e F1 para a classe minoritária.
- Recomenda-se a execução do notebook em ambiente que suporte as versões indicadas das bibliotecas. # Students-Prevision
