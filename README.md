# Google Data Analytics Capstone: CO2 Emission Case Study
Course: [Google Data Analytics Capstone: Complete a Case Study](https://www.coursera.org/learn/google-data-analytics-capstone)
## Introduction
[Ask](https://github.com/chrissy049/Capstone/blob/main/README.md#ask), [Prepare](https://github.com/chrissy049/Capstone/blob/main/README.md#prepare), [Process](https://github.com/chrissy049/Capstone/blob/main/README.md#process), [Analyze](https://github.com/chrissy049/Capstone/blob/main/README.md#analyze-and-share), [Share](https://github.com/chrissy049/Capstone/blob/main/README.md#analyze-and-share), and [Act](https://github.com/chrissy049/Capstone/blob/main/README.md#act).
### Quick links:
Data Source: [climatewatchdata.org](https://www.climatewatchdata.org/ghg-emissions?end_year=2020&regions=TOP&start_year=2005) [accessed on 09/09/23]  
Imported Data: [CVS file](https://github.com/chrissy049/Capstone/blob/main/ghg-emissions%20(1).csv)
Data Visualizations: [R](https://github.com/chrissy049/Capstone/blob/main/Visualizations.html)  
## Background
### CO2 Emissions
Carbon dioxide (CO2) emissions are a significant contributor to global climate change and the ongoing crisis of rising temperatures. These emissions primarily result from the burning of fossil fuels such as coal, oil, and natural gas for energy production, transportation, and industrial processes. As CO2 accumulates in the atmosphere, it acts as a greenhouse gas, trapping heat and leading to rising temperatures. This temperature increase causes a domino of adverse effects, including more frequent and severe weather events, rising sea levels, disrupted ecosystems, and threats to human health. To combat the devastating impacts of CO2 emissions, countries and communities worldwide must transition to cleaner energy sources, enhance energy efficiency, promote sustainable transportation, and implement policies aimed at reducing emissions. 

### Scenario
A policymaker in the United States wants to propose a plan to inform other policymakers from different countries about global climate change. They need information tracking CO2 emissions from countries emitting significant amounts of CO2 in the atmosphere. The policymaker has a colleague who is a data analyst in the oil industry and has asked them to create an analysis on CO2 emissions based on countries starting in 2005. Furthermore, the analysis will be sent to multiple policymakers and ignite a dialogue to collectively make an impact.

## Ask
### Business Task
Evaluate the CO2 emissions since 2005 and formulate a prediction of what CO2 emissions will be like in the next five years.
### Analysis Questions
Questions that will guide the future environmental program:  
1. How likely will the top emitting countries continue to decline their CO2 emissions?
2. What is the impact, good or bad, of minimizing CO2 emissions?


## Prepare
### Data Source
Imported Data: [CVS file](https://github.com/chrissy049/Capstone/blob/main/ghg-emissions%20(1).csv)
The data will be sourced from climatewatchdata.org to analyze and identify trends from 2005 to 2020 which can be downloaded from [climatewatchdata.org](https://www.climatewatchdata.org/ghg-emissions?end_year=2020&regions=TOP&start_year=2005). The data has been made available by Climate Watch under this [license](https://www.climatewatchdata.org/about/permissions). This public and open data is used to gather insights on national and global progress on climate change for policymaking, research, media, and more. 

### Data Organization
On climatewatchdata website, there are multiple filters one can apply to produce a particular dataset. It can show data on a high-level and in-depth scale, factor in multiple data sources, specify certain gaseous chemicals, and more. The basic filters used for this analysis are data: collected only from Climate Watch, included top emitting countries, and time ranged from 2005 to 2020. 

## Process
RStudio is used to process and visualize the dataset. The raw data given was manageable enough to be done on a spreadsheet however, I wanted to track and present the steps taken to create this case study. RStudio allows users to share in-line code and executed code in a single file which makes R an efficient tool to use here.


Observations:  
1. The Year column was set as a char data type. Using mutate(), I changed the data type into double.

2. The dataset contained a couple of N/A rows displaying ClimateWatch as a Country and N/A values. Using the filter() function, I was able to remove those rows.

### Data Cleaning
1. All the rows having irrelevant naming conventions are adjusted. For example, the region the European Union had was labeled "European Union (27)",  so I removed the "(27)" from its name.
2. Columns "iso" and "unit" were removed before it became unless data.
3. The raw data was not tidy because each row did not capture a single observation. Instead each row listed data for each year for a country making it a wide table. I used the gather() function to make sure each row was a single observation for its respective year, now making it a long table.
  
## Analyze and Share
Data Visualization: [R](https://github.com/chrissy049/Capstone/blob/main/Visualizations.html)  
The data is stored appropriately and is now prepared for analysis.

![CO2 Emission Graph](https://github.com/chrissy049/Capstone/assets/136738354/ba815f54-6777-4b2a-b2cc-2a488d7ff9b7)
  
## Act
After creating data visualizations and identifying the trends in each region and the overall trend, CO2 emissions have minimally decreased in the long run with the exception of China and India as they have significantly increased their CO2 emissions. It can be predicted that the following regions will strive to decline their CO2 emissions: the United States and the European Union. The other countries have remained consistent since 2005. 
Initiatives to help bring down CO2 emission would be transition into renewable energy sources. Change doesn't happen overnight so the slightest swap can create a domino effect into other environmental changes. Education also plays an important role in reducing CO2 emissions. It is not only up to the policymakers to make change. It is up to the people, from an environmental perspective, to understand the impact their country is making and reflect on their own role in the world. 
