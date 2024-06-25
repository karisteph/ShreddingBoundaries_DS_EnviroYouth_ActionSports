# Shredding Boundaries: Data-Driven Solutions for Environmental Stewardship and Youth Empowerment through Action Sports
## Introduction
Polluted air and water heavily impact surfers and skateboarders alike.

In NYC, long-term exposure to PM2.5, the deadliest urban air pollutant, causes 1 in 25 deaths!<sup>1</sup>

Rockaway Beach suffers 188% more flooding than the city average<sup>2</sup> , exposing the peninsula to fecal bacteria like Enterococci commonly found in floodwater<sup>3</sup> and eventually the ocean.

This project presents an analysis of past environmental data in areas of NYC where surfing and skateboarding are prevalent. The data was reviewed and processed for stakeholders Brujas and the Laru Beya Collective to ultimately provide recommendations on how they can maximize the impact of sustainable initiatives all while promoting cross-disciplinary cooperation and community cohesion.

<sup>1</sup>[Real-Time Air Quality: P](https://a816-dohbesp.nyc.gov/IndicatorPublic/data-features/realtime-air-quality/#:~:text=Long%2Dterm%20exposure%20to%20PM2,department%2C%20and%20other%20health%20threats.) by Environment and Health Data Portal, <sup>2</sup>[New Data Tool Shows Rockaway](https://www.rockawave.com/articles/new-data-tool-shows-rockaway-suffers-from-more-flooding-than-citywide-average/) by The Wave, <sup>3</sup>[Microbiological Assessment of Tap Water](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7068305/) by National Library of Medicine


![image](https://github.com/karisteph/ShreddingBoundaries_DS_EnviroYouth_ActionSports/assets/157851606/93e95914-a263-43c7-a025-bf054968a34d)
Photo by Corey Wilson on [surfline.com](https://www.surfline.com/surf-news/the-surfskate-connection/34930)

![image](https://github.com/karisteph/ShreddingBoundaries_DS_EnviroYouth_ActionSports/assets/157851606/af8a6265-c3cf-41a0-87d7-f74904af47ed)

Photo by Anton Nilsson on [familytraveller.com](https://familytraveller.com/usa/vacation-destinations/asia/sky-brown-olympic-skateboarder/)


## Business Problem
The Laru Beya Collective and Brujas are looking to merge the waves of surf culture with the streets of skateboarding, uniting their communities under a singular banner of action sports and environmental stewardship. They tasked me with looking into New York City's Beach Water Samples dataset and the city's Air Quality dataset. The company wants to know:

What areas of the city put skateboarders most at risk to environmental hazards?

What areas of the beach put surfers most at risk to environmental hazards?

How can we use the insights from the project to organically foster cross-disciplinary cooperation and community cohesion?

How can we use our platform to amplify outreach and make a tangible impact on both environmental conservation and social empowerment within communities?

## Data and Resources Used
(![image](https://github.com/karisteph/ShreddingBoundaries_DS_EnviroYouth_ActionSports/assets/157851606/8e55a13b-9210-4dcc-8d37-4adb0478d2d0)

The two datasets used throughout this project are provided by the Department of Health and Mental Hygiene accessed through the New York City Open Data website. That includes:

Beach Water Samples dataset from 2005 to 2023

Enterococci bacteria measurements from the beach water samples collected

Air Quality dataset from 2008 to 2022

Measurements for air pollutant, fine particles (PM 2.5), for each tested area of the city

## Methods
We address our business problem by employing data science techniques, beginning with data cleaning.
- The initial Beach Water Sample data exploration included:26,999 records and 6 columns
- The Laru Beya Collective is interested in the last three years of the beach water samples dataset in order to address the areas where the Entercocci bacteria is still the most present
- The youth organization is only interested in regions that concern Rockaway beach because that is the only surfable beach in all five boroughs of the city
  
- The initial Air Quality data exploration included:18,025 records and 12 columns
- Brujas is interested in the last three years of the air quality dataset in order to address the areas where the pollutants are still the most present
- The youth organization is interested in data from all five boroughs of the city
- The youth organziation wanted to target the most hazardouse air pollutant which is PM 2.5

After cleaning the data I generated the master dataset and conducted an analysis using Python.

Limitations: 
Any skepticism in the data is mainly due to the lack of year round sample collection.
Also important to note that the Air Quality dataset provided data only up until 2022.

Further exploration of the data led to the application of more advanced modeling techniques starting from a Shift(1) baseline model, to a SES first simple model, and finally the ARIMA/SARIMA model as the final model.  

Model Progression (Beach Water Samples):
- Shift (1) baseline model
- SES first simple model
- ARIMA final model

![image](https://github.com/karisteph/ShreddingBoundaries_DS_EnviroYouth_ActionSports/assets/157851606/efd0c413-86d9-4fea-b9c6-7c5b4e50c566)


Model Progression (Air Quality):
- Shift (1) baseline model
- SES first simple model
- SARIMA final model

![image](https://github.com/karisteph/ShreddingBoundaries_DS_EnviroYouth_ActionSports/assets/157851606/639aa23e-c763-4b94-b830-dab04a3bc5fe)


## Data Analysis Results

Beach Water Samples: 
- The highest concentrations of Enterococci bacteria are found in ROCKAWAY BEACH 9TH - 13TH in the July 28 2023 sample intake
- The second highest concentrations of Enterococci bacteria are found in ROCKAWAY BEACH 15TH - 22TH in the July 28 2023 sample intake
- The third highest concentrations of Enterococci bacteria in 2023 are found in ROCKAWAY BEACH 23RD - 59TH in the September 7 2023 sample intake
- 9th street to 59th street put surfers the most at risk because those areas had the highest levels of Enterococci bacteria in all of Rockaway Beach in 2023
- Enterococci bacteria levels in the beach water exhibit a seasonal pattern.
- The levels tend to increase during the summer months, peaking in July and August, and decrease during the winter months.
- This pattern suggests a correlation between higher bacteria levels and warmer weather, which could be due to factors such as increased
  beach attendance or environmental conditions favorable for bacteria growth.

Air Quality:
- The highest concentrations of PM 2.5 are all found in the Manhattan borough

- Midtown and Chelsea put skateboarders the most at risk because those areas had the highest levels of PM 2.5 in all of NYC in 2022

- Winter yielded higher concentrations of PM 2.5 than summer samples

## Recommendations

1. Brujas: Consider using your social media platform to enlighten the community of the environmental dangers posed to urban skateboarders. A color coded map that highlights the areas with the highest concentrations of PM 2.5 could make it easier for people to engage with the content.
  
2. Laru Beya: Organize beach clean ups in targeted areas of the beach and the time of the year when they are the most polluted.

3. Brujas + Laru Beya: Host a surf skate workshop with the goal of empowerment through knowledge. Environmental component:Frame air and water quality information as a tool for personal empowerment rather than a set of rules. Explain how air pollution and water contamination affects the body during intense physical activities especially for surfers and skateboarders who are in those environments for long periods of time. Highlight how understanding air and water quality can help them make informed decisions about when and where to skate and/or surf to maximize their performance and reduce the risk of discomfort or health issues. Action sports component: surfers teach skaters how to surf and skaters teach surfers how to skate. Swap skills, make new connections, strengthen the community. 

4. Laru Beya + Brujas: Forge dynamic partnerships outsisde the surf/skate community: Brujas partner with NY Restoration Project (tree planting organization) and host tree planting events, Laru Beya partner with local schools/organizations near the most affected areas of the beach and offer educational talks regarding the project's findings. The goal? Equip the youth with knowledge so they can enhance their urban resilience to climate change.

## Future Investigations

- Conduct a comprehensive assessment and impact analysis of each youth organization (Brujas + Laru Beya). Track the project's effectiveness by monitoring key indicators such as youth engagement, environmental actions, community partnerships, and participant feedback. Use these insights to refine strategies and drive continuous improvement.

- Develop an advanced model that integrates the project’s environmental data with the organization’s assessment and impact analysis. This model will deeply explore and enhance the critical connections between action sports, environmental stewardship, and youth empowerment, solidifying and amplifying their mutual impact.

- As surf and skate organizations that frequently travel, consider expanding this project to other cities. I can adapt the project to suit regional environmental conditions and community needs. Conducting thorough analysis of your next destination will yield valuable data and foster new partnerships with environmental advocates, surf, and skate communities worldwide.

## For More Information

Please review the full analysis in the jupyter notebook [ShreddingBoundaries_DS_EnviroYouth_ActionSports](https://github.com/karisteph/ShreddingBoundaries_DS_EnviroYouth_ActionSports/blob/main/ShreddingBoundaries_DS_EnviroYouth_ActionSports.ipynb)

Refer to the [Presentation](https://www.canva.com/design/DAGI3kww6GY/g1BcNCC9PspndSiHOoOfug/edit?utm_content=DAGI3kww6GY&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

## Contributor

[Karina Baculima](https://github.com/karisteph)

## Repository Structure

|— README.md                                                 <- The top-level README for reviewers of this project
|— ShreddingBoundaries_DS_EnviroYouth_ActionSports_Repo.pdf  <- PDF version of repository
|— ShreddingBoundaries_DS_EnviroYouth_ActionSports_Presentation.pdf <- PDF version of project presentation
|— ShreddingBoundaries_DS_EnviroYouth_ActionSports.ipynb     <- Interactive computing environment including analysis in Jupyter                                                                            notebook
|—                                                           <- PDF version of jupyter notebook
|— .gitignore                                                <- Exclude listed files
|— Data                                                      <- Beach Water Samples dataset and Air Quality dataset


