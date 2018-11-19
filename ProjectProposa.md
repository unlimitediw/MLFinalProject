# Map information processor

### PLAN A:
  * Collect city information and predict it's GDP, population.

### PLAN B:
  * Using city map photo to predict it's GDP, population

### PLAN C:
  * Using multi map informations to predict ...

### PLAN D:
  * Using GDP, Population and topographic information to generate map(GAN)
  
### PLAN E:
  * Predict value of a city base on the topographic information an find it's corresponding city
  * Predict the potential value of a city

### Explanation:
  * Map information is easy to get as a student and there is lots of implicit latent information inside of it.
  * In this project, I want to firstly analyze the numeric data to give a evaluation to the city with supervise learning. I may use the svm, Mlp and some other algorithm to construct this model. In the next step, I want to use image information with CNN to find some correlation and inside information of the map. After that, I want to combine many map images such as cartography and satellite map to generate more accurate result. After this, I want to use the inverse prediction to generate the map using GAN. At the end, with the data, I want to find the most high potential city in the world and some places have the potential to become a city around the world.
  
  
# Project Proposal: World Cities Evaluation System
@WENTAO LI

### Abstract
There are [4037 cities](https://brilliantmaps.com/4037-100000-person-cities/) with more than 100,000 population around the world from the largest cities such as [Shanghai](https://en.wikipedia.org/wiki/Shanghai), [Tokyo](https://en.wikipedia.org/wiki/Tokyo) and [New York City](https://en.wikipedia.org/wiki/New_York_City) to some unknown small cities like [Boise](https://en.wikipedia.org/wiki/Boise,_Idaho) and [Thunder Bay](https://en.wikipedia.org/wiki/Thunder_Bay) and also from some well developed historic cities like [London](https://en.wikipedia.org/wiki/London) and [Istanbul](https://en.wikipedia.org/wiki/Istanbul) to some 'young' developing cities such as [Abidjan](https://en.wikipedia.org/wiki/Abidjan) and [Dar es Salaam](https://en.wikipedia.org/wiki/Dar_es_Salaam). In this project, I want to find the relationship between the city development statu and it's ground truth features such as population, weather and Map image. Furthermore, I want to predict the development trend of the city and generate it's future hypothetical map image base on the previous data analysis and GAN technique. At the same time, I will try to find the places around the world map that have the possibilty to become a livable city base on the prebuild model and some geograhy and weather feature.

### Introduction
When considering to evaluate a city, people are easy to comapre it with their familiar hometown and the world famous cities. However, it is not accurate sometime due to the lack of commoness among these cities and evaluating it without consider some inside features such 
