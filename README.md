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
* Statistical tests to see link between US LNG prices and exports
* Advances visualisations on Tableau
* Create and deploy dashboard on Streamlit

* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations
The business needs to know about LNG trade activites, with a focus on outflows from the United States and in flows to European countries, so visualisations need to show the prime months for European gas demand, the typical times of year that US LNG flows start to rise, and, latterly, the prices of US LNG at different points of the year historically. 

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

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
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

Used the Code Institute LMS for guidance on plotting the pie charts and line graphs: https://learn.codeinstitute.net/ci_program/daai_3
For guidance on creating a Sankey diagram: https://plotly.com/python/sankey-diagram/


### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.
