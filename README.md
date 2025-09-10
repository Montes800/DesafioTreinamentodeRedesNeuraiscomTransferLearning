# 🧬 Projeto de Transfer Learning com CNN – Histologia Colorretal

Este projeto foi desenvolvido como parte de um desafio de Transfer Learning em Python, utilizando TensorFlow/Keras no Google Colab.

## 📌 O código original sugeria o uso do dataset Cats vs Dogs, mas eu substituí pelo dataset Colorectal Histology (histologia colorretal), que contém 8 classes de tecidos, fornecendo um desafio mais realista e científico.

## 👉 Além disso, contei com a ajuda da IA ChatGPT para organizar e otimizar o processo, garantindo um pipeline mais claro e funcional.

## 🔧 Alterações feitas em relação ao código original

Substituição do dataset:

## ❌ Antes: cats_vs_dogs

## ✅ Agora: colorectal_histology

Preprocessamento otimizado:

Normalização automática ([0,1])

Divisão em treino (80%) e teste (20%) já no carregamento via tensorflow_datasets

Estrutura do modelo:

Foi criada uma CNN do zero, mas também deixei preparado para possíveis testes com Transfer Learning (ex: VGG16).

Foram adicionadas camadas Conv2D + MaxPooling, seguidas de Flatten + Dense + Dropout para reduzir overfitting.

Otimização feita com ajuda da IA:

Organização do código em blocos bem comentados.

Explicação de cada etapa (pré-processamento, construção do modelo, treino, avaliação).

Automação do carregamento e batching dos dados.

## 📊 Estrutura do Código
1. Importação de Bibliotecas

Importação do TensorFlow, Keras e bibliotecas auxiliares.

2. Carregamento do Dataset

Uso do tfds.load("colorectal_histology") para carregar e dividir automaticamente em treino e teste.

3. Pré-processamento

Normalização das imagens.

Batching com 128 imagens.

Uso de cache e prefetch para acelerar o treino.

4. Construção da CNN

Três camadas convolucionais com ativação ReLU.

Pooling para redução dimensional.

Camada Flatten + Dense(256) + Dropout.

Saída final com softmax para 8 classes.

5. Compilação e Treinamento

Loss: sparse_categorical_crossentropy

Otimizador: adam

Métrica: accuracy

Treinamento com 10 épocas.

6. Avaliação

Impressão da acurácia no conjunto de teste.

Gráfico da evolução da acurácia ao longo das épocas.

## 📌 Exemplo de Saída
Número de classes: 8
Epoch 10/10
Train accuracy: 0.87
Validation accuracy: 0.84
Acurácia no conjunto de teste: 0.85
