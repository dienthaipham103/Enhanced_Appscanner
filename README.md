# Appscanner_voting
This code was implemented as part of the MAppGraph [1] paper. It is based on the implementation of Single Large Random Forest Classifier of AppScanner [2]. It is now available on https://github.com/Thijsvanede/AppScanner. But there are some more changes in the code to adapt with our project.

## Introduction
Appscanner is a method for mobile traffic classification based on flows. They define flows in a mobile traffic and use an Machine Learning model to classify flows among different apps. But for our approach - MAppGraph, we capture mobile traffic chunks in a specific duration of time (say 5 minutes) and classify them. To solve our problem by Appscanner method, we use voting scheme. Many flows are extracted from a mobile traffic chunk. After that,  the label of each flow is predicted by Appscanner method. Finally, the voting scheme is used to conclude the final label of the traffic chunk.

Moreover, our dataset is very large compared to the dataset in Appscanner project. So, we can build 16 different Machine Learning models. Each model is trained on a different dataset. Because a mobile traffic chunk is predicted by 16 models, so the voting scheme is also used here to get the final result.
