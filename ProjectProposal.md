# Project Proposal: World Cities Evaluation System
*WENTAO LI

*George Washington University, <unlimitediw@gwmail.gwu.edu>

### Abstract
* There are [4037 cities](https://brilliantmaps.com/4037-100000-person-cities/) with more than 100,000 population around the world from the largest cities such as [Shanghai](https://en.wikipedia.org/wiki/Shanghai), [Tokyo](https://en.wikipedia.org/wiki/Tokyo) and [New York City](https://en.wikipedia.org/wiki/New_York_City) to some small cities like [Boise](https://en.wikipedia.org/wiki/Boise,_Idaho) and [Thunder Bay](https://en.wikipedia.org/wiki/Thunder_Bay) and also from some well developed historic cities like [London](https://en.wikipedia.org/wiki/London) and [Istanbul](https://en.wikipedia.org/wiki/Istanbul) to some 'young' developing cities such as [Abidjan](https://en.wikipedia.org/wiki/Abidjan) and [Dar es Salaam](https://en.wikipedia.org/wiki/Dar_es_Salaam). Small city can grow to a large one and the young city also can be a well developed city in the future. It is believable that there are some correlation among these cities and in this project I want to find the relationship between the city development status and  ground truth features such as population, climate and Map image. Furthermore, I will predict the development trend of the city and generate the future hypothetical map image base on the previous data analysis and GAN technique. At the same time, I may try to find the places around the world map that have the possibility to become a livable city base on the prebuilt model and some geography and climate features.

### Introduction
When considering to evaluate a city, people always compare it with their familiar hometown and the world famous cities. However, it is not accurate sometime due to the lack of commonness among these cities and evaluating it without considering some implicit features such as city elevation map and metropolis area effect. What if we considering this evaluation problem with an overall database and good combination of machine learning methods?

In this project, I will try both kernel SVM and MLP method to process the numerical features such as population, longitude and latitude and category features such as climate like 'tropical wet' and 'Marine west coast' and generate the development level of the city. At the same time, I will use CNN model to find the commonness of the city map, elevation map, satellite map and so on. All of the SVM, MLP and CNN model will be a supervised or semisupervised learning model with label such as [GDP](https://en.wikipedia.org/wiki/Gross_domestic_product) level.

Furthermore, I will combine the city data in history timeline(by RNN or Markov model) and city category (by feature clustering or GDP level) to generate the future features and development level of this city. With this future prediction result, I will also try to generate the city map in the future by GAN technique. On the other hand, if have time, I will also try to extract some features such as geography and climate information from prebuilt model and do a world map searching with an evaluate function which aims to find the most livable places for human to build a new city.

More specifically, in the part of classification problem with numeric and category features input, soft SVM with kernel is able to linearly separable these cities but will be slow for training if use a large scale of dataset and the performance is not guaranteed base on the kernel function. To the MLP model, the process of model training is more implicit and may perform better if the dataset is large and sparse and it can also solve the non-linear separable problem. I will compare their performance in the experiment part later. In the part of map image processing, I select CNN since it has a high performance in image processing data with weight sharing and feature extraction. For instance, CNN can recognize the river or coast line no matter which direction and shape it is. In the part of city future trend prediction, RNN or Markov model is more applicable due to their good performance in future prediction base on previous state.

The following two section about future map generating and livable place searching is more productive and interesting. In the part of map generating, I will use a unsupervised learning algorithm [GAN](https://arxiv.org/pdf/1406.2661.pdf)(Generative adversarial network) and more specifically use the [Image to Image Translation with a conditional generative adversarial network](https://arxiv.org/pdf/1611.07004.pdf) and [cycle-consistent adversarial network](https://arxiv.org/pdf/1703.10593.pdf). This algorithm include two parts which one for generate fake image and one for discriminate the fake image from the real image and play a minmax game. In my model, I will first train the GAN model with data A,B where A has the real feature and real image while B has the real features and generate the fake image. If the model is trained successfully, I can use this model and the predicted features from RNN to generate the future map. May be we can have a view of the future world and it is believed work well especially in the developing country since it can take the developed country data as a template. 

The second section is about the livable spaces searching and it is more like an application of my evaluation model. I will first do a region evaluation to find the high value less human activity area likes plain and spilt these area into thousands of little square image with features of weather, elevation level and so on. After that, I will apply my feature adjusted combined evaluation model to these features and generate a list of evaluation values. The places with highest evaluation value may be taken into consideration to build a city.

### Steps and Timeline
* Project Proposal
  * Finished. Nov 19 2019
* Data Collection and Preprocessing
  * Some data resources are found, but still need the pure city map image dataset and an appropriate label dataset for cities.
  * Preprocess data that will be used by SVM, MLP and CNN directly including work of labeling, Feature scaling and special optimization base on selecting model.
  * Deadline: Nov 21 2019.
* Building Kernel Soft SVM model and MLP Model
  * Find an appropriate kernel and high value features for the SVM model and adjust the hyperparameters with experiment.
  * Find an appropriate layers and layer size for the MLP model and adjust it with experiment.
  * Evaluate a best model for numeric and category value in this project.
  * Deadline: Nov 22 2019
* Building CNN Model
  * Select an appropriate existing CNN model to train and test the city or global map dataset(small part).
  * Adjusting its inside layers and find the best performance model.
  * Deadline: Nov 25 2019
  
* Combining the SVM(or MLP) model and the CNN model to generate the new model for better city evaluation accuracy.
  * Test it with the test set spilt at the data preprocessing steps and print the score.
  * Deadline: Nov 26 2019
* (Optional) Building the RNN(or Markov) Model to Predict the Future Trend of City
* (Optional) Building the GAN Model
  * Using the geography image as X and city image as Z and taking evaluation value as parameter to train and test the model.
  * Using an empty geography image to build a city image.
  * Combining the future evaluation of a city, previous city image and existing geography image to build the future city image.
* (Optional) Finding the livable area for human
  * Reconstruct the city evaluation model with only nature feature such as geography and climate as features.
  * Evaluate the area around the world roughly and selecting the large areas with high value.
  * Spilt the large areas and evaluating the small areas again(may reconstruct the model again) and find the most livable places for human.
* Bias, Variance and Noise Analyzation
  * Using bagging or other methods to improve the performance.
  * Adding some specific layers to the GAN to improve the image performance.
  * Something else, unknown yet.
  * Deadline: Dec 1 2019
* Final Project Paper Writing
  * Deadline: Dec 5 2019
* Checking
  * Timeline may delay when facing hard problem.

### [Datasets and Reference](https://github.com/unlimitediw/MLFinalProject/blob/master/DataRef.md)
