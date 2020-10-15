# Desafio SQL - Analista de Dados

Este desafio tem como objetivo testar suas habilidades em análise de dados utilizando SQL. O desafio é baseado em problemáticas reais, e visa ao máximo trazer a você um cenário próximo ao da realidade de um Analista de Dados na HVAR Consulting.

# Cenário

Para este desafio, considere o seguinte cenário: A HVAR Consulting está inaugurando sua mais nova solução de tecnologia, o HVendas. Nesse novo produto, _insights_ de vendas serão apresentados a clientes de forma customizada e aperfeiçada às necessidades deles. A solução segue um simples fluxo de processamento:

1. O cliente envia sua base de dados de vendas para o HVendas
1. O cliente requisita uma análise específica de _insights_ de vendas
1. O analista de dados do HVoice desenvolve essa análise
1. O cliente recebe a base de dados agora customizada para essa análise

Neste cenário, você é o analista de dados em questão. 

Neste repositório você encontrará o arquivo `data.zip`, sendo este uma lista de arquivos `csv` compactados. Estes arquivos compõem a base de dados da OLIST disponibilizada na plataforma [Kaggle](https://www.kaggle.com/olistbr/brazilian-ecommerce). Cada arquivo `csv` possui informações específicas. Seu trabalho será de responder as requisições utilizando essa base de arquivos.

# Requisitos de Negócio

1. A não ser que especificado, todas as requisições devem ser respondidas utilizando a linguagem SQL em padrão ANSI
1. As requisições devem ser respondidas com clareza, tanto em relação ao código, quanto ao texto que as acompanha
1. Assuma que você não tem controle criativo do banco de dados, ou seja, não é permitida a criação de novas colunas nos arquivos originais.

# Requisitos Não-Funcionais

1. Embora o dataset tenha tamanho limitado, assuma que você está trabalhando com milhões de registros, escreva queries eficientes e evite processamento excessivo.
1. Assuma que o cliente utilizará os dados da forma como vieram, ou seja, não altere o conteúdo, nomes dos arquivos, e nomes das colunas.
1. Na HVAR, você trabalhará com inúmeras pessoas. Escreva suas queries de forma legível, contanto com boas práticas de utilização SQL.

# O Problema

Um dos clientes do HVendas fez algumas requisições de análises de dados. Seu trabalho é, conforme descrito acima, de _processar_ essas requisições e gerar as bases de dados requisitadas. Cada requisição deverá ser respondida com:

1. Um ou mais blocos de código com uma query SQL
1. Um ou mais arquivos `csv` contendo os resultado das queries
1. Uma análise em texto justificando aa queries e analisando os resultados. Sinta-se livre para incluir gráficos, medições, ou qualquer conteúdo extra que auxilie na análise.

**OBS:** A solução de uma requisição não é necessariamente uma única query, nem uma única base de dados (`csv`). Uma solução pode ser composta de vários desses conjuntos. Por isso, leia com atenção as requisições e garanta que todos os requisitos estão sendo atendidos em sua solução.

## Requisição 1

O cliente realizará em breve uma promoção no estado de São Paulo. Esta promoção será para compradores que utilizam boleto como forma de pagamento. Para maximizar a eficiência da campanha, o cliente gostaria de uma base que contenha os 10 produtos mais vendidos utilizando esta forma de pagamento. O cliente gostaria também de comparar as categorias de produtos em quantidade de vendas, da melhor categoria (mais vendas), à pior (menos vendas). O cliente pediu que apenas dados dos anos de 2018 e 2019 fossem utilizados.

## Requisição 2

O cliente gostaria de recompensar revendedores que apresentam alta performance na plataforma. Para isso, o cliente precisa saber os vendedores que fizeram mais vendas. Como forma de recompensação, o cliente oferecerá 20% de desconto para esses vendedores no frete de suas mercadorias da categoria mais vendida. Deixe claro na base de dados o valor original do frete, e o novo valor com desconto. O cliente também gostaria de saber quais as regiões que mais vendem produtos dessa categoria.

## Requisição 3

O cliente suspeita que produtos na categoria `brinquedos` estão com baixa de vendas por conta do frete. Para isso, o cliente gostaria de receber uma análise dividindo os produtos dessa categoria em quatro sub-categorias: 1) frete grátis; 2) frete abaixo de 10 reais; 3) frete abaixo de 20 reais; 4) frete superior a 20 reais. O cliente também precisa da quantidade de produtos vendidos em cada subcategoria, e da mediana de preços desses produtos.

### Requisição 4

O cliente gostaria de saber quais dos vendedores possuem melhor recepção em termos de avaliações. Para isso, o cliente criou a seguinte métrica: um vendedor pode ser avaliado utilizando um _coeficiente de aprovação_. Este coeficiente nada mais é do que uma média de avaliações de cada produto. Uma vez calculado o coeficiente de avaliação, o cliente gostaria de extrair a média deste coeficiente para o vendedor, e de categorizá-los da seguinte forma:

1. Coefieciente entre 4 e 5: Serviço bom
1. Coefieciente entre 3 e 4: Serviço regular
1. Coefieciente entre 1 e 2: Serviço ruim

**OBS:** As médias de coeficiente dos vendedores devem ser arredondadas para o valor mais próximo (para cima no caso de maior ou igual a .5, para baixo no caso de menor que .5).

# Entrega

O entregável deste desafio deverá ser o conjunto de queries, bases de dados e análises que atendam cada uma das requisições. Por favor entregue de forma legível e simples de compreender. A entrega pode ser feita diretamente com o e-mail com o qual você está em contato para o processo seletivo.

# Dicas

1. O [GoogleBigQuery](https://cloud.google.com/bigquery) é uma ótima ferramenta para importação dos dados e criação das queries SQL. Ele pode ser utilizado gratuitamente com [certas limitações](https://cloud.google.com/bigquery/pricing).
1. O [LaTeX](https://www.latex-project.org/) é uma excelente ferramenta para montar o relátorio, permitindo facilmente adicionar blocos de códigos legíveis para suas queries SQL, além de fácil criação de tabelas, imagens e afins para os relatórios.
