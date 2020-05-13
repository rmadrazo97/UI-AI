# UI-AI

UI-AI is a NN (neural network) for identifying basic UI (User Interface) sketched components. These components are based on the most widely used front-end components library. The basic components (classes) that this NN can identify are:
| Class        | Component           | 
| ------------- |:-------------:| 
| 0 | button |
| 1 | card |
| 2 | carousel |

## Project Overview
#### This neural netwokr is a concept validation for a html an css AI generator which identifies sketches and returns pre-built components based on the recognized drawings. 
For this project I used a common Neural nerwork built with the help of tensor flow and Keras libraries. Specifically, the Keras secuential model, which provides a simple NN architecture with just a plain stack of layers as the image shown below. 

![alt text](https://miro.medium.com/max/874/1*eJ36Jpf-DE9q5nKk67xT0Q.jpeg "NN Keras")

## Files Structure


### Data Generation
In order to increase dataset size and reduce overfitting, I created a file which generated 5 transformed images for each drawing. The resulting images were randombly cropped, shifted, exposed, zoomed in and out with the help ok keras Data Augmentation.

### Image Converter
This notebook converts common (squared) png or jpg images into a np.array ready data structure which represent the image's files in a gray scale from 0 to 255. Using the folder structure provided for the data, it outputs 4 ready to use files:
        ..1. trainning images
        ..2. trainning labels
        ..3. testing images
        ..4. testing labels     
        
### Data
The data was generating using a digital sketches with a touchscreen and pen enabled device ( Ipad :) ).
In total I created 150 drawings for each class.

### Main
Laboratory like test using fashionmnist to test the libraries.

### Main2
Neural Network implementation using augmented dataset 

### Main2
Neural Network implementation with out the augmented dataset.

## Bootstrap Components
#### Button
Inline-style: 
![alt text](https://media.geeksforgeeks.org/wp-content/uploads/bootstrap-solid-button.png "Bootstrap Component")

#### Card
Inline-style: 
![alt text](https://i.stack.imgur.com/yV6OV.png "Bootstrap Component")

#### Carousel
Inline-style: 
![alt text](https://javascript-source.com/designblog/data/upload/2017/04/indicators-example.jpg "Bootstrap Component")


#### Carousel

More on Boostrap here: [Boostrap Docs](https://getbootstrap.com/)

## Results
The resulting models provided an average accuracy between 35% up to 52% which are fair enough results for the dataset size and neural network architecture and techniques used.
The model could be severely improved using a convolutional neural network which are optimal architectures for image identification. 
As a concept validation and "prototype" this model prooves that it is possible to identify common ui sketches and identify it's classes. With this in hand, I would like to continue the project with a proper NN architecure and a broader and more diverse dataset. Providing a web interface to upload sketches and download pre-built UI with html, js, css and bootstrap

## Author
- Alejandro Madrazo
.- Universidad Francisco Marroquin | 2020
