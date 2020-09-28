# Tarea 6 generative adversarial networks (GANs)
Generative Adversarial Networks module for the Advanced Machine Learning course at Universidad de los Andes.

Students: Natalia Suarez and Cristhian Forigua 

Tutors: Camila Escobar and Angela Castillo

## Objectives:
1.  Learn to generate artificial data by using Generative Adversarial Networks.
2.  Solve one of the most common problems in the GANs framework.
3.  Learn how to use a model for multidomain image-to-image translation.

## Requirements
We suggest you create a new conda environment for this task. 
To create the new environment run the following line: 
```
$ conda create --name envname python=3.7.6
```
To install the remaining requirements run the following: 
```
$ conda install pytorch==1.2.0 torchvision==0.4.0 cudatoolkit=9.2 -c pytorch
$ pip install -r requirements.txt
```
For this homework, we want you to explore two of the most important applications of GANs: Image generation and image-to-image translation.
## Part 1: Image generation
For this part we will be using the MNIST Dataset. The idea here is to generate images from 0 to 9 by using a conditional generative adversarial network (CGAN). As an example, we left you the expected generated sequence that you should achieve. 

<img src="https://user-images.githubusercontent.com/66923636/94369443-53caab80-00af-11eb-9a44-1221e2a8716b.png" />

### Running the code:
To start, run the following line: 
```
$ python CGAN.py
```
### Visualizing the results
When you run the code a new folder (named "images") will be created. Inside that folder all your results will be saved. 
### Report part 1
1. Go to the function sample_image and complete it. Follow the steps we leave you as a guide (0.5 points). 
2.  Run the file CGAN.py and take a look at the results you obtained. How are the results? Do you consider there is a problem? If you do, mention the problem and why it could be happening. Otherwise, justify why you consider the results are good (0.5 points).
3.  Explore the code and understand it. Based on your previous answer, try to improve your results by changing whatever you want (batch_size, lr, sample noise, steps for G, etc). Discuss what results are better and why. Be sure to include all the results in the report. Remember that it is up to you to decide which results are better because there is not a general metric of evaluation (1.5 points).
4.  Take the baseline model and compare it with the model that got the best results. Graph the Discriminator and Generator losses against the epoch and discuss (0.5 points).
## Part 2: Multidomain image-to-image translation: 
The idea here is to translate an image into five different domains by using StarGAN. For this part we will be using the CelebA Dataset. 
<p align="center"><img width="40%" src="http://mmlab.ie.cuhk.edu.hk/projects/celeba/intro.png" /></p>
For simplicity, we will train our models for only 5 domains: 

                'Arched_Eyebrows', 'Blond_Hair', 'Brown_Hair', 'Male', 'Young'
### Running the code:
To start, run the following line inside the StarGAN folder: 
```
$ python main.py
```
### Visualizing the results
Go to the folder StarGAN -> stargan -> samples. Her you will find the multidomain translation results at every 1000 iterations. 
### Report part 2
1.  Run the baseline model we gave you. Show your results and describe them. Why do you think the results are not so good?. For this point you can either use the pretrained weights we provide you or train from scratch. The pretrained weights are available at /media/user_home2/Data_AML/CelebA/models (points 0.5).
2.  Take the StarGAN generator loss function, change the strength of one term to zero and visualize the results. Do the same for the discriminator loss function. Discuss, based on the results, the importance and influence of each loss function you chose. At this part, you should have two experiments: one for the generator and one for the discriminator (points 1.5).
## Bono
Create a .txt file like the one in /media/user_home2/Data_AML/CelebA/list_attr_celeba.txt. Do not modify the first six lines and in line number 7 put the path of a one-person face image (different to the ones provided in the dataset). Classify it according to the dataset classes and the number correspondent for each class. 
For example, the next line shows an exmample of a 5 classes dataset and the image have the attributes 3 and 4: 

imageNew.jpg -1 -1 1 1 -1


Finally, show the resulting images generated for the selected labels. Show the result and discuss it (0.5 points).
## Deadline
19th October 2020 - 11:59 pm
## Credits
This repository is adapted from Erik Linder-Norén PyTorch-GAN implemention, which can be found at https://github.com/eriklindernoren/PyTorch-GAN 
