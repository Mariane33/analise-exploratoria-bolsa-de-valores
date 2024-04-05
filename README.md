# Aula 01: Análise Exploratória com Google Sheets

Nesta aula, exploramos o uso do Google Sheets para análise exploratória de dados da bolsa de valores. Utilizamos diversas fórmulas como VLOOKUP e SUMIF, além de interagir com o ChatGPT para gerar insights adicionais.

## Objetivos

- Analisar as bases de variações na B3.
- Realizar análises exploratórias pelo Google Sheets com fórmulas.
- Utilizar o ChatGPT para obter insights adicionais.
- Gerar tabelas e calcular estatísticas como Máximo, Mínimo e Média.

## Desafios desta aula

Além dos objetivos principais, os seguintes desafios foram propostos:

1. Calcular as variações percentuais (semanal, mensal, anual e em 12 meses).
2. Utilizar o ChatGPT para obter faixas de idade.
3. Pedir ao ChatGPT para gerar a fórmula IF para as faixas de idade.

## Soluções Encontradas

- **Desafio 1**: Para calcular as variações percentuais, utilizamos as fórmulas do Google Sheets para realizar os cálculos com base nos dados fornecidos.
- **Desafio 2**: Interagimos com o ChatGPT para obter as faixas de idade e as integramos ao nosso projeto.
- **Desafio 3**: Utilizamos o ChatGPT para gerar a fórmula IF para as faixas de idade, facilitando o processo de análise e categorização dos dados.

# Aula 02: Gráficos e Análises com Google Colab e Python Pandas

Nesta aula, exploramos a geração de gráficos e tabelas no Google Sheets, além de iniciar a manipulação de dados com Python Pandas no Google Colab.

## Objetivos

- Gerar tabelas e cálculos de estatísticas.
- Criar gráficos no Google Sheets.
- Conhecer o Google Colab.
- Iniciar a manipulação de dados com Python Pandas.

## Desafios desta aula

Além dos objetivos principais, os seguintes desafios foram propostos:

1. Criar um gráfico de barras olhando a faixa etária e o valor da variação.
2. Fazer outro gráfico de barras com a faixa etária e a quantidade de empresas que estão em cada faixa etária.
3. Explorar os tipos de gráficos com os dados já feitos.

## Soluções Encontradas

- **Desafio 1**: Para criar o gráfico de barras com a faixa etária e o valor da variação, utilizamos as funções adequadas do Google Sheets para extrair os dados de forma eficaz.
- **Desafio 2**: Para o segundo gráfico de barras, contamos o número de empresas em cada faixa etária e plotamos os resultados.
- **Desafio 3**: Exploramos diferentes tipos de gráficos, como gráficos de linha, gráficos de pizza, entre outros, para visualizar os dados de maneira variada e compreender melhor os insights.

# Aula 03: Manipulação de Dados e Criação de Gráficos com bibliotecas Python

Nesta aula, continuamos a manipulação de dados com Pandas no Google Colab, desta vez transformando a planilha de ações. Além disso, começamos a construir gráficos com a biblioteca Plotly.

## Objetivos

- Manipular dados com Pandas.
- Transformar a planilha de ações com funções do Pandas.
- Construir gráficos com a biblioteca Plotly Express.
- Usar o Chat GPT durante o código.

## Desafios desta aula

Além dos objetivos principais, os seguintes desafios foram propostos:

1. Pesquisar com a documentação da biblioteca Plotly como mudar a formatação dos números do gráfico de barras.
2. Fazer o gráfico de pizza no df_analise_segmento com a mesma biblioteca Plotly.
3. Fazer o GroupBy da categoria de idades e gerar o gráfico de barras.

## Soluções Encontradas

- **Desafio 1**: Para mudar a formatação dos números do gráfico de barras, consultei a documentação da biblioteca Plotly: (https://plotly.com/python/bar-charts/).
- **Desafio 2**: Para fazer o gráfico de pizza no df_analise_segmento com a biblioteca Plotly, utilizei o seguinte código:
  ```python
  import plotly.express as px

  fig = px.pie(df_analise_segmento, names='Segmento', values='Variacao_rs', title='Variação Reais por Segmento')
  fig.show()
- **Desafio 3**: Para fazer o GroupBy da categoria de idades e gerar o gráfico de barras, utilizei o seguinte código:
python

df_analise_cat_idade = df_principal.groupby('Cat_idade')['Variacao_rs'].sum().reset_index()

fig = px.bar(df_analise_cat_idade, x='Cat_idade', y='Variacao_rs', text='Variacao_rs', title='Variação Reais por Categoria de Idade')
fig.show()

