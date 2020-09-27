# Tarea 6 generative adversarial networks (GANs)
Generative Adversarial Networks module for the Advanced Machine Learning course at Universidad de los Andes.
Students: Natalia Suarez and Cristhian Forigua 
Tutors: Camila Escobar and Angela Castillo

## Objectives:
1.  Learn to synthesis artifitial data by using Generative Adversarial Networks.
2.  Solve one of the most common problems in the framework.
3.  Learn how to use a model for multidomain image-to-image translation.

## Requirements
We suggest you to create a new conda environment for this task. 
To create the new environment run the following line: 
```
$ conda create --name envname python=3.7.6
```
To install the remaining requirements run the following: 
```
$ conda install pytorch==1.2.0 torchvision==0.4.0 cudatoolkit=9.2 -c pytorch
$ conda pip install -r requirements.txt
```
For this homework, we want you to explore two of the most important applications of GANs: Image generation and image-to-image translation.
## Part 1: Image generation
For this part it will be used the MNIST Dataset. The idea here, is to generate images from 0 to 9 by using a conditional generatvie adversarial network (CGAN). As an example, we let you an expected sequence of generated images you sould reach.
![187200](https://user-images.githubusercontent.com/66923636/94369443-53caab80-00af-11eb-9a44-1221e2a8716b.png)
### Running the code:
To start, run the following line: 
```
$ python CGAN.py
```
