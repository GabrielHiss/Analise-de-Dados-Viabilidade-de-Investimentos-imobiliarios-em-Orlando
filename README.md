Apresentação completa do caso em: https://medium.com/@gabriel.hiss 

<b> Importando os dados </b> 🎲

Os dados foram obtidos pela [Datascy](https://www.datascy.com/) e estão disponíveis no meu [GitHub](https://github.com/GabrielHiss/Analise-de-Dados-Viabilidade-de-Investimentos-imobiliarios-em-Orlando/blob/main/OrlandoAirbnbRentalDataAnalytics-%20Sem%20tratamento.xlsx).

<b> Limpeza dos Dados via Excel - Preparação do Dados </b> 👩‍💻

Como a Database foi disponibilizada em .xlsx (Excel) utilizou-se recursos de limpeza por este softaware como a fórmula TRIM, os filtros da aba de Dados e outros.

Posteriormente foram realziados alguns cálculos com fórmulas mais básicas SUM, MEAN e outras e principalmente a criação de gráfico para análises.

<b> Análise Econômica </b> 📚

<b> Etapa 1: </b> Cálculo do lucro mensal e anual dos imóveis disponíveis em mercado como da própia agência obtidos estão na planilha dispónivel no [Github](https://github.com/GabrielHiss/Analise-de-Dados-Viabilidade-de-Investimentos-imobiliarios-em-Orlando/blob/main/Revenue_Orlando.xlsx)

<b> Etapa 2: </b> Uso do SQL para saber a média de preços por quantidade de quartos, foi criada uma planilha separada como base: [Planilha base de média de preços](https://github.com/GabrielHiss/Analise-de-Dados-Viabilidade-de-Investimentos-imobiliarios-em-Orlando/blob/main/Airbnb_Orlando_Market_MyRental.xlsx)  

-Código SQL utilizado para análise de imóveis da agência no [DataWorld](https://data.world/)- 

SELECT avg(price_per_night), bedrooms

FROM airbnb_listings_orlando_myrenta

Where bedrooms >= 2 and bedrooms <= 5 

group by bedrooms

-Código SQL utilizado para análise de imóveis do mercado no [DataWorld](https://data.world/)- 

SELECT avg(price_per_night), bedrooms

FROM airbnb_listings_orlando_market

Where bedrooms >= 2 and bedrooms <= 5 

group by bedrooms

<b> Etapa 3: </b> Para descobrirmos se o projeto irá se pagar no horizonte de planejamento do projeto (60 anos) e qual será o lucro, podemos realizar uma distribuição de fluxo de caixa. Para um cenário normal temos a planilha de [análise econômica](https://github.com/GabrielHiss/Analise-de-Dados-Viabilidade-de-Investimentos-imobiliarios-em-Orlando/blob/main/Suporte%20do%20Trabalho%20Final.xlsx) e para o cenário com queda de 20% do lucro temos uma segunda planilha de [análise econômica](https://github.com/GabrielHiss/Analise-de-Dados-Viabilidade-de-Investimentos-imobiliarios-em-Orlando/blob/main/Suporte%20do%20Trabalho%20Final%20-%2020%25.xlsx).

<b> Conclusões </b>

As tratativas permitiram a análsie de viabilidade do investimento. As quebras em diversas foram devido a quantidade de dados (deixando o carregamento lento) e para organização do raciocínio por ser um trabalho de várias etapas e condições de cenários.
