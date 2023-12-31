### Project Description:

Investigation on the relationship between raw materials’ price and electricity price

Electricity prices are generally determined by several factors, largely the cost of power generation, and transmission. The cost of generation is highly correlated with the price of the raw materials. In the United States, the fuels for power generation mainly comes from natural gas and coal. They together account for more than half of the power generation source.

Fuel prices may increase during periods of high electricity demand and when there are fuel supply constraints or disruptions because of extreme weather events and accidental damage to transportation and delivery infrastructure. We assume higher fuel prices, in turn, will result in higher costs to generate electricity. Therefore, our topic is to estimate the correlation between natural gas prices, coal prices and electricity prices of different states in the United States from year 2011 to 2021.

We accessed our yearly data via the open data on EIA. Firstly, we plotted the average electricity price, coal price and natural gas price yearly changes. As we can see from our plots, The average price of electricity is generally on a rise from year 2011 to 2021. However, the average price for natural gas and coal, to the contrary of our initial assumptions, varied a lot over the years.
To better understand this situation, we used text processing to analyze the news from google news. With all the recent news relevant to the US electricity market and coal and natural gas price, using sentimental analysis we found that score of polarity became negative in recent months, which means words like ‘bad’, and ‘worse’ appeared more often. This can be an indicator for a ‘worse’ situation in electricity, coal and natural gas price, which typically means a surge in price.
 

Last, we designed an econometrics model using fixed effect model to quantify the relationship between electricity price and natural gas and coal price. The model comes as follow:

Electricity Priceit= α + βNatural Gas Priceit + δCoal Priceit  + ci + λt + εit

t = 1,2,3…T    i = 1,2,3…N
ci , λt are fixed effects. ci is state fixed effect, λt is time fixed effect.
εit is the error term.

The result for this model reads as follow: 

           Parameter  Std. Err.     T-stat    P-value    Lower CI    Upper CI
coal_price    -0.0023     0.0053    -0.4405     0.6608     -0.0129      0.0083
ng_price       0.1901     0.2582     0.7363     0.4638     -0.3244      0.7047

As we can see that the P value for both parameters are above 0.5, which indicates that coal price and natural gas price do not have a significant influence on the electricity price. The omitted variable bias is the reason that we get this result:
Factors other than the raw material prices that also determine the electricity price were not considered in this model. For example, power plant costs (financing, construction, maintenance, and operating costs), transmission and distribution system cost, and also regulations on the price. Without including those factors in the model, it is not valid to explain the changes in electricity solely based on the change in its raw material prices.
