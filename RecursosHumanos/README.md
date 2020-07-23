
# Indice de satisfação de colaborador:
* Análise para verificar o grau de satisfação de colaboradores para auxiliar o departamento de recursos humanos com ações de retenção e diminuição de custos com contração. Criação de modelo que permita prever a probabilidade de um colaborador deixar a empresa.
* Features projetadas a partir análise exploratória para quantificar o grau de satisfação dos colaboradores em relação a empresa 
* Otimização Random Forest utilizando GridsearchCV para atingir o melhor modelo. 


## Código e recursos utilizados 
**Versão Python:** 3.6
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, tensorflow  


## Análise Exploratória
Visualização das distribuições dos dados e os valores para as várias variáveis categóricas e contínuas. Algumas variáveis categóricas foram transformadas com valores numéricos com o auxilio do OneHotEncoder.


## Criação do modelo 
Após realizar a transformação das variáveis categóricas, os dados foram divididos treino e teste conforme distribuição em 80% e 20%.

Foram implementação de três modelos diferentes e avaliados utilizando métrica de matriz de confusão. 

Dentre os modelos utilizados estão:
**Regressão Logística**
**Random Forest**
**Deep Learning**