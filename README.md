# Análise de Sentimentos com BERTimbau para IPT Soluções

Este projeto foi desenvolvido como parte da matéria de Residência em Software da Universidade Tiradentes, em colaboração com a empresa IPT Soluções. O objetivo principal é criar um modelo de Inteligência Artificial capaz de classificar textos em português de acordo com o sentimento expresso, utilizando uma arquitetura baseada no modelo BERT.

## 📜 Descrição do Projeto

O notebook `Previsão_de_sentimentos_com_Embbeding.ipynb` implementa um fluxo completo de Machine Learning para análise de sentimentos. Ele abrange desde o pré-processamento dos dados de texto, passando pelo treinamento de um modelo de Deep Learning, até a avaliação de sua performance e o uso para predições em novas frases.

O modelo é treinado para classificar textos em 6 categorias de sentimentos, sendo ideal para aplicações como análise de feedback de clientes, monitoramento de redes sociais ou automação de atendimento.

## ✨ Funcionalidades

* **Pré-processamento de Texto:** Limpeza e normalização de textos em português para otimizar a análise do modelo.
* **Análise de Sentimento:** Classificação de textos em 6 categorias distintas:
    * Satisfação
    * Frustração
    * Confusão
    * Urgência/Pressão
    * Raiva/Irritação
    * Neutro
* **Treinamento de Modelo:** Utiliza o poderoso modelo BERTimbau, uma versão do BERT pré-treinada para o português do Brasil.
* **Avaliação de Performance:** Gera uma matriz de confusão e um relatório de classificação para avaliar a precisão e outras métricas do modelo.

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Modelo de IA:** BERTimbau (`neuralmind/bert-base-portuguese-cased`)
* **Frameworks de Deep Learning:** TensorFlow e Keras
* **Bibliotecas Principais:**
    * `Hugging Face Transformers`: Para carregar e utilizar o modelo BERT.
    * `Pandas`: Para manipulação dos dados.
    * `TensorFlow-Text`: Para tokenização e pré-processamento de texto.
    * `Scikit-learn`: Para avaliação de métricas e matriz de confusão.
    * `ftfy` e `emoji`: Para limpeza e tratamento de texto.
    * `Seaborn` e `Matplotlib`: Para visualização de dados.
* **Ambiente:** Google Colab (recomendado, devido ao uso de GPU).

## 🗂️ Estrutura do Projeto

O projeto consiste em um único arquivo principal:

* `Previsão_de_sentimentos_com_Embbeding.ipynb`: Notebook Jupyter contendo todo o código para carregamento de dados, pré-processamento, definição, treinamento, avaliação e predição do modelo.

## ⚙️ Como Executar o Projeto

Siga os passos abaixo para configurar e executar o projeto em um ambiente Google Colab.

### 1. Pré-requisitos

* Uma conta Google para acessar o Google Colab e o Google Drive.
* O arquivo de dados `dataset_sentimentos_expandido (1).csv`.

### 2. Configuração do Ambiente

1.  **Faça o upload do dataset:** Suba o arquivo `dataset_sentimentos_expandido (1).csv` para o seu Google Drive. É recomendado criar uma pasta específica para o projeto, por exemplo, `MyDrive/BERT/`.

2.  **Abra o Notebook no Google Colab:** Faça o upload do arquivo `.ipynb` para o Colab e abra-o.

3.  **Instale as Dependências:** Execute a primeira célula de código que contém os comandos `pip install` para instalar todas as bibliotecas necessárias.
    ```bash
    pip install numpy pandas tensorflow tensorflow-text transformers ftfy emoji scikit-learn seaborn matplotlib
    ```

### 3. Atualize o Caminho do Dataset

No notebook, localize a célula que carrega o arquivo CSV. **Você precisa alterar o caminho** para corresponder ao local onde você salvou o dataset no seu Google Drive.

```python
# CÉLULA A SER ALTERADA
data = pd.read_csv('/content/drive/MyDrive/BERT/dataset_sentimentos_expandido (1).csv',
                   header=None,
                   names=cols,
                   engine='python',
                   encoding='utf-8')
