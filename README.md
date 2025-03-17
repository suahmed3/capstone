# Capstone Project - LNG Trading

**Capstone Project - LNG Trading** is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* I will be using two datasets in this project, one for the initial analysis, and the other for some secondary analysis to supplement the findings from the first dataset and test further hypoetheses to inform the business strategy.

The primary dataset is from the International Energy Agency (IEA) and shows monthly gas flow per million cubic metres from 31 participating countries, primarily covering Europe, as of February 2025. 

The secondary dataset is from the US Energy Information Administration (EIA), showing the montly prices of US LNG exports from 1997 to 2024. 


## Business Requirements
* The business is a new US-based investment fund that has been given a mandate to trade in energy and commodities. Due to the disruption in supply chains and changing nature of where fuels are sourced as a result of geopolitical events, the fund is interested in exploring liquified natural gas (LNG). 

It is particularly focused on trade flows between the US and Europe, and where opportunities may lie for US LNG exports. The traders at the fund need data analysis done in this field to examine the best opportunities for investment and viable strategies based on markets, time of year, and likelihood of future return.


## Hypothesis and how to validate?
My hypotheses are as follows:
* European Union countries have a higher demand for LNG during winter months
* LNG producers export less during their winter
* Prices for US LNG rise in line with demand
* The best time to invest is during late summer/early autumn as prices are still low but demand is set to rise rapidly

I will validate these hypotheses by analysing the data, creating visualisations, and checking if correlations exist, where relevant.

## Project Plan
* Outline the high-level steps taken for the analysis.

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
* Advances visualisations on Tableau
* Create and deploy dashboard on Streamlit

* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations
The business needs to know about LNG trade activites, with a focus on inflows to European countries and US LNG export prices, so visualisations need to show the prime months for European gas demand, the trends in terms of where these countries export to and import from, and the prices of US LNG at different points of the year historically. 

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?

There were no data privacy, bias, or fainess issues with the data, as it does not concern individuals, and is instead about LNG trading patterns and prices.

* How did you overcome any legal or societal issues?

There were no legal or societal issues to overcome as these data were publicly available and do not identify specific individuals or corporations.

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.

Dashboard on Tableau:
https://public.tableau.com/app/profile/saad.ahmed1183/viz/LNGTradeFlows/Dashboard1_1

This dashboard shows the trade flows of LNG in 2024 for 31 countries, primarily Europe, all covered under the IEA. It is currently set to show all the export destinations of gas exported from Germany, with the size of each box element showing the number of times LNG has flowed to each destination, and the colour denoting the absolute volume in million cubic metres, the darker the higher this is.

Additionally, there are two line graphs showing the prices of US LNG exports $ per million cubic feet, the first showing the values in 2023 and the second in 2024. Finally, there is a map showing the LNG imports for European Union countries in 2024, with the darkness of the shade showing higher imports in million cubic metres.

Dashboard on Google Python Flask Web App displays this same dashboard with the same capabilities, it can be found here: https://tableau-app-xyz.a.run.app/

The data insights are communicated to both technical and non-technical audiences through clearly displaying trends in a way that doesn't overwhelm people by including unnecessary information. For example, I didn't think it pertinent to include MAXFLOW or Borderpoint, and while I did include Flow Volume and Count of LNG Flow, these were not written on the dashboard elements so as not to confuse non-technical audiences. Instead, hovering on each element will give you additional information that is more precise, without the display compromising the meaning.

This need to communicate xomplex data insights to different audiences is also why I included line graphs with the prices of US LNG exports clearly displayed for each month in 2023 and 2024. I created two line graphs, 2023 on top and 2024 below, to simplify the display, with the bottom graph showing the months clearly, and having different Y axes to show more clearly that US LNG export prices had a different range of absolute values between the years, but that the broader trends in price fluctuation were roughly similar.


## Unfixed Bugs

One unfixed bug was my inability to create a Sankey diagram to be able to show LNG export Exit and Entry points, showing flow to different countries. I found a different and ultimately better alternative, through both the heatmap for 2024, which is customisable, and the map graph.

I recognised a few gaps in my knowledge, and consulted the internet, Chat GPT, and my own notes to be able to complete what was needed. It improved my understanding because I was able to reiterate some things that I had picked up but forgotten, and had a practical use case for them through this project, which will aid my memory.


## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. From the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.


## Main Data Analysis Libraries
* Pandas
* Numpy
* Matplotlib
* Plotly


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

Sourced dataset from here: https://www.iea.org/data-and-statistics/data-product/gas-trade-flows
Sourced second dataset from here: https://www.eia.gov/dnav/ng/hist/n9133us3m.htm
Used the Code Institute LMS for guidance on plotting the pie charts and line graphs: https://learn.codeinstitute.net/ci_program/daai_3
For guidance on creating a Sankey diagram: https://plotly.com/python/sankey-diagram/
Asked ChatGPT for help with the code: https://chatgpt.com/share/67d04a05-db50-8005-8c7a-b5a6f35bdc8b
For help to be able to visually compare US LNG export prices in 2023 and 2024: https://community.tableau.com/s/question/0D54T00000C5hf4SAB/multiple-series-on-line-graph


### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.
