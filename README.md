# 📉 Previsão de Desemprego Juvenil na Zona do Euro com LSTM

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![Status](https://img.shields.io/badge/Status-Concluído-green)

> Uma análise preditiva utilizando Deep Learning para modelar tendências econômicas complexas com base em dados históricos reais.

---

## 📋 Sobre o Projeto

Este projeto aplica redes neurais recorrentes do tipo **LSTM (Long Short-Term Memory)** para prever a taxa de desemprego na Zona do Euro. O objetivo principal foi validar a capacidade dessa arquitetura de Deep Learning em capturar padrões não-lineares e responder a choques econômicos, como a crise da COVID-19.

A análise utiliza uma série temporal histórica real, cobrindo o período de **1990 a 2023**, extraída da base de dados do Federal Reserve (FRED).

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Modelagem & Deep Learning:** TensorFlow / Keras (LSTM)
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização:** Matplotlib
* **Pré-processamento:** Scikit-Learn (MinMaxScaler)
* **Design da Apresentação:** Figma

## 📊 Metodologia

1.  **Coleta de Dados:** Extração da série histórica `HIGN00EA19M052N` (Harmonized Unemployment Rate) do FRED.
2.  **Pré-processamento:** Normalização dos dados (escala 0-1) para otimizar a performance da rede neural.
3.  **Janelamento (Windowing):** Criação de janelas deslizantes de 12 meses (Look-back) para treinar o modelo a olhar para o passado antes de prever o futuro.
4.  **Treinamento:** Modelo sequencial com camada LSTM e Dense, otimizado com Adam e função de perda MSE.

## 🚀 Resultados

O modelo demonstrou alta aderência aos dados reais, com destaque para:

* **Precisão:** Erro Médio Quadrático (MSE) final de **0.0024** na escala normalizada.
* **Sensibilidade:** Capacidade de acompanhar a subida abrupta do desemprego durante a pandemia de 2020 e a subsequente recuperação econômica.
* **Robustez:** Ausência de *overfitting* significativo, com as curvas de treino e validação convergindo adequadamente.

![Gráfico de Resultados](images/result_chart.png)

## 📂 Estrutura do Repositório

* `/data`: Arquivos CSV utilizados.
* `/notebooks`: Código fonte completo em Jupyter Notebook.
* `/presentation`: Slides do projeto.
* `/images`: Gráficos gerados.

## 👨‍💻 Autores

* **Gabriel Lopes Cavallari** - *Análise de Dados, Visualização e Documentação*
* **Derek Amaral** - *Implementação do Modelo LSTM e Pesquisa*

---
*Este projeto foi desenvolvido como parte da disciplina de Inteligência Artificial do IFSP.*
