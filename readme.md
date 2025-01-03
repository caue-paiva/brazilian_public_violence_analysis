:us:

## Data Analysis of the Historical Series from IPEA's "Map of Violence"

This project implements a Python script for data analysis and **visualization with plots** based on data from **IPEA** (Institute for Applied Economic Research) and its "Map of Violence" database. It allows analyzing data such as Homicide and Suicide Rates by state and year. The dataset also includes gender-separated data, enabling a historical series analysis of violence against women.

The script is operated via **terminal commands**, where the user inputs the years for analysis and specifies the dataset/historical series to be analyzed.

The **program automatically generates plots, one for each specified year**, based on the retrieved data. The plots will be saved in the current directory.

The datasets/historical series currently implemented are:

* Homicide rate
* Homicide rate for women
* Suicide rate
* Suicide rate for women

**Note:** The API data is provided by municipality, but it is aggregated by state to simplify the analysis and plot generation.

### How to Use the Code

1) Create a virtual environment to isolate dependencies:

```bash
python3 -m venv environment_name
```

2) Activate the virtual environment:

* Linux command
   ```bash
   source environment_name/bin/activate
   ```
* Windows command
   ```bash
   environment_name/Scripts/activate
   ```

3) Install the project dependencies
```bash
pip install -r requirements.txt
```

4) Run the project:
```bash
python3 projeto_final.py
```

5) Select the years and the historical series to analyze via terminal inputs.

### Auxiliary File
The file `info_municipios_ibge.csv` is a CSV extracted from IBGE databases, containing information about Brazilian municipalities. This file is necessary because the IPEA API only returns the municipality codes for the collected data. Therefore, it's required to map each code to its corresponding state to enable state-level aggregation and analysis.

### Python Libraries Used

* **Pandas**: A library for manipulating tabular data with DataFrames, enabling operations similar to `GROUP BY` and pivot tables on DataFrames.

* **Requests**: A library for making HTTP requests easily, simplifying API access.

* **Matplotlib**: A library for creating graphs from the extracted data.

### Inspiration
I am currently developing a [project](https://github.com/caue-paiva/intelli.gente_data_extraction) funded by FAPESP focused on **public data collection and analysis**. Therefore, I found it fitting to create a final project for the GRACE course monitors that also encompassed this theme.

Additionally, the IPEA "Map of Violence" database includes various historical series, such as gender-based violence and psychological violence, among others. This makes it possible to **expand the project to focus on collecting even more data on violence against women in Brazil**, providing a historical series that allows tracking changes in this scenario over time.


:br:

# Projeto Final Monitores Curso GRACE 2024

## Análise de Dados da Série Histórica do IPEA Mapa Da Violência.

Esse projeto implementa um script em Python para análise de dados e geração de **gráficos** a partir dos dados do **IPEA** (Instituto de Pesquisas Econômicas Aplicadas) e de sua base do "Mapa da Violência", permitindo analisar dados como Taxa de Homicídio e Suicídio com uma análise por estado e por ano. A base também contém dados separados por gênero, permitindo uma análise da série histórica de dados sobre violência contra a mulher.

A utilização do script se dá por **comandos no terminal**, no qual o usuário digita quais anos serão utilizados para a análise e qual dado/série histórica será analisado.

O **programa automaticamente gera gráficos, um para cada ano especificado**, a partir dos dados obtidos. Os gráficos serão salvos no diretório atual.

Os dados/séries históricas atualmente implementados são:

* taxa de homicídio

* taxa de homicídio de mulheres

* taxa de suicídio

* taxa de suicídio de mulheres

**OBS:** Os dados da API são por município, mas eles são agregados por Estado para facilitar a análise e desenho de gráficos.

### Como utilizar o código

1) Criar um ambiente virtual para baixar as dependências de forma isolada

```Bash
python3 -m venv nome_ambiente
```

2) Ativar o ambiente virtual:

* Comando no terminal do linux
   ```bash
   source nome_ambiente/bin/activate
   ```

* Terminal do Windows:
   ```bash
   nome_ambiente/Scripts/activate
   ```

3) Baixar as dependências do projeto:
```bash
pip install -r requirements.txt
```

4) Rodar o projeto:
```bash
python3 projeto_final.py
```

5) Escolher os anos e a série histórica a ser analisada, por meio de inputs no terminal.

### Arquivo Auxiliar
O arquivo "info_municipios_ibge.csv" é um csv extraido das bases do IBGE contendo informações sobre os municípios do Brasil. Ele é necessário pois a API do IPEA apenas retorna o código do município dos dados coletados, portanto é necessário mapear cada código ao seu estado para permitir uma agregação e análise pelos estados.

### Libraries do Python Utilizadas 

* **Pandas**: Library para manipulação de dados tabulares com DataFrames, permite operações similares a GROUP BY e tabelas pivô nos dataframes


* **Requests**: Library para realizar requests HTTP de forma mais fácil, permitindo acesso a API mais facilmente

* **Matplotlib**: Lib para criar os gráficos a partir dos dados extraidos


### Inspiração
Eu estou atualmente desenvolvendo um [projeto](https://github.com/caue-paiva/intelli.gente_data_extraction) com bolsa FAPESP sobre **coleta e análise de dados públicos**. Portanto eu achei pertinente fazer um projeto final do curso de monitores da GRACE que também englobasse esse tema. 

Além disso, a base do IPEA do Mapa da Violência contém diversas séries históricas, incluindo análise da violência por gênero, violência Psicológica... entre outras, então seria possível **expandir o projeto e focar em coletar ainda mais dados sobre a violência contra as mulheres no Brasil**, com uma série histórica permitindo ver a mudança nesse cenário ao longo do tempo.