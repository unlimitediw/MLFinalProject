# Project Proposal: World Cities Evaluation System
*WENTAO LI

*George Washington University, <unlimitediw@gwmail.gwu.edu>

### Abstract
There are [4037 cities](https://brilliantmaps.com/4037-100000-person-cities/) with more than 100,000 population around the world from the largest cities such as [Shanghai](https://en.wikipedia.org/wiki/Shanghai), [Tokyo](https://en.wikipedia.org/wiki/Tokyo) and [New York City](https://en.wikipedia.org/wiki/New_York_City) to some small cities like [Boise](https://en.wikipedia.org/wiki/Boise,_Idaho) and [Thunder Bay](https://en.wikipedia.org/wiki/Thunder_Bay) and also from some well developed historic cities like [London](https://en.wikipedia.org/wiki/London) and [Istanbul](https://en.wikipedia.org/wiki/Istanbul) to some 'young' developing cities such as [Abidjan](https://en.wikipedia.org/wiki/Abidjan) and [Dar es Salaam](https://en.wikipedia.org/wiki/Dar_es_Salaam). Small city can grow to a large one and the young city also can be a well developed city in the future. It is believable that there are some correlation among these cities and in this project I want to find the relationship between the city development status and  ground truth features such as population, climate and Map image. Furthermore, I will predict the development trend of the city and generate the future hypothetical map image base on the previous data analysis and GAN technique. At the same time, I may try to find the places around the world map that have the possibility to become a livable city base on the prebuilt model and some geography and climate features.

### Introduction
When considering to evaluate a city, people always compare it with their familiar hometown and the world famous cities. However, it is not accurate sometime due to the lack of commonness among these cities and evaluating it without considering some implicit features such as city elevation map and metropolis area effect. What if we considering this evaluation problem with an overall database and good combination of machine learning methods?

In this project, I will try both kernel SVM and MLP method to process the numerical features such as population, longitude and latitude and category features such as climate like 'tropical wet' and 'Marine west coast' and generate the development level of the city. At the same time, I will use CNN model to find the commonness of the city map, elevation map, satellite map and so on. All of the SVM, MLP and CNN model will be a supervised or semisupervised learning model with label such as [GDP](https://en.wikipedia.org/wiki/Gross_domestic_product) level.

Furthermore, I will combine the city data in history timeline(by RNN or Markov model) and city category (by feature clustering or GDP level) to generate the future features and development level of this city. With this future prediction result, I will also try to generate the city map in the future by GAN technique. On the other hand, if have time, I will also try to extract some features such as geography and climate information from prebuilt model and do a world map searching with an evaluate function which aims to find the most livable place for human to build a new city.

More specifically, in the part of classification problem with numeric and category features input, soft SVM with kernel is able to linearly separate these cities but it will be slow for training if use a large scale of dataset and the performance is not guaranteed base on the kernel function. To the MLP model, the process of model training is more implicit and may perform better if the dataset is large and sparse and it can also solve the non-linear separable problem. I will compare their performance in the experiment part later. In the part of map image processing, I select CNN method since it has a high performance in image data processing with weight sharing and feature extraction. For instance, CNN can recognize the river or coast line no matter which direction and shape it is. In the part of city future trend prediction, RNN or Markov model is more applicable due to their good performance in future prediction base on previous states.

The following two section about future map generating and livable place searching is more productive and interesting. In the part of map generating, I will use a unsupervised learning algorithm [GAN](https://arxiv.org/pdf/1406.2661.pdf)(Generative adversarial network) and more specifically use the [Image to Image Translation with a conditional generative adversarial network](https://arxiv.org/pdf/1611.07004.pdf) and [cycle-consistent adversarial network](https://arxiv.org/pdf/1703.10593.pdf). GAN algorithm includes two parts which one for generating fake image and one for discriminating the fake image from the real image and play a minmax game. In my model, I will first train the GAN model with data A,B that A has the real feature and real image while B has the real features and generates the fake image. If the model is trained successfully, I can use this model and the predicted features from RNN to generate the future map. May be we can have a view of the future world and it will work well especially in the developing countries since it can takes the developed countries data as a template. 

The second section is about the livable spaces searching and it is more like an application of my evaluation model. I will first do a region evaluation to find the high value and low human activity areas like plain and spilt these area into thousands of little square images with features of weather, elevation map and so on. After that, I will apply these features to my evaluation model and generate a list of hypo values. The places with highest value may be taken into consideration to build a city.

### [Steps and Timeline(link)](https://github.com/unlimitediw/MLFinalProject/blob/master/Timeline.md) 
* Project Proposal(2019/11/19).
* Data Collection and Preprocessing(2019/11/21).
* Building Kernel Soft SVM model and MLP Model(2019/11/22).
* Building CNN Model(2019/11/25).
* Combining the SVM(or MLP) model and the CNN model to generate the new model for better city evaluation accuracy(2019/11/26).
* Bias, Variance and Noise Analysis(2019/12/01).
* Final Project Paper Writing(2019/12/05).
* (Optional)Building the RNN(or Markov) Model to Predict the Future Trend of City.
* Building the GAN Model.
* Finding the livable area for human.

### [Datasets and Reference(link)](https://github.com/unlimitediw/MLFinalProject/blob/master/DataRef.md)
