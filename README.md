# SnakeID - Ironhack Final Data Analytics Project

## Description
This repository contains two trained Convolutional Neural Networks (CNNs) which are able to identify two species of snakes- the Western diamondback rattlesnake and DeKay's brown snake. 

**Note**: I plan to include another three species of snake into the classification task at a a latter date. 

## Contents 
Here are the folders and their respective files:

1. Scripts and Notebooks folder `_scripts_and_notebooks`:

This folder contains the jupyter notebooks that I used to build the CNNs and preprocess data and a final .py file.

- `_scripts_and_notebooks/1_building_testing_CNN_notebook.ipynb`: This jupyter notebook was used to preprocess image data and build the CNNs, as well as to evaluate them.

- `_scripts_and_notebooks/2_snakeID_function_notebook.ipynb`: This jupyter notebook was used to develop the final function which will be used to call the trained CNN and analyze new images. 

- `_scripts_and_notebooks/3_main_snakeID.ipynb`: This jupyter notebook was used to demonstrate that the function works

- `_scripts_and_notebooks/main_snakeID.py`: The final .py script that contains the function to be run in order to analyze new images. 

2. Functions folder  `_functions`:
- `_functions/functions.py `: This contains the function **SnakeID** which needs to be imported in order to to run the `main_snakeID.py` for analysing new images. Just import by running this :
```python
from functions import snakeID
``` 
To use the function you need to pass arguments:
```python
snakeID(model_name, weights, directory, no_images = 1)
``` 
Where
 `model_name` is the filename(with extension) of the model to be entered as a string within quotes'', `weights` is the filename of the model's weights to be entered as strings, `directory` is the filepath of to the **subfolder** of images to be analyzed to be entered as strings, and no_images  is the number of images to be analyzed entered as integer. 



3. CNN models and weights folder `_cnn_models_and_weights`:
- `_cnn_models_and_weights/model_first_try.json` : first CNN that I trained which got a validation accuarcy of about 0.83.
- `_cnn_models_and_weights/model_second_try.json`: second CNN that I trained which got a validation accuracy of about 0.90 
- `_cnn_models_and_weights/first_try_weights.h5`: the weights of the first CNN 
- `_cnn_models_and_weights/second_try_weights.h5`: weights of the second CNN, which also needs to be loaded along with it to be used properly. 
- For more information on how to load them please refer to the notebook `_scripts_and_notebooks/1_building_testing_CNN_notebook.ipynb`

4. Other Images folder `_images`:
- `_images/snake_id.jpg`: This is just an image file of the plot output of the validation analysis, which shows the results of idenification. The plots of images which have a green border were correctly predicted, where as red border is wrong.

5. Snake Image data:
- `_snakes_american_data/read_first.txt`: Just a text file containing the link to the image dataset and which snake classes were used. The file was too large to upload on GitHub.   
