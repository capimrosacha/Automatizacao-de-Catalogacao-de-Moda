# 👗 Automatização de Catalogação de Moda com Deep Learning

Este projeto utiliza Redes Neurais Artificiais (MLP - Multi-Layer Perceptron) para classificar automaticamente itens de vestuário utilizando o dataset **Fashion MNIST**. O objetivo principal é criar um sistema capaz de categorizar produtos de forma automatizada para otimizar processos de e-commerce e logística.

## 📊 O Dataset
O conjunto de dados **Fashion MNIST** consiste em:
* **60.000** imagens para treinamento.
* **10.000** imagens para teste.
* Imagens em tons de cinza com resolução de **28x28 pixels**.
* **10 classes** distintas de produtos (Camisetas, Calças, Bolsas, etc.).

## 🧠 Arquiteturas e Experimentos
O projeto explora diferentes configurações de redes neurais para encontrar o melhor equilíbrio entre acurácia e generalização:

* **Modelo Robusto (ReLU):** Camadas densas com ativação ReLU para capturar relações não lineares.
* **Funções de Ativação:** Testes comparativos utilizando as funções `Tanh` e `Sigmoide`.
* **Técnicas de Regularização:**
    * **Dropout:** Inclusão de camadas de descarte (ex: 20%) para reduzir o overfitting.
    * **L1 e L2:** Penalização de pesos para melhorar a robustez do modelo.
* **Otimização Dinâmica:**
    * `EarlyStopping`: Interrupção do treino ao detectar estagnação na perda de validação.
    * `ReduceLROnPlateau`: Redução automática do *learning rate* quando o desempenho para de melhorar.

## 🛠️ Tecnologias Utilizadas
* **Python 3.x**
* **TensorFlow / Keras**: Construção e treinamento das redes neurais.
* **Scikit-learn**: Divisão de dados e métricas de avaliação.
* **Matplotlib / Seaborn**: Visualização de métricas e matrizes de confusão.
* **Numpy**: Processamento numérico e manipulação de arrays.

## 🚀 Como Executar

### 1. Pré-processamento
O código realiza as seguintes etapas automaticamente:
1. **Normalização:** Escalonamento dos pixels para valores entre 0 e 1.
2. **Reshape:** Transformação das imagens em vetores unidimensionais de 784 posições.
3. **One-Hot Encoding:** Codificação das classes para saídas categóricas.

### 2. Instalação de Dependências
```bash
pip install tensorflow scikit-learn matplotlib seaborn numpy
```
### 3. Instalação de Dependências
```bash
python catalogacao_moda.py
```

📈 Resultados Visualizados
O projeto gera automaticamente:

1. **Curvas de Acurácia e Perda:** Para monitorar o aprendizado em tempo real.

2. **Matriz de Confusão:** Para identificar quais peças de roupa o modelo tem mais dificuldade em distinguir.

Equipe: Eric Rodrigues Arrais & Kenya Tyeh Kusano Santos | 
Data: 06/09/2025
