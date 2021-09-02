# Appscanner_voting
This code was implemented as part of the MAppGraph [1] paper. It is based on the implementation of Single Large Random Forest Classifier of AppScanner [2]. It is now available on https://github.com/Thijsvanede/AppScanner. But there are some more changes in the code to adapt with our project.

## Introduction
Appscanner is a method for mobile traffic classification based on flows. They define flows in a mobile traffic and use an Machine Learning model to classify flows among different apps. But for our approach - MAppGraph, we capture mobile traffic chunks in a specific duration of time (say 5 minutes) and classify them. To solve our problem by Appscanner method, we use voting scheme. Many flows are extracted from a mobile traffic chunk. After that,  the label of each flow is predicted by Appscanner method. Finally, the voting scheme is used to conclude the final label of the traffic chunk.

Moreover, our dataset is very large compared to the dataset in Appscanner project. So, we can build 16 different Machine Learning models. Each model is trained on a different dataset. Because a mobile traffic chunk is predicted by 16 models, so the voting scheme is also used here to get the final result.

## Dataset
For training, there are 16 small datasets. For each small dataset, there are 101 mobile traffic chunks of 101 apps. The duration of one mobile traffic chunk is 50 minutes. With this dataset, we can train 16 different models. The training datset is saved in folder appscanner_models.

For testing, there is a dataset including mobile traffic chunks (in 5 minutes) of 101 apps. Each app has about 100-300 traffic chunks to test. The testing dataset is saved in folder test. 
