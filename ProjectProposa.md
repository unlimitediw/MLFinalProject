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
* There are [4037 cities](https://brilliantmaps.com/4037-100000-person-cities/) with more than 100,000 population around the world from the largest cities such as [Shanghai](https://en.wikipedia.org/wiki/Shanghai), [Tokyo](https://en.wikipedia.org/wiki/Tokyo) and [New York City](https://en.wikipedia.org/wiki/New_York_City) to some unknown small cities like [Boise](https://en.wikipedia.org/wiki/Boise,_Idaho) and [Thunder Bay](https://en.wikipedia.org/wiki/Thunder_Bay) and also from some well developed historic cities like [London](https://en.wikipedia.org/wiki/London) and [Istanbul](https://en.wikipedia.org/wiki/Istanbul) to some 'young' developing cities such as [Abidjan](https://en.wikipedia.org/wiki/Abidjan) and [Dar es Salaam](https://en.wikipedia.org/wiki/Dar_es_Salaam). Samll city can grow to a large one and the young city also can be a well developed city in the future. It is believable that there are some correlation among these cities and in this project I want to find the relationship between the city development statu and it's ground truth features such as population, climate and Map image. Furthermore, I will predict the development trend of the city and generate it's future hypothetical map image base on the previous data analysis and GAN technique. At the same time, I may try to find the places around the world map that have the possibilty to become a livable city base on the prebuilt model and some geograhy and climate features.

### Introduction
<p>When considering to evaluate a city, people always comapre it with their familiar hometown and the world famous cities. However, it is not accurate sometime due to the lack of commonness among these cities and evaluating it without considering some implicit features such as city elevation map and metropolitian area effect. What if we condiering this evaluation problem with an overall database and well combination of machine learning methods?
<p>In this project, I will try both kernel SVM and MLP method to process the numerical features such as population, longitude and latitude and classification features such as climate like 'tropical wet' and 'Marine west coast' and generate the development level of the city. At the same time, I will use CNN model to find the commonness of the city map, elevation map, satellite map and so on. All of the SVM, MLP and CNN model will be a supervised or semisupervised learning model with label such as [GDP](https://en.wikipedia.org/wiki/Gross_domestic_product).
<p>Furthermore, I will combine the city data in history timeline and city classification (by feature clustering of GDP level) to generate the future features and development level of this city. With this future prediction result, I will also try to generate the city map in the future by GAN technique.
<p>In this project, I will try both kernel SVM and MLP method to process the numerical features such as population, longitude and latitude and classification features such as climate like 'tropical wet' and 'Marine west coast' and generate the development level of the city. At the same time, I will use CNN model to find the commonness of the city map, elevation map, satellite map and so on. All of the SVM, MLP and CNN model will be a supervised or semisupervised learning model
<p>including thousands of cities' map, climate and resource feature and so on and a cobination of machine learning method such as SVM and MLP dealing with numeric and classification value and CNN dealing with map image data while using evaluation result and GAN to generate future development trend and map?

