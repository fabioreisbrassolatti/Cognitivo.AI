a. Como foi a definição da sua estratégia de modelagem?

Resposta: Minha estratégia de modelagem respeitou o seguinte processo:

1-) Análise da base de dados em sí
2-) Análise descritiva das variáveis disponíveis
3-) Criação e análise de variáveis relacionadas a vizinhança, anúncios e usuários.
4-) Preparação da ABT
5-) Rodada e análise dos seguintes modelos de regressão: MQO, Ridge, Lasso, Random Forest e Gradient Boosting
6-) Seleção do melhor modelo
7-) Avaliação dos modelos na base teste
8-) Conclusão sobre a modelagem

O ETL, juntamente com a documentação e conceituação das variáveis foi feito no software Knime. De posse da ABT utilizei a stack Python/Jupyter/Github para modelagem e análise dos dados. Para simplicidade de software, clareza e agilidade na gestão do dado, preferi usar cada ferramenta para o que ela tem de melhor.

O modelo tem parte das variáveis atreladas ao usuário e parte a vizinhança. Estou confortável com a abordagem, pois na Econometria Clássica, Carter Hill, o Preço é variável dada, a demanda se ajusta àquele nível de preço. Acredito que este modelo sirva como uma ferramenta de recomendação para maximização de receita. Tendo parte do modelo atrelada a características do usuário e a vizinhança, conseguimos “determiniar” locais com maiores demanda, portanto permitem preços maiores, e usuários mais engajados e que aumentando a demanda no site com hospedagens altamente disponíveis podem ser melhores remunerados, aumentando o engajamento da oferta, a liquidez no site e a geração de receita. Além de facilitar imensamente a criação de modelos de machine Learning, pois tudo foi projetado para se retroalimentar com pouca intervenção humana. 

Link com o projeto de etl e conceituação das variáveis: https://drive.google.com/drive/folders/1Q46Zn6w9NQbvebq1jRuWZ5ApX5L1gZEY?usp=sharing

b. Como foi definida a função de custo utilizada?
Resposta: Dentro da Lib SKLearn é usada função de maximização do R².

c. Qual foi o critério utilizado na seleção do modelo final?
Resposta: Por não dispor de um engenheiro de software,fiz manualmente a seleção. Esta seleção foi baseada no R² e análise dos scores das bases de treino e teste de todos os 5 modelos de regressão testados, que foram: OLS, Ridge, Lasso, Random Forest e Gradient Boosting.

d. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?
Resposta: Minha literatura recomenda não utilizar backtest como ferramenta de pesquisa,Lopez de Prado 2018 pg 151. Por isso a escolha do método foi a de pontuação no score na base teste.

e. Quais evidências você possui de que seu modelo é suficientemente bom?
Resposta: Preço usualmente é a uma variável dada. O mercado se ajustará a determinado preço, principalmente numa plataforma onde a oferta de similares é farta. Acredito que este modelo é usado como uma sugestão da ferramenta, que do modo como foi criada, possibilita alguns tipos de maximização  de receita e engajamento. Duas variáveis muito importantes para sites como o AirBnB.