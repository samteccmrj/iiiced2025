# III CED 2025

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-blue.svg)](https://creativecommons.org/licenses/by/4.0/)

## Análise e Clusterização de Dados Educacionais

Este repositório contém os scripts utilizados para análise exploratória, clusterização e avaliação de ganhos de aprendizagem em dados educacionais coletados durante uma formação docente sobre Inteligência Artificial aplicada à Educação.

A análise combina técnicas de **mineração de dados**, **aprendizagem não supervisionada** e **análises estatísticas**, com o objetivo de identificar perfis docentes e investigar mudanças nas competências relacionadas ao uso educacional da IA.

## Estrutura do Repositório

```
iiiced2025
│
├── README.md
├── dados
│   └── dataset_pre_teste.xlsx
│   └── dataset_pos_teste.xlsx
│
├── iii_ced_2025.ipynb
│   └── clusterizacao_ia_educacao.ipynb
│
└── LICENSE
```

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

A análise foi conduzida nas seguintes etapas:

1. **Análise exploratória dos dados (EDA)**  
   - inspeção das distribuições das respostas
   - verificação de consistência do dataset

2. **Padronização das variáveis**  
   - aplicação do método *StandardScaler*

3. **Clusterização com algoritmo K-Means**  
   - identificação de perfis docentes

4. **Definição do número de clusters**
   - Método do Cotovelo (*Elbow Method*)
   - Índice de Silhueta (*Silhouette Score*)

5. **Visualização dos clusters**
   - projeção dos dados em duas dimensões com **PCA**

6. **Análise de evolução após a formação**
   - projeção dos dados do pós-teste nos clusters identificados

7. **Análise estatística**
   - teste de **Wilcoxon** para comparação pré e pós
   - correlação de **Spearman** entre avaliação da formação e ganho de aprendizagem

## Resultados

A análise identificou **três perfis docentes** quanto à familiaridade com o uso educacional da Inteligência Artificial:

- **Perfil de Aproximação Inicial com IA**
- **Perfil de Experimentação Pedagógica com IA**
- **Perfil de Integração Pedagógica da IA**

A comparação entre pré-teste e pós-teste indicou mudanças na distribuição dos perfis, sugerindo evolução no nível de familiaridade com ferramentas de IA após a participação na formação.

Também foi observado:

- **ganho médio absoluto de aprendizagem:** 6,63 pontos
- **ganho normalizado médio:** 0,36
- **teste de Wilcoxon:** diferença estatisticamente significativa entre pré e pós-testes ($p < 0.001$)
- **correlação de Spearman:** associação moderada entre avaliação da formação e ganho de aprendizagem ($\rho = 0.50$)

## Tecnologias Utilizadas

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Referências Metodológicas

- Tan, P., Steinbach, M., & Kumar, V. (2016). *Introduction to Data Mining*.
- Rousseeuw, P. (1987). Silhouettes: A graphical aid to the interpretation and validation of cluster analysis.
- Jolliffe, I. (2016). *Principal Component Analysis*.
- Pallant, J. (2020). *SPSS Survival Manual*.

## Reprodutibilidade

A análise pode ser reproduzida diretamente no Google Colab ou em ambiente Python local.

### Execução no Google Colab (recomendado)

1. Acesse o Google Colab:  
https://colab.research.google.com

2. Faça o upload do notebook disponível neste repositório:

iii_ced_2025.ipynb

3. Faça o upload dos datasets localizados em:

dados/dataset_pre_teste.xlsx  
dados/dataset_pos_teste.xlsx

4. Execute as células do notebook sequencialmente.

O ambiente do Google Colab já possui as bibliotecas necessárias para execução da análise.

### Execução local (opcional)

Caso prefira executar localmente, instale as dependências necessárias:

pip install pandas scikit-learn matplotlib seaborn jupyter

Em seguida, execute o notebook:

jupyter notebook
