# ResNet for bird classification

## Problem description
I competed in the class's Kaggle competition for bird classification https://www.kaggle.com/competitions/birds23sp/overview. In general, the competition is to find the most accurate model to predict a bird's species from an image of it. For my project, I added constraints. My goal was to find the best ResNet Model structure for predicting a birds species after training the pre-trained model for one epoch. In addition, to try to get a higher score for the competition, I trained resnet18 for more epochs and submitted its predictions. 

## Previous work
I used the class's Transfer Learning to Birds tutorial - https://colab.research.google.com/drive/1kHo8VT-onDxbtS3FM77VImG35h_K_Lav?usp=sharing#scrollTo=ciUXCJ5LvN1p.
All the models I used were ResNets with different model structures loaded pre-trained using pytorch - https://pytorch.org/hub/pytorch_vision_resnet/.

## My approach
First, I loaded the Kaggle dataset into Google CoLab by downloading the dataset then uploading it as my own dataset. I loaded it into CoLab using the Kaggle API. I then used the code from the class's Transfer Learning to Birds tutorial with some minor changes to get the pytorch DataLoaders from the dataset. Again, mostly using the code from the tutorial, I trained each resnet18, resnet34, resnet50, resnet101, resnet152 for one epoch and saved their states in checkpoints in my Google Drive. I then used Matplotlib to plot the losses over the one epoch for each model against each other. For resnet18, I also trained it for 8 epochs and had it predict on the test data for submission to the competition. 

## Datasets
The dataset I used was the dataset given by the Kaggle competition - https://www.kaggle.com/competitions/birds23sp/data.

## Results

## Discussion


My project's experiments were not as extensive as I would have liked them to be. I would have liked to train each ResNet model structure for more epochs and predict using those models and experiment with other pre-trained models other than ResNet. However, I started my project trying to create my own model on attu. I had a working model (was not very accurate ~1% test accuracy) but attu ran into issues (I think space issues). All of my main python that defined my model and had all of the code that I used to pre-process the data to be usable in the way I was using the model (included resizing all of the images to 256x256 and 64x64) was deleted. I also completely lost access to attu, so I pivoted to this new project. Because of this late start, I didn't have enough time to train the amount of models and for the amount of epochs I wanted to. 
