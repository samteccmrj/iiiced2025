# III CED 2025

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-blue.svg)](https://creativecommons.org/licenses/by/4.0/)

# Análise e Clusterização de Dados Educacionais

Este repositório contém os scripts e procedimentos utilizados para análise exploratória e clusterização de dados educacionais utilizando técnicas de mineração de dados.

O objetivo da análise é identificar perfis de participantes a partir de respostas coletadas em questionários educacionais, utilizando métodos de aprendizagem não supervisionada.

## Estrutura do Repositório

├── dados/
│  ├── dataset_pre_teste.xlsx
│  ├── dataset_pos_teste.xlsx
├── iii_ced_2025.ipynb
├── README.md
└── LICENSE


## Conjunto de Dados

O dataset utilizado contém respostas de professores participantes de uma formação sobre Inteligência Artificial aplicada à Educação.

As variáveis analisadas correspondem a oito afirmações avaliadas em escala Likert (1 a 5), relacionadas a:

- compreensão sobre Inteligência Artificial na Educação
- identificação de aplicações pedagógicas
- percepção de riscos éticos
- orientação aos estudantes
- elaboração de prompts
- refinamento de solicitações em ferramentas de IA
- identificação de atividades educacionais apoiadas por IA
- personalização de materiais educacionais com IA

## Metodologia

A análise foi conduzida em três etapas principais:

1. **Análise exploratória dos dados**
2. **Clusterização utilizando o algoritmo K-means**
3. **Visualização dos grupos identificados**

Para definição do número de clusters foi utilizado:

- método do cotovelo (Elbow Method)
- métrica de Silhouette

Para visualização da distribuição dos grupos foi aplicada:

- **Análise de Componentes Principais (PCA)**

## Resultados

A análise identificou três perfis principais de participantes:

- **Perfil de Aproximação Inicial com IA**
- **Perfil de Experimentação Pedagógica com IA**
- **Perfil de Integração Pedagógica da IA**

Esses perfis representam diferentes níveis de familiaridade e integração pedagógica da Inteligência Artificial no contexto educacional.

## Tecnologias Utilizadas

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Reprodutibilidade

A análise pode ser reproduzida diretamente no Google Colab ou em ambiente Python local.

### Execução no Google Colab (recomendado)

1. Acesse o Google Colab:  
https://colab.research.google.com

2. Faça o upload do notebook disponível neste repositório:

iii_ced_2025.ipynb

3. Faça também o upload do dataset localizado em:

dados/dataset_pre_teste.xlsx


4. Execute as células do notebook sequencialmente.

O ambiente do Google Colab já possui as bibliotecas necessárias para execução da análise.

### Execução local (opcional)

Caso prefira executar localmente, instale as dependências necessárias:

pip install pandas scikit-learn matplotlib seaborn jupyter

Em seguida, execute o notebook:

jupyter notebook
