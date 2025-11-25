## Embrapa -  Área plantada do gergelim no Brasil em 2024


# Base de dados

Este repositório reúne implementações de modelos de Inteligência Artificial aplicados a bases de dados públicas. Como estudo de caso, utiliza dados geoespaciais da Embrapa (GeoInfo) referentes à área plantada de gergelim no Brasil em 2024. O projeto inclui pré-processamento dos dados, construção e treinamento de redes neurais.

 [https://geoinfo.dados.embrapa.br/metadados/srv/por/catalog.search#/metadata/2bef1465-96f3-4132-8670-6382efd603a7] 



**Atributos do Dataset**

|Nome|
|---------------|
|ogc_fid|	
|id|	
|cd_geocodu|	
|nm_estado|	
|nm_regiao|	
|area|	
|area_plant|	
|prod_mil_t|	
|prodt_kgha|	
|geometry|	



# Problema de Interesse

O problema de interesse neste projeto é de regressão, pois o objetivo é prever valores contínuos relacionados à área plantada de gergelim no Brasil. Utilizando dados geoespaciais e variáveis ambientais provenientes de bases públicas, busca-se treinar modelos baseados em Redes Neurais capazes de estimar a quantidade de área plantada em diferentes regiões, contribuindo para análises agrícolas e suporte à tomada de decisão. 



# Arquitetura de rede neural

**MLP (Multi-Layer Perceptron)** 

Por que MLP?
Os dados geoespaciais foram transformados em uma tabela (ex.:), configurando o problema em tabular, e o MLP apresenta um bom desempenho, com:


- Baixa complexidade de implementação

- Treinamento rápido

- Bom desempenho em regressão com dados estruturados (aprendizado supervisionado, previsão de área)

- Fácil ajuste de hiperparâmetros

- Resolvem problemas não-linearmente separáveis, usadas para regressão ou classificação complexa


**Arquitetura de uma MLP**

- Camada de Entrada (Input Layer): Recebe dados brutos de entrada (cada neurônio = uma feature).

- Camadas Ocultas (Hidden Layers): Fazem combinações não-lineares dos dados, permitindo resolver problemas complexos e não-linearmente separáveis

- Camada de Saída (Output Layer): Gera a resposta final (classe, valor de regressão etc.), depende da tarefa (número de neurônios igual ao número de classes na classificação multiclasses, por exemplo)