# Detecção de Bots no Twitter usando BERT no Keras

## Objetivo

#### O objetivo deste projeto é treinar uma rede neural utilizando o modelo BERT no Keras para detectar bots no Twitter. O modelo será treinado com o dataset **Twitter-Bot Detection**, disponível no Kaggle.

## Estrutura do Relatório

1. [Introdução](#introdução)
2. [Metodologia](#metodologia)
3. [Preparação dos Dados](#preparação-dos-dados)
4. [Arquitetura da Rede Neural](#arquitetura-da-rede-neural)
5. [Treinamento do Modelo](#treinamento-do-modelo)
6. [Avaliação do Modelo](#avaliação-do-modelo)
7. [Resultados](#resultados)
---

## 1. Introdução

O crescimento da atividade de bots no Twitter tem gerado grandes preocupações no campo da cibersegurança e da confiança em plataformas de mídia social. Identificar contas automatizadas de bots de forma eficaz é essencial para manter a integridade dessas plataformas.

Este projeto utiliza **BERT (Bidirectional Encoder Representations from Transformers)**, uma técnica poderosa de modelagem de linguagem, aplicada à detecção de bots.

## 2. Metodologia

A abordagem envolve os seguintes passos:

- Carregar e explorar o dataset **Twitter-Bot Detection** do Kaggle.
- Realizar pré-processamento do texto dos tweets.
- Utilizar o modelo BERT pré-treinado para representar as sequências de texto.
- Construir uma rede neural no Keras para classificar as contas como "Bot" ou "Humano".
- Avaliar o desempenho do modelo com métricas adequadas.


## 3. Preparação dos Dados

1. **Importação dos Dados**: O dataset foi importado e explorado para entender melhor sua estrutura.
2. **Entendimento da Estrutura**: Visualização do tamanho de cada um dos tweets
3. **Tokenização**: Os tweets foram tokenizados usando o tokenizador do BERT para prepará-los para o modelo.


## 4. Arquitetura da Rede Neural

A rede neural utilizada foi baseada no modelo BERT pré-treinado com uma camada densa adicional para a classificação binária. A arquitetura é composta por:

- **Camada BERT**: Carregando o modelo pré-treinado para transformar os textos em embeddings de alta dimensionalidade.
- **Camadas Densas**: Para ajuste fino, utilizamos algumas camadas densas para ajustar os pesos e realizar a classificação final.
- **Camada de Saída**: Com uma única unidade e função de ativação Sigmoid, para classificação binária (Bot ou Humano).

## 5. Treinamento do Modelo

1. **Compilação do Modelo**: O modelo foi compilado utilizando o otimizador Adam e a função de perda `binary_crossentropy`.
2. **Treinamento**: O modelo foi treinado em 2 épocas, tendo em vista o fato do modelo BERT ser um pouco demorado para rodar.

## 6. Avaliação do Modelo

O modelo foi avaliado utilizando as seguintes métricas:

- **Accuracy**: Percentual de previsões corretas.
- **Precision e Recall**: Para avaliar a qualidade das previsões em termos de precisão e cobertura.

## 7. Resultados

O modelo apresentou os seguintes resultados:

- **Acurácia Final**: 50.4%
- **Precision**: 50.4%
