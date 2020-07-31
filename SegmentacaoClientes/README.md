
# Campanha segmentada de clientes:

* Uma financeira pensando em lançar uma campanha mais direcionada para seus clientes, solicitou uma demanda ao departamento de marketing.
* Ao entender o cliente, os profissionais de propaganda podem lançar uma campanha adaptada às necessidades específicas. Neste caso a equipe quer lançar uma campanha de marketing dividindo seus clientes alvos em três grupos distintos.
* Visto que a companhia possui grande disponibilidade de dados sobre os clientes, a ideia do projeto consiste análisar e explorar esses dados na eminência de obter informações relaventes que permitam criar modelos de machine learning que possam ser aplicados para auxiliar na segmentação de marketing.

* Features projetadas a partir análise exploratória para quantificar o grau de de segmentação em cada grupo de clientes.

* Otimização com o método de Clustering k-means com objetivo particionar as observações 
dentre k grupos fazendo com que cada observação pertença ao grupo mais próximo da média.
* Para selecionar o melhor número de clusters utlizamos o método Elbow

* Por fim fizemos uma análise de componente principal para redução de dimensionalidade junto com método de redes neural Auto encoder para tentar obter uma melhor compactação das informações.


## Código e recursos utilizados 
**Versão Python:** 3.6
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, tensorflow, keras  


## Análise Exploratória
A análise exploratória foi feita no intuito de reconhecer como diferentes variáveis podem estar correlacionadas ou associadas uma à outra. Tais análises revelaram padrões importantes sobre comportamento de compras dos clientes.


## Criação do modelo 
Após realizar a transformação das variáveis categóricas, os dados foram divididos treino e teste conforme distribuição em 80% e 20%. As informações adquiridas durante a fase de exploração possibilitaram a utilização das técnicas não supervisionado de agrupamento e análise de componentes principais para uma melhor segmentação dos grupos.
