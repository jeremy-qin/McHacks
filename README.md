# McHacks
McHacks Challenge - Covid19 Detection Prototype



The dataset folder contains all the data used in our model to predict ones' chance of having/contacted covid. The data used were from two open public datasets : Covid-CT and SARS-CoV-2. The two datasets can be found in the following URLs: https://www.kaggle.com/plameneduardo/sarscov2-ctscan-dataset and https://github.com/UCSD-AI4H/COVID-CT

We used a prototype implemented with figma to imitate what it should of looked like in a real application.
Of course, the results found in the prototype might not correspond to the actual prediction, but as mentioned before, 
this prototype is fixed and does not have any algorithm from the model implemented within. 

To train our model, we used the Huawei MindSpore Framework on the Huawei AI Platform. The training was done on a provided Huawei Ascend Processor (NPU) training server, which is enabled by Huawei Ascend CANN Compute Architecture for Neural Networks. If we wanted to create a real application, using MindSpore allows us to train deep neural networks more easily. In our case, we used MindSpore GoogleNet convolutional neural network for our binary image classification task.

In order to train and evaluate the model on the command line, we directly put our create_dataset function in dataset.py that was given to us in the MindSpore guide. Below, will show how to execute them on the command line.

Notebooks were also created to give a demo of how we loaded our data and how we can use it to train our model.

# How to train model on command line:
In command line, type: python train.py

# How to evaluate model on command line:
Change config.py for testing dataset.
In command line, type: python eval.py --checkpoint_path= example_path


# References:
Xingyi Yang et al. COVID-CT-Dataset: A CT Scan Dataset about COVID-19. 2020. arXiv: 2003.13865. URL: https://arxiv.org/abs/2003.13865

Soares, Eduardo, Angelov, Plamen, Biaso, Sarah, Higa Froes, Michele, and Kanda Abe, Daniel. "SARS-CoV-2 CT-scan dataset: A large dataset of real patients CT scans for SARS-CoV-2 identification." medRxiv (2020). doi: https://doi.org/10.1101/2020.04.24.20078584.
