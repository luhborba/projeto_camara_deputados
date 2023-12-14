# Projeto Câmara dos Deputados

Projedo de construção de um DW para posterior análise dos dados retirados diretamente do site da camara dos deputados.

### 📋 Pré-requisitos

De que coisas você precisa para instalar o software e como instalá-lo? 
Basicamente não, estou utilizando o Google Colaboratory, sendo necessário apenas instalar a biblioteca pyspark

```
!pip install pyspark
```
Para obter os dados acesse: 
https://dadosabertos.camara.leg.br/swagger/api.html#staticfile
Neste projetos os dados foram retirados na data 20/10/2023

### Ações realizadas

* Identificação e Mapeamento dos Dados
* Avaliação de dados
* Modelagem Dimensional (Divisão de dados em Fato - Dimensões)
* PySpark para Tratamento de Dados
* Criação de DW com SQL
* Inserção de Dados

## Projeto Construído com 

* Python
* Google Colaboratory
* PySpark
* Pandas
* Modelagem Dimensional
* SGBD PostgreSQL
* Power BI
* Render 

## Explicação

Comecei o projeto utilizando o pandas para tratar dados de deputados, que foram extraidos diretamente do câmara dos deputados. Porém após uma outra análise dos dados decidi utilizar todo o processo no arquivo 'Ano-2023.csv', utilizei o pyspark no ambiente do Google Colaboratory, anter de iniciar o uso do pyspark realizei uma análise rápida através do próprio csv, entendendo os dados presentes e construindo uma modelagem dimensional para melhor analisar dos dados, buscando melhor performace nas análises.


Nesta primeira etapa foi criado os DataFrames de Deputados, Categorias e Empresas que seram as dimensões, para posterior criação do dataframe fato_gastos.
Todo esse passo a passo está documentando no meu linkedin:
<p><a href="https://www.linkedin.com/pulse/saga-portif%25C3%25B3lio-parte-2-usando-pyspark-luciano-borba-tzyuf/?trackingId=jWArR5GSTmKK0S5GCIJBEA%3D%3D" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="luhborba" height="30" width="40" /></a></p>

Depois realizei a modificação dos tipos de dados no DataFrame, pois todos estavam como long e/ou string em todos os DataFrames criados.
Segue postagem:
<p>
<a href="https://www.linkedin.com/pulse/saga-portif%25C3%25B3lio-parte-3-modificando-tipo-de-dados-das-luciano-borba-hs57f/?trackingId=jWArR5GSTmKK0S5GCIJBEA%3D%3D" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="luhborba" height="30" width="40" /></a></p>

Após a limpeza e modelagem dos dados, a proxima etapa foi a criação do Data Warehouse para este projeto, utilizei o SGBD do PostgreSQL, comecei inicialmente com um Banco Local, no decorrer do processo de construção do projeto migrei para o Render, utilizando uma instância gratuita na cloud de PostgreSQL. Utilizei comandos SQL para criação do banco, você pode chegar na minha postagem do Linkedin:
<p><a href="https://www.linkedin.com/pulse/saga-portif%25C3%25B3lio-parte-3-criando-dw-com-sql-sgbd-postgresql-borba-ybbff/?trackingId=jWArR5GSTmKK0S5GCIJBEA%3D%3D" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="luhborba" height="30" width="40" /></a></p>

Depois fiz a inserção dos dados de forma manual utilizando o pgAdmin 4:
<p><a href="https://www.linkedin.com/pulse/saga-portif%25C3%25B3lio-parte-5-inserindo-dados-dw-da-forma-luciano-borba-okmcf/?trackingId=jWArR5GSTmKK0S5GCIJBEA%3D%3D" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="luhborba" height="30" width="40" /></a></p>

Agora foi o momento de especificar quais perguntas eu quero responder, como também foram realizados alguns ajustes:
Segue postagem:
<p><a href="https://www.linkedin.com/pulse/saga-portif%25C3%25B3lio-parte-6-perguntas-e-ajustes-luciano-borba-xubwf/?trackingId=GegGtnwaaFXzYBLvMmi2Dw%3D%3D" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="luhborba" height="30" width="40" /></a></p>

Por fim, vem a construção do DataViz utilizando o PowerBI:
Segue postagem:
<p><a href="https://www.linkedin.com/pulse/saga-portif%2525C3%2525B3lio-parte-7-dataviz-com-power-bi-luciano-borba-myhif%3FtrackingId=mzzxLUuaQaeP8dPF48uN5g%253D%253D/?trackingId=mzzxLUuaQaeP8dPF48uN5g%3D%3D" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="luhborba" height="30" width="40" /></a></p>

Segue dashboard:
https://app.powerbi.com/view?r=eyJrIjoiZGJjZDYyYzEtOWQ4Yy00MzIwLWI2MTUtM2FmYTY2NTUyZGI5IiwidCI6IjM2ZjUxZmFhLThiYTItNDcxNy1iMmFlLTEwNTIxNzFjNjM0YiJ9
