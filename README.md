# Neural_Network_Charity_Analysis

## Overview

This project worked with machine learning and neural networks. The goal of the project was to create a binary classifier that would train with data gathered on more than 30k organizations that have received funding from Alphabet soup, with this information the neural network will be trained and will be used to predict where Alphabet soup should make investments in the future.

## Results


* Data Preprocessing

  * What variable(s) are considered the target(s) for your model?
  
    The variable in the data set considered as a target was the "IS_SUCCESFUL', meaning that the money was used effectively, in this model we wanted to really get to the people that will get the most of the funding.
    
  * What variable(s) are considered to be the features for your model?
  
    The variables taken as features were the following, they were used because it could give to the model insight on the companies and should be considered:
  
      * APPLICATION_TYPE—Alphabet Soup application type
      * AFFILIATION—Affiliated sector of industry
      * CLASSIFICATION—Government organization classification
      * USE_CASE—Use case for funding
      * ORGANIZATION—Organization type
      * STATUS—Active status
      * INCOME_AMT—Income classification
      * SPECIAL_CONSIDERATIONS—Special consideration for application
      * ASK_AMT—Funding amount requested
      
      
![Screen Shot 2022-11-08 at 7 53 05](https://user-images.githubusercontent.com/104656920/200582601-aaa6eb06-6a38-4041-92e0-f36ebcc02e79.png)

  * What variable(s) are neither targets nor features, and should be removed from the input data?
    
    The following variables are just ID, therefore were not considered for the analysis:
    
      * EIN and NAME—Identification columns
  
  ![Screen Shot 2022-11-08 at 7 51 04](https://user-images.githubusercontent.com/104656920/200582441-e036969e-2b9a-424a-9915-0154a66bb040.png)

* Compiling, Training, and Evaluating the Model

  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
  
    I used the rule of having 3x the number of feauteres, when we use the encoder the number of fetures go up to 43, therefore the number of neurons I selected was 120 for the optimization. Layers, I selected 3 because is known to have the enough power to understand the relationship in the data. Activation function I tried using sigmoid and relu because the input values were always positive and I needed to create a binary classifier, which sigmoid activtion is pretty good at doing so.
    
  * Were you able to achieve the target model performance?
    
    It was not possible to get to the target performance that was above the 75%, with all the modifications made to the model I couldn´t
     get passed the threshold of 73% accuracy.
  * What steps did you take to try and increase model performance?
    
    First I eliminated columns, the ASK_AMT much of the companies that were funded had the similar amount given, so I thought maybe this was affecting the model, but it did not helped. Then I tried changing the number of neurons and adding a hidden layer, this didn´t helped to improve the model. Finally, I tried different configurations of activation functions which proved that not using the correct activation functions could make the model worse, therefore I decided to keep the Sigmoid and Relu.
    
    ### 1st attempt
    
    ![Screen Shot 2022-11-08 at 8 06 48](https://user-images.githubusercontent.com/104656920/200585852-b9e2907e-cffb-4d09-91cb-9d5c2879d656.png)

    ### 2nd attempt
    ![Screen Shot 2022-11-08 at 8 04 37](https://user-images.githubusercontent.com/104656920/200585345-a26d81d0-0750-4b7a-bc76-c06a6b396cc8.png)
    
    ### 3rd attempt
    ![Screen Shot 2022-11-08 at 8 04 12](https://user-images.githubusercontent.com/104656920/200585514-e3b5004e-b1ef-45bd-9edc-7a87379c7453.png)

## Summary

  Overall the neural network did a decent job, however, it was not as great as we could have expected. With this great amount of features if we wanted to run more epochs the time consumption is very high. In the first run It was used 50 epochs and it was nearly 15 min of waiting fot the model. Therefore there are other machine leraning techniques that could be faster and could be better for this data set. The one that comes to mind is Random Forest Classifier. This method in seconds brought an accuracy of 72.5%. Therefore we know that the data needs more preprocessing.
  
  <img width="705" alt="Screen Shot 2022-11-08 at 8 16 09" src="https://user-images.githubusercontent.com/104656920/200588190-41e19097-1de1-4f23-8239-a2babc4e807c.png">
