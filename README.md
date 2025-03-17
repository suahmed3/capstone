# Capstone Project - LNG Trading

**Capstone Project - LNG Trading** is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content

I will be using two datasets in this project, one for the initial analysis, and the other for some secondary analysis to supplement the findings from the first dataset and test further hypoetheses to inform the business strategy.

The primary dataset is from the International Energy Agency (IEA) and shows monthly gas flow per million cubic metres from 31 participating countries, primarily covering Europe, as of February 2025. 

The secondary dataset is from the US Energy Information Administration (EIA), showing the montly prices of US LNG exports from 1997 to 2024. 


## Business Requirements

The business is a new US-based investment fund that has been given a mandate to trade in energy and commodities. Due to the disruption in supply chains and changing nature of where fuels are sourced as a result of geopolitical events, the fund is interested in exploring liquified natural gas (LNG). 

It is particularly focused on trade flows to and within Europe. The traders at the fund need data analysis done in this field to examine the best opportunities for investment and viable strategies based on markets, time of year, and likelihood of future return.


## Hypothesis and how to validate?

My hypotheses are as follows:

* European Union countries have a higher demand for LNG during winter months
* LNG producers export less during their winter
* Prices for US LNG rise in line with demand
* The best time to invest is during late summer/early autumn as prices are still low but demand is set to rise rapidly

I will validate these hypotheses by analysing the data, creating visualisations, and checking if correlations exist, where relevant.

## Project Plan

These are the steps to be taken for this analysis:
* Import both datasets
* Check attributes of LNG trade flow dataset
* Clean the LNG trade flow dataset
* Basic visualisation for the dataset
* Advanced visualisation for the dataset
* Run statistical tests
* Check attributes of US LNG export prices dataset
* Clean it
* Basic visualisations
* Advanced visualisations on Tableau
* Tableau dashboard

The two datasets I used were from the IEA and the EIA. The IEA dataset for LNG import and export patterns was collected on a monthly basis, going back to October 2008. The EIA dataset of US LNG export prices was collected on a monthly basis also, since January 1997 with some exceptions (the second half of 1997, and all of 1998, 1999, and the year 2000).

I sourced the datasets from these websites and imported them into VS Code to read, clean, analyse, and process them. I focused on 2023 and 2024 values when it came to visualisation to provide a manageable reference point for the business and to show the most recent data available. It was important to cover more than one year, to show annual trends, and compare whether monthly fluctuations roughly hold stable in different periods.

For processing, I go into futher detail later on in this document, but it focused around checking null values, renaming variables for ease of analysis, and excluding variables that were not relevant to the business case for Tableau and the dashboard, while still keeping it elsewhere if needed for deeper future analysis.

I created line graphs to visualise gas imports and exports in the EU in 2024, LNG imports into the UK in 2024, and a pie chart showing share of total gas exports by country in the countries in the European gas network. 

I also created line graphs to show US LNG export prices in 2023 and 2024, in Tableau. I made a heatmap to show LNG export destinations and volumes in 2024, and a geographical map to show LNG imports into the EU in 2023.

I used these research methodologies to compare trends in the LNG trade across the European gas network and of prices for US LNG exports. These metholodologies helped me to address the hypotheses in line with the business case.


* Visusalisations

Here are links to my visualisations:

Total Gas Imports by Country 2024 - https://github.com/suahmed3/capstone/blob/1d302185402b3dcb1b7c69d0b408fea67561babd/Total%20Gas%20Imports%20by%20Country%202024.png

Total Gas Exported from EU 2024 - https://github.com/suahmed3/capstone/blob/b1d0ab09b87139f6b3acbddee54939e8c29c29e9/Total%20Gas%20Exported%20from%20EU%202024.png

Total LNG Imported by EU 2024 - https://github.com/suahmed3/capstone/blob/b1d0ab09b87139f6b3acbddee54939e8c29c29e9/Total%20LNG%20imported%20to%20EU%202024%20line%20graph.png

UK LNG Imports 2024 - https://github.com/suahmed3/capstone/blob/b1d0ab09b87139f6b3acbddee54939e8c29c29e9/UK%20LNG%20imports%202024.png

US LNG Export Prices 2023 - https://github.com/suahmed3/capstone/blob/b1d0ab09b87139f6b3acbddee54939e8c29c29e9/US%20LNG%20export%20prices%202023.png

US LNG Export Prices 2024 - https://github.com/suahmed3/capstone/blob/b1d0ab09b87139f6b3acbddee54939e8c29c29e9/US%20LNG%20export%20prices%202024.png

The others can be seen on the Tableau dashboard.


## The rationale to map the business requirements to the Data Visualisations

The business needs to know about LNG trade activites, with a focus on inflows to European countries and US LNG export prices, so visualisations need to show the prime months for European gas demand, the trends in terms of where these countries export to and import from, and the prices of US LNG at different points of the year historically. 

## Analysis techniques used

I used trend analysis for the prices of US LNG exports, displaying the results for both 2023 and 2024 in a dashboard. I also used trend analysis and comparative analysis for LNG imports into EU countries in 2023 and both import and export destinations and levels between 31 mostly European countries in the European gas network in 2024, with a focus on Germany.

The limitations were that I didn't use predictive analysis or trend forecasting. This is an alternative approach I could've taken, I could have actually used 2023's data to test predictive models to see if they accurately predicted 2024's trends in German export flows, LNG import demand in the EU, and US LNG export prices.

In terms of structuring my data, there were a number of steps I needed to take. In the ETL stage, I checked the first dataset, the IEA LNG exports, got its description, info, and whether it contained null values.

I then had to reshape the data to be able to use it in Tableau, which involved melting columns with names such as Jun-24 and Jan-23 into a date-time format, creating the value 'Month'. I then kept only the variables relevant to the analysis, which were Month, Exit, Entry, and the also newly named Flow Volume which was previously bundled under each month. I included Borderpoint too, but decided to exclude this from analysis in Tableau as I considered it redundant and could be needlessly confusing for non-experts if included within a dashboard.

The data limited me somewhat, as there were some unnamed export destinations, simply marketed as Liquefied Natural Gas, which weren't caught in the initial ETL, so I had to exclude them within Tableau. Luckily, there were very few of these, so it didn't tamper with the overall conclusions or implications of the dataset, the trends held firm.

I also did not have figures for US LNG imports through the data I used, as the United States is not one of the participating countries in this dataset, which was primarily focused on the European natural gas network. The only dataset from the same source which showed gas flows between all OECD countries did not break down these statistics by month, instead only showing the annual amounts, which is not sufficient for a more focused analysis and the business case.

I used generative AI - namely ChatGPT - to help me fix code pertaining to reshaping the dataset for use in Tableau, and for tips on creating a Sankey diagram. 

## Ethical considerations

There were no data privacy, bias, or fairness issues with the data, as it does not concern individuals, and is instead about LNG trading patterns and prices. It could be argued that there were some biases in that despite some of the countries in the European gas network also importing LNG from countries outside of the same network, this was not recorded in the dataset. 


There were no legal or societal issues to overcome as these data were publicly available and do not identify specific individuals or corporations.

## Dashboard Design

Dashboard on Tableau:
https://public.tableau.com/app/profile/saad.ahmed1183/viz/LNGTradeFlows/Dashboard1_1

This dashboard shows the trade flows of LNG in 2024 for 31 countries, primarily Europe, all covered under the IEA. It is currently set to show all the export destinations of gas exported from Germany, with the size of each box element showing the number of times LNG has flowed to each destination, and the colour denoting the absolute volume in million cubic metres, the darker the higher this is.

Additionally, there are two line graphs showing the prices of US LNG exports $ per million cubic feet, the first showing the values in 2023 and the second in 2024. Finally, there is a map showing the LNG imports for European Union countries in 2024, with the darkness of the shade showing higher imports in million cubic metres.

The data insights are communicated to both technical and non-technical audiences through clearly displaying trends in a way that doesn't overwhelm people by including unnecessary information. For example, I didn't think it pertinent to include MAXFLOW or Borderpoint, and while I did include Flow Volume and Count of LNG Flow, these were not written on the dashboard elements so as not to confuse non-technical audiences. Instead, hovering on each element will give you additional information that is more precise, without the display compromising the meaning.

This need to communicate xomplex data insights to different audiences is also why I included line graphs with the prices of US LNG exports clearly displayed for each month in 2023 and 2024. I created two line graphs, 2023 on top and 2024 below, to simplify the display, with the bottom graph showing the months clearly, and having different Y axes to show more clearly that US LNG export prices had a different range of absolute values between the years, but that the broader trends in price fluctuation were roughly similar.

## Conclusions

Through my analysis, I found these results for the following hypotheses:

* European Union countries have a higher demand for LNG during winter months

This was validated as correct for both 2023 and 2024.

* LNG producers export less during their winter 

This was validated - while the European countries focused on had higher exports in December, the absolute volume exported was much lower than the winter months.

* Prices for US LNG rise in line with demand

This cannot be accurately discerned from the existing data, it would require an additional dataset. However, what we can see is that US LNG export prices were at their highest in January in both 2023 and 2024, and experienced rises towards the end of year, in Autumn and Winter. 

* The best time to invest is during summer as prices are still low but demand is set to rise rapidly

This would require additional analysis to prove, but in the patterns of prices, we can see that they hold relatively steady for most of the year, and noticeable dips tend to begin in June or July, before starting to rise again from September. In both 2023 and 2024, prices have been at their lowest in August, which suggests this hypothesis may be correct.

## Unfixed Bugs

One unfixed bug was my inability to create a Sankey diagram to be able to show LNG export Exit and Entry points, showing flow to different countries. I found a different and ultimately better alternative, through both the heatmap for 2024, which is customisable, and the map graph.

I recognised a few gaps in my knowledge, and consulted the internet, Chat GPT, and my own notes to be able to complete what was needed. It improved my understanding because I was able to reiterate some things that I had picked up but forgotten, and had a practical use case for them through this project, which will aid my memory.


## Development Roadmap

I faced some challenges with Tableau initially but it was because the data wasn't properly formatted for easy usability within Tableau. The stratgies I used were research, finding resources on Google and also asking Chat GPT.

Another was my inability to figure out how to plot both 2023 and 2024's US LNG export prices line graphs on the same chart, though this was mitigated by placing them one above and one below, and keeping the months visible on the chart below, for easier comparison.

I plan to learn predictive analysis for the next project, as well as learning to better pre-preparing data for use in Tableau as part of the initial ETL process. I will also ensure that initial visualisations have graph axes that start from zero.


## Main Data Analysis Libraries
* Pandas
* Numpy
* Matplotlib
* Plotly


## Credits 

Sourced dataset from here: https://www.iea.org/data-and-statistics/data-product/gas-trade-flows

Sourced second dataset from here: https://www.eia.gov/dnav/ng/hist/n9133us3m.htm

Used the Code Institute LMS for guidance on plotting the pie charts and line graphs: https://learn.codeinstitute.net/ci_program/daai_3

For guidance on creating a Sankey diagram: https://plotly.com/python/sankey-diagram/

Asked ChatGPT for help with the code: https://chatgpt.com/share/67d04a05-db50-8005-8c7a-b5a6f35bdc8b

For help to be able to visually compare US LNG export prices in 2023 and 2024: https://community.tableau.com/s/question/0D54T00000C5hf4SAB/multiple-series-on-line-graph

