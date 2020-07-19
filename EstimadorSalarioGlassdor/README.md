# Estimador de Salarios em Data Science:
* Modelo para estimar salários na área de ciência de dados para auxiliar os candidatos negociar seus ganhos quando conseguirem um novo emprego.
* Scrapping de 1000 vagas de trabalho do glassdoor utilizando python selenium
* Features projetadas a partir do texto de cada cargo para quantificar o valor que as empresas empregam em habilidades como python, excel, aws e spark 
 * Otimização Regressão Linear, Lasso e Random Forest utilizando GridsearchCV para alcancar o melhor modelo. 
* Construção de uma interface com api flask 

## Código e recursos utilizados 
**Versão Python:** 3.7  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, selenium, flask, json, pickle  
**Scraper Github:** https://github.com/arapfaik/scraping-glassdoor-selenium  
**Artigo:** https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905  
**Flask:** https://towardsdatascience.com/productionize-a-machine-learning-model-with-flask-and-heroku-8201260503d2


## Web Scraping
Tweaked the web scraper github repo (above) to scrape 1000 job postings from glassdoor.com. With each job, we got the following:
Ajuste do script web scraper do github (acima) obter 1000 postagens de trabalho do glassdoor.com. A cada etapa, extraímos as seguintes features:
*	Titulo da Vaga
*	Estimativa_Salarial
*	Descricao_Vaga
*	Avaliacao
*	Nome_Companhia
*	Localizacao
*	Tamanho
*	Fundamento
*	Tipo_Propriedade
*	Industria
*	Setor
*	Receita
*	Concorrencia


## Limpeza dos dados
Após o scrap, foi preciso limpar os dados para que ficassem utilizáveis em o nosso modelo. Fiz as seguintes alterações e criei as seguintes variáveis

*	Made columns for employer provided salary and hourly wages
*	Criação de colunas de salário hora 
*	Remoção de linhas que não continham salário 
*	Criação de nova coluna para informar o estado da companhia 
*	Conversão de data inauguração da companhia em idade da companhia 
*	Made columns for if different skills were listed in the job description:
*	Criada colunas para representar diferentes habilidades que foram listadas na descrição da vaga como:
    * Python  
    * R  
    * Excel  
    * AWS  
    * Spark 


## Análise Exploratória
Visualização dasdistribuições dos dados e os valores para as várias variáveis categóricas. Abaixo estão alguns destaques das tabelas dinâmicas. 


## Criação do modelo 
Primeiramente foi transformado variáveis categóricas em variáveis dummy. Também foi dividido os dados em treinamento e teste distribuido em 80% e 20% respectivamente.

Foram implementados três modelos diferentes e avaliados utilizando o erro absoluto médio. Foi escolhido essa métrica pela sua facilidade em interpretar e os outliers não interferirem muito para esses tipos de modelo.   

Dentreo os modelos estão:
*	**Multiple Linear Regression** – Baseline para o modelo
*	**Lasso Regression** - Devido ao fato dos dados das muitas variáveis ​​categóricas serem esparsos, pensei que uma regressão normalizada como o laço seria eficaz
*	**Random Forest** – Novamente, com a escassez associada aos dados, pensei que seria um bom ajuste. 

## Performance do modelo
O modelo Random Forest superou em muito as outras abordagens nos conjuntos de teste e validação. 
*	**Random Forest** : MAE = 11.22
*	**Linear Regression**: MAE = 18.86
*	**Ridge Regression**: MAE = 19.67

## Produção
Nesta etapa, foi criado um endpoint com API do flask hospedado em um servidor da web local. A API recebe uma solicitação com uma lista de valores de uma lista de vagas de trabalho e retorna um salário estimado.
 



