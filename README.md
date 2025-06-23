# Detecção de Fraudes com Machine Learning

Este projeto tem como objetivo desenvolver e avaliar modelos de machine learning e deep learning para a detecção de fraudes em transações financeiras.

## 🚀 Requisitos

Para rodar o projeto corretamente, você precisa:

- Python 3.10+
- pip atualizado
- Ambiente virtual (recomendado)
- As seguintes bibliotecas instaladas:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn
  - imbalanced-learn
  - torch (PyTorch)
  - joblib
  - kagglehub

## ▶️ Como Rodar

1. Clone este repositório
2. Crie e ative um ambiente virtual
3. Instale as dependências
4. Coloque os datasets em `/data/raw/` conforme necessário
5. Execute os notebooks desejados encontrados no diretório `notebooks/`

Os principais notebooks são:

- `data-clean.ipynb` - Análise Exploratória, limpeza, balanceamento e _encoding_ dos dados
- `neural-network.ipynb` — Rede Neural V1
- `neural-network-v2.ipynb` — Rede Neural V2 (estrutura alternativa)
- `random-forest.ipynb` — Modelo Random Forest

## 🧠 Sobre a RNA V1

A primeira versão da Rede Neural Artificial foi construída com uma arquitetura simples composta por três camadas lineares e funções de ativação ReLU. Utiliza função de ativação Sigmoid na saída, sendo adequada para classificação binária.

Ela foi treinada sobre um dataset balanceado com SMOTE e os dados normalizados com StandardScaler.

Hiperparâmetros principais:

- 3 camadas densas (64 → 32 → 1)
- Função de perda: BCE Loss
- Otimizador: Adam
- Epochs: 20
- Batch size: 256

## 📊 Avaliação da RNA V1

O modelo foi avaliado por meio de:

- Acurácia
- Precisão
- Recall
- F1-Score

## Outras Abordagens

### Rede Neural Artificial V2

Com o objetivo de melhorar as métricas da RNA inicial, uma nova versão foi implementada (V2), com ajustes como aumento do número de neurônios e camadas, uso de dropout para regularização e aumento do número de épocas. No entanto, apesar da expectativa de ganho de desempenho, o modelo V2 apresentou um leve declínio nas métricas de classificação em comparação com a versão V1. Possivelmente, o aumento da complexidade contribuiu para overfitting ou instabilidade no treinamento. Por isso, o modelo V1 foi mantido como principal referência para comparação.

### Random Forest

Além da RNA, foi também implementado um modelo baseado em Random Forest, utilizando a biblioteca scikit-learn. A abordagem seguiu a estrutura padrão de separação dos dados em treino e teste, normalização com StandardScaler, treinamento do classificador e avaliação dos resultados. O modelo apresentou excelente desempenho, com alta acurácia, recall e F1-score, sendo uma alternativa robusta e interpretável para o problema de detecção de fraudes.

## 💡 Considerações

A RNA demonstrou bom desempenho na detecção de fraudes. Posteriormente, foram realizados aprimoramentos na versão V2, incorporando regularização com Dropout e aumentando a complexidade da rede.

Também foram implementados modelos alternativos como Random Forest para comparação de desempenho.

## 📂 Estrutura

- `data/`: diretório para os dados brutos e processados
- `notebooks/`: notebooks de experimentação e treino
- `models/`: modelos salvos (.pth, .joblib)

## 🔮 Trabalhos Futuros

Sugerem-se melhorias como:

- Integração dos modelos em sistemas reais
- Exploração de técnicas como LSTM, autoencoders e ensembles híbridos
- Implementação da validação cruzada (k-fold) para maior robustez dos resultados
- Monitoramento contínuo de performance em produção, com revalidação periódica

---

Fonte: Este projeto foi desenvolvido como parte de um Trabalho de Conclusão de Curso sobre detecção de fraudes com redes neurais e aprendizado de máquina.

Autores: Guilherme Batista Fernandes Coelho & Diego Motta
