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
