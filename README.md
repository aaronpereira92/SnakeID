# SnakeID - Ironhack Final Data Analytics Project

## Description
This repository contains two trained Convolutional Neural Networks (CNNs) which are able to identify two species of snakes- the Western diamondback rattlesnake and DeKay's brown snake. 

**Note**: I plan to include another three species of snake into the classification task at a a latter date. 

## Contents 
Here are the folders and their respective files:

- #### Scripts and Notebooks folder:

1. `_scripts_and_notebooks/1_building_testing_CNN_notebook.ipynb`: notebook to preprocess image data, build the CNNs, and evaluation.

2. `_scripts_and_notebooks/2_snakeID_function_notebook.ipynb`: to develop the final function which uses trained CNN to analyze new images. 

3. `_scripts_and_notebooks/3_main_snakeID.ipynb`: This jupyter notebook was used to demonstrate that the function works

4. `_scripts_and_notebooks/main_snakeID.py`: The final .py script that contains the function to be run in order to analyze new images. 


- #### functions folder:

1. `_functions/functions.py `: This contains the function **SnakeID** which needs to be imported in order to to analyze new images.  

  Just import by running this :
  ```python
  from functions import snakeID
  ``` 

  To use the function you need to pass arguments:
  ```python
  snakeID(model_name, weights, directory, no_images = 1)
  ``` 
  Where:
   `model_name` is the filename(with extension) of the model to be entered as a string within quotes'', 
   `weights` is the filename of the model's weights to be entered as strings, 
   `directory` is the filepath of to the **subfolder** of images to be analyzed to be entered as strings, 
   no_images  is the number of images to be analyzed entered as integer. 



- #### CNN models and weights folder:
1. `_cnn_models_and_weights/model_first_try.json` : first CNN that I trained which got a validation accuarcy of about 0.83.
2. `_cnn_models_and_weights/model_second_try.json`: second CNN that I trained which got a validation accuracy of about 0.90 
3. `_cnn_models_and_weights/first_try_weights.h5`: the weights of the first CNN 
4. `_cnn_models_and_weights/second_try_weights.h5`: weights of the second CNN. 
Note: For more information on how to load them please refer to the notebook `_scripts_and_notebooks/1_building_testing_CNN_notebook.ipynb`

- #### Other Images folder:
1. `_images/snake_id.jpg`: This is just an image file of the plot output of the validation analysis, which shows the results of idenification. The plots of images which have a green border were correctly predicted, where as red border is wrong.

- #### Snake Image data:
1. `_snakes_american_data/read_first.txt`: Just a text file containing the link to the image dataset and which snake classes were used.


## Database

- Got the images from the following link:
https://www.kaggle.com/datasets/sameeharahman/preprocessed-snake-images

## Project Presentation
For the google slides presentation please click on the following link:

https://docs.google.com/presentation/d/1MfyzNY2Sk8ZAZ4uEMxidvSpVP5Pd-5SAvDGExghZOeo/edit?usp=sharing

## SnakeID output

![alt text](https://github.com/aaronpereira92/SnakeID/blob/fdd590e0055d544ba6b6eb85462005fac3f1af6a/_images/snake_id.jpg)
