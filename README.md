
# PROJETO INTEGRADOR II - IMOBILIÁRIA PROPERATI

O objetivo do Projeto é criar modelos de Regressão Linear que possam ser utilizados a fim de estimar o preço por metro quadrado em dólar de propriedades utilizando o conjunto de dados da imobiliária Properati.


## Autores
Andreia Bacic - [@andreiabac](https://github.com/andreiabac)
Alex Pivato - [@aleeexp](https://github.com/aleeexp)
Guilherme A. C. Butzke - [@guilherme-atomo](https://github.com/guilherme-atomo)
Lucas Gentile - [@gentile95](https://github.com/gentile95)

## Descrição

   1 - FEATURES DA BASE DE DADOS
   As variáveis categóricas bairro e tipo de propriedade foram convertidas em variáveis fictícias utilizando o método get_dummy para permitir escrever modelos de regressão linear com o grupo das variáveis selecionadas.
    - preço em dólar (price_usd);
    - preço por metro quadrado (price_m2);
    - média de preço por metro quadrado (avg_price_m2);
    - tamanho da propriedade (total_m2);
    - distância em metros até o ponto do Obelisco (dist_obelisk);
    - tipo de propriedade apartamento (type_apartment);
    - tipo de propriedade casa (type_house);
    - tipo de propriedade loja (type_store);
    - bairro Caballito (type_Caballito);
    - bairro Caballito (type_Caballito);
    - bairro Palermo (type_Palermo.

   2 - DADOS.
        Os dados foram filtrados a fim de reduzir o tamanho do conjunto de dados. A seleção foi feita baseada nos bairros que possuem a maior quantidade de propriedades, como parâmetro selecionamos os bairros com mais de 900 propriedades. Os bairros filtrados foram os seguintes:
            - Caballito com 1299 propriedades;
            - Belgrano com 1264 propriedades;
            - Palermo com 1231 propriedades;
        O conjunto de dados reduziu de 14860 para 3794 registros.
        
   3 - VARIÁVEL PREDITORA
        A variável de predição (target) dos modelos utilizada é price_m2.
        
   4 - Análise dos Dados
       A correlação entre todas as variáveis, incluindo as variáveis dummys, observamos que a correlação entre o preço da propriedade (price_usd) e tamanho da propriedade (total_m2) é a mais forte.
        A correlação entre preco_m2 e total_m2 não é significativa comparada com as demais.
        

   5 - MODELOS TREINADOS
        Foram testados os seguintes modelos de regressão linear:
            - Regressão Linear Simples.
            - Regressão Linear Múltipla.
            - Regressão Ridge.
            - Regressão Lasso.
            - Regressão Gradiente Descendente.
            - Regressão Polinomial.


## Conclusões
   O enunciado sugere previsão de preços por m2, porém encontramos melhores resultados usando preço total em dólar como variável target;
   Acontece que o preço total em dólar tem uma alta correlação com o total de metros quadrados. Isso implica em uma relação linear entre essas duas features;
   Houveram tentativas de enriquecer o dataset com algumas features para melhorar o resultado na predição de preço por m2. Foram comparados alguns modelos de regressão diferentes também. Em todos os modelos obteve-se melhor resultado com o target sendo o preço total em dólares;
   Para uma melhor predição do preço por m2, o dataset poderia fornecer informações melhores correlacionadas com o preço por m2, exemplo, área verde da propriedade, nível de acabamento, quantidade de cômodos, quantidade de suítes, quantidade de banheiros, possui piscina, quantidade de garagens e uma série de outras features que fariam a diferença nesse sentido;
   Sendo assim, a sugestão para um melhor resultado para esse modelo é usar o preço total em dólares como variável target.
