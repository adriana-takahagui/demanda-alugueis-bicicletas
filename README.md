# Demanda de Aluguéis de Bicicleta 

## **Introdução do Problema** 

Qualquer empresa com fins lucrativos precisa traçar estratégias para aumentar a demanda de seu serviço. E a melhor forma de fazer isso é analisando os dados para uma tomada de decisão baseada em fatos e dados. E o case apresentado elucida como podemos fazer isso através da construção de um dashboard. 

**Problema**: Determinada cidade tem investido em ciclovias e a empresa em questão, que oferece serviço de aluguel de bicicletas e tem diversos pontos de aluguéis espalhados nesta cidade, possui como objetivo aumentar o número de bicicletas alugadas. 

**Objetivo do Dashboard**: Ajudar na compreensão do negócio extraindo informações relevantes e a despertar ideias e insights que contribuam na elaboração de estratégias para aumentar as vendas do serviço de aluguel de bicicletas desta empresa. 

**Dataset**: Dados foram extraídos do Kaggle: https://www.kaggle.com/code/hardikjain10/seoul-bike-rented/data

**Dicionário de Dados**: Abaixo segue uma descrição das variáveis utilizadas para a construção do dashboard.

➔ Date (data): Data <br>
➔ Rented Bike Count (aluguel): Contagem de bicicletas alugadas <br>
➔ Hour (hora): Horário do dia <br>
➔ Temperature(°C) (temperatura): Temperatura em ºC <br>
➔ Humidity(%) (umidade): Umidade em % <br>
➔ Wind speed (m/s) (vento): Velocidade do vento em m/s <br>
➔ Visibility (10m) (visibilidade): Visibilidade a cada 10m <br>
➔ Dew point temperature(°C) (temp_orvalho): Temperatura do ponto de orvalho em °C <br>
➔ Solar Radiation (MJ/m2) (radiacao_solar): Radiação Solar em MJ/m² <br>
➔ Rainfall (mm) (precipitacao_pluviometrica): Precipitação Pluviométrica em mm <br>
➔ Snowfall (cm) (neve): Queda de neve em cm <br>
➔ Seasons (estacao): Estação do ano <br>
➔ Holiday (feriado): Se o dia era um feriado <br>
➔ Functioning Day (dia_util): Se o dia era útil ou não <br>

**Para acessar e navegar pelo dashboard no Power BI**, clique [aqui](https://app.powerbi.com/view?r=eyJrIjoiZjVhNmJkZGUtZmJiNy00MTFlLWE0MDQtZDY5YjI1M2NlZDQxIiwidCI6IjgxMTFjMzgxLThjM2EtNDNkMS05ODc4LTA5ZjAzZGQ0N2Y1NiJ9) 

## **Desenvolvimento**

Um dos fatores que influencia a demanda de aluguéis de bicicleta é a condição climática. E o conjunto de dados analisado traz exatamente isso: quais eram as diversas condições climáticas (como temperatura, chuva, umidade, entre outros) em cada hora do dia e a quantidade de bicicletas alugadas em cada horário. 

Levando em consideração essa primeira análise, comecei a explorar os dados e suas diversas variáveis montando um primeiro relatório ("Análise de Demanda de Aluguéis de Bicicletas") e, assim, verificar o relacionamento entre as variáveis e a quantidade de aluguéis. Posteriormente, elaborei um "Simulador Financeiro" para auxiliar na análise de diversos cenários e na avaliação de possíveis respostas para determinados eventos. 

![Screenshot](dashboard01.png)
Figura 1

Na **Página Inicial** (Figura 1), podemos ver uma breve descrição do problema, o período de dados e a fonte de dados utilizada. 

![Screenshot](dashboard02.png)
Figura 2

Na **"Análise de Demanda de Aluguéis de Bicicletas"** (Figura 2), podemos analisar as diversas variáveis do conjunto de dados, como elas se relacionam com o volume de bicicletas alugadas e como influenciam o aumento ou não de aluguéis. 
1. No visual **"Qtde Aluguéis por estação, ano e mês"**, podemos constar que o maior volume de aluguéis ocorreu nos períodos mais quentes. Notamos também como os volumes são diferentes em cada estação, sendo portanto um grande indicativo de ser uma variável relevante para o volume de aluguéis. 
2. Em **"Qtde Aluguéis por período do dia e horário"**, o maior volume ocorreu no começo do dia e no final da tarde e à noite, sendo o horário outra variável importante para o aumento de aluguéis. 
3. Não vemos uma grande diferença em relação ao volume de aluguéis nos dias da semana em **"Qtde Aluguéis por dia da semana"**. 
4. E a maioria da quantidade de aluguéis ocorreram em dias que não eram **feriados**, mas isso não impede que alguma ação também seja realizada nos feriados. 

![Screenshot](dashboard03.png)
Figura 3

5. E no **tooltip** (dica de ferramenta) dos visuais **"Qtde Aluguéis por estação, ano e mês"** e **"Qtde Aluguéis por período do dia e horário"** (Figura 3) podemos acompanhar as médias de temperatura, umidade, chuva, etc.

![Screenshot](dashboard04.png)
Figura 4

6. Partindo para analisar as condições climáticas (Figura 4), resolvi criar faixas de valores para facilitar a análise da influência de cada situação no volume de aluguéis. A tabela mostra, portanto, como as diversas variáveis como as condições climáticas influenciam na demanda de aluguéis de bicicletas e como suas combinações podem trazer insights para elaborar estratégias que levem ao aumento da demanda do serviço.

![Screenshot](dashboard05.png)
Figura 5

7. E no tooltip da tabela (Figura 5), trago as informações referentes às faixas de valores apresentadas, assim como legenda das cores utilizadas. <br>
Todo o tratamento para definir as faixas de valores foi realizada no Power Query Editor. 

![Screenshot](dashboard06.png)
Figura 6

8. Podemos então combinar as variáveis de diversas maneiras e ordem para analisarmos quais os fatores que mais influenciam a quantidade de aluguéis de bicicletas, como, por exemplo, na imagem da Figura 6 vemos que as condições mais favoráveis são: temperatura média, umidade alta, chuva fraca e radiação baixa. 

![Screenshot](dashboard07.png)
Figura 7

No **Simulador Financeiro** (Figura 7), a ideia é possibilitar a análise "What If" (E se) simulando diversos cenários financeiros para extrair insights baseado em dados históricos. 

Para iniciar, adicione o valor cobrado por aluguel, o valor de manutenção por aluguel e o valor das outras despesas mensais. 
A partir daí, as possibilidades das simulações baseiam-se na alteração percentual da(o):
* Quantidade de aluguéis 
* Valor cobrado por aluguel 
* Manutenção por aluguel
* Outras despesas mensais 

E o resultado pode ser conferido na tabela logo abaixo, onde visualizamos as variações positivas ou negativas da simulação. 

![Screenshot](dashboard08.png)
Figura 8

**Exemplo de Simulação** (Figura 8): vamos supor que queiramos dar um desconto de 5% no valor cobrado no aluguel. Para suprir esse desconto, podemos vender mais, cortar despesas ou aumentar o custo de manutenção. 
Escolhendo vender mais, precisamos aumentar a quantidade de aluguéis em, no mínimo, 20% para começar a ter algum lucro. 

## **Conclusão e Insights**

Portanto, através do dashboard apresentado, conseguimos compreender quais condições são mais favoráveis para aumentar a demanda de aluguéis de bicicletas. E, de acordo com a análise realizada e os dados apresentados, seria no final da tarde e à noite, temperatura média e alta, umidade alta, chuva fraca, radiação baixa, e nas estações mais quentes como verão, primavera e outono. 
 
Além disso, é possível simular financeiramente diversos cenários. Por exemplo, para verificar se, diante de determinado desconto, quais ações podem ser tomadas para ter lucro com esse desconto, seja vender mais em quantidade de aluguéis ou cortar as despesas. Ou se tiver um aumento no custo da manutenção, quais são os possíveis cenários para mitigar esse aumento para o cliente? 

E diante de tais informações, é possível criar campanhas estratégicas, promoções, promoções relâmpagos. <br>
Criar diversos tipos de planos como: planos mensais ou plano família. <br>
Talvez promover eventos de saúde apresentando o benefício de andar de bicicleta, mesmo não tendo uma, mas alugando. 

Eu também recomendaria uma pesquisa de satisfação para colher dados a respeito dos aspectos positivos e negativos do serviço prestado.  
E assim elaborar diversas estratégias junto as áreas de negócio da empresa para montar planos de ações visando o objetivo de aumentar a quantidade de aluguéis de bicicletas. 

## **Próximos Passos**

Os próximos passos seriam criar um modelo de Machine Learning que ajude a prever a quantidade de aluguéis ao longo de um ano. Desta forma, preparar-se melhor para enfrentar os desafios do negócio. 
