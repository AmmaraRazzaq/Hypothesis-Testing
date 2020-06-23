# Hypothesis Testing

Study the effect of recession on mean housing prices in university towns and non-university towns. Are the mean housing prices in university towns affected by recession? Are the mean housing prices in university towns and non-university towns affected the same way by recession? 

Two hypothesis tests will be performed. First hypothesis test will test the effect of recession on mean housing prices in university towns. The effect will be studied by comparing mean housing prices of the quarter before recession started to the recession bottom. Second hypothesis test will test the effect of recession on university towns vs non-university towns in terms of price ratio. (`price_ratio=quarter_before_recession/recession_bottom`)

To test the hypothesis, we have to assume a null hypothesis.

**Hypothesis1** There is an effect of recession on mean housing prices in university towns. 

**Null Hypothesis** There is no effect of recession on mean housing prices in university towns.

**Hypothesis2** Effect of recession on university towns and non-university towns is different. 

**Null Hypothesis** There is no difference between university towns and non-university towns in terms of effect of recession on mean housing prices.

## Data Resources

* From the [Zillow research data site](http://www.zillow.com/research/data/) there is housing data for the United States. In particular the datafile for [all homes at a city level](http://files.zillowstatic.com/research/public/City/City_Zhvi_AllHomes.csv), ```City_Zhvi_AllHomes.csv```, has median home sale prices at a fine grained level.

* From the Wikipedia page on college towns is a list of [university towns in the United States](https://en.wikipedia.org/wiki/List_of_college_towns#College_towns_in_the_United_States) which has been copy and pasted into the file ```university_towns.txt```.

* From Bureau of Economic Analysis, US Department of Commerce, the [GDP over time](http://www.bea.gov/national/index.htm#gdp) of the United States in current dollars (use the chained value in 2009 dollars), in quarterly intervals, in the file ```gdplev.xls```. For this project, only GDP data from the first quarter of 2000 onward is considered.

## Terminologies
* A _university town_ is a city which has a high percentage of university students compared to the total population of the city.
* A _recession_ is defined as starting with two consecutive quarters of GDP decline, and ending with two consecutive quarters of GDP growth.
* A _recession bottom_ is the quarter within a recession which had the lowest GDP.

# Methodology

We are running hypothesis test to see the effect of recession on housing prices in university towns and non-university towns. To implement the hypothesis testing, following steps will be followed.
<ol>
    <li>The prices of houses in housing data are given on yearly basis. This data needs to be converted to quarters because recession is measured on quartelry basis.
    <li>Next we need to find recession start and recession bottom. A recession starts with two consecutive quarters of GDP decline and ends with two consecutive quarters of GDP rise. A recession bottom is the quarter with lowest GDP during recession period. To find the recession period, GDP data from Bureau of Economic Analysis, US Department of Commerce is used.
    <li>The houses in the housing data need to be separated into two categories; university towns and non-university towns and to do this a list of university towns is used.
    <li>Once the housing data is converted to quarters and we know the effect of recession on the housing prices in terms of price ratio we will divide the housing data into university towns and non-university towns to run hypothesis test on these two groups. The hypothesis test will show if the recession has affected the university towns and non-university towns in the same way. 
