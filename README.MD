# Análise de Sentimento de Resenhas de Filmes no IMDB

Este projeto utiliza o **conjunto de dados IMDB**, que contém 50.000 análises de filmes classificadas como positivas ou negativas. A análise é realizada utilizando técnicas de **Processamento de Linguagem Natural (NLP)**.

## Índice

1. [Conjunto de Dados](#conjunto-de-dados)
2. [Objetivo](#objetivo)
3. [Como Utilizar](#como-utilizar)
   - [Usando Poetry](#usando-poetry)
   - [Usando Ambiente Virtual](#usando-ambiente-virtual)
4. [Resultados](#resultados)

## Conjunto de Dados

O conjunto de dados utilizado pode ser baixado diretamente do Kaggle: [IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews).

## Objetivo

O objetivo deste projeto é explorar técnicas de NLP, comparando o modelo TF-IDF com a arquitetura Transformers, a fim de avaliar a eficácia de cada abordagem na análise de sentimentos. 

Acesse [IMDB.ipynb](IMDB.ipynb) para ter detalhes do estudo.

## Como Utilizar

Para utilizar este repositório, recomenda-se criar um ambiente virtual ou utilizar um gerenciador de dependências, como o Poetry. Abaixo, estão as instruções para ambas as abordagens:

### Usando Poetry

1. Instale o Poetry via pipx:

   ```bash
   pipx install poetry
   ```

2. Navegue até o diretório do projeto:

   ```bash
   cd caminho/para/o/projeto
   ```

3. Instale as dependências:

   ```bash
   poetry install
   ```

### Usando Ambiente Virtual

1. Crie um ambiente virtual:

   ```bash
   python -m venv ambiente_virtual
   ```

2. Ative o ambiente virtual:
   - Em Linux ou macOS:

     ```bash
     source ambiente_virtual/bin/activate
     ```

   - Em Windows:

     ```bash
     ambiente_virtual\Scripts\activate
     ```

3. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

## Resultados

Os resultados das métricas de cada modelo podem ser vistos previamente a seguir:

| Métrica          | TF-IDF + LinearSVC         | Transformers            |
|------------------|-----------------------------|--------------------------|
| **Negativas**    |                             |                          |
| Precision         | 0.91                        | 0.69                     |
| Recall            | 0.89                        | 0.93                     |
| F1-Score          | 0.90                        | 0.79                     |
| Support           | 4961                        | 21314                    |
| **Positivas**    |                             |                          |
| Precision         | 0.90                        | 0.89                     |
| Recall            | 0.92                        | 0.58                     |
| F1-Score          | 0.91                        | 0.70                     |
| Support           | 5039                        | 21124                    |
| **Acurácia**     | 0.90 (10.000)              | 0.76 (42.438)           |
| **Média Macro**  |                             |                          |
| Precision         | 0.91                        | 0.79                     |
| Recall            | 0.90                        | 0.76                     |
| F1-Score          | 0.90                        | 0.75                     |
| Support           | 10.000                     | 42.438                   |
| **Média Ponderada** |                           |                          |
| Precision         | 0.90                        | 0.79                     |
| Recall            | 0.90                        | 0.76                     |
| F1-Score          | 0.90                        | 0.75                     |
| Support           | 10.000                     | 42.438                   |

