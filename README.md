# Produção hospitalar do SUS em Salvador

Trabalho da AV3 da disciplina Análises de Negócios com Uso de Big Data.

## Objetivo

Analisar como as Autorizações de Internação Hospitalar (AIHs) processadas em Salvador se distribuíram por estabelecimento, mês e nível de complexidade entre janeiro e junho de 2024.


## Base de dados

Usamos os dados de produção hospitalar do SIH/SUS, publicados
pelo Ministério da Saúde no Portal de Dados Abertos do SUS.

Do ZIP de 2024, utilizamos os seis arquivos mensais de janeiro a junho.
Os arquivos seguem o padrão `sih_procedimentos_hospitalares_sus_{mes}_2024.csv`,
com `jan`, `fev`, `mar`, `abr`, `mai` e `jun`.

Os seis CSVs têm 859.694.413 bytes descompactados e contêm 2.727.557 linhas.
Após filtrar pelo município do atendimento (`IBGE = 292740`), o recorte
de Salvador ficou com 51.775 linhas e 16 colunas de origem.

Data de acesso: 22/11/2026.

[Página oficial da base](https://dadosabertos.saude.gov.br/dataset/sih_producao_hospitalar)
· [Download do ZIP de 2024](https://s3.sa-east-1.amazonaws.com/ckan.saude.gov.br/saes/drac/SIH_Pprocedimento_Hosp/csv/sih_procedimentos_hospitalares_sus_2024_csv.zip)

## Como executar

1. Baixe o [notebook AV3 AIH SALVADOR.ipynb](AV3%20AIH%20SALVADOR.ipynb).
2. No Google Colab, vá em **Arquivo → Fazer upload de notebook** e selecione o arquivo.
3. Clique em **Ambiente de execução → Executar tudo**.

A primeira célula baixa o ZIP oficial do SIH/SUS. As células seguintes
filtram os registros de Salvador, preparam a base e exibem as tabelas
e o gráfico da análise.

## Ambiente de execução

O notebook foi executado no Google Colab com estas versões:

- Python 3.13.18
- pandas 2.2.3 — leitura, limpeza e análise dos dados
- Matplotlib 3.10.0 — geração do gráfico
- PyArrow 23.0.1 — exportação da base tratada em Parquet

  ## Integrantes

- CAMILA LACERDA BARBOSA
- DEIVSON LAUREANO VIEIRA PIRES
- LEONARDO DA SILVA BADAUÊ
- LUCAS KELVIM SILVA CASTRO
- WENDEL SANTOS MUNIZ
- YAN MOTA ESQUIVEL DAS NEVES

## Organização do repositório

- `AV3 AIH SALVADOR.ipynb` — notebook com a importação, a limpeza e a análise dos dados.
- `requirements.txt` — bibliotecas e versões usadas no projeto.
- `README.md` — descrição do trabalho, fonte dos dados e instruções de execução.
