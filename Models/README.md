#  The file contains a experimentation 
This code defines a flexible TensorFlow/Keras model builder framework for transfer learning image classification models. 
Its main goal is to let the user:
*  choose a pretrained CNN backbone (MobileNetV2, ResNet50, EfficientNetB0, etc.) 
*  attach different classifier “heads” 
*  optionally load saved architectures/weights from files 
*  Provide a list of multiple modes ready to be __compiled__

## The Deducted version that was used.
I wanted a fast, simple solution to run all the experiments thus I deduct parts from the previous projectto create a function:
*  Selection of Pretrained CNN
*  User can provide a list of functions that create a classification head
    *  Essentially the function is a wrap of Tensorflow Functional API

### Functionalities in the form of Callbacks
We have the main callback a combination of multiple functionalities and is responsible for:
  *  Saving the metrics of each model. The file has a __custom name__ that consists of :
        *  Date & Time
        *  The model name
        *  Specific metrics that the model stoped
  *  Early Stoping. Depending on the score of the metrics
  *  Saving and storing the model and the weights for fast reloads.

     
The second callback provides live updates of specific statistics with the form of graphs
![Live updates](https://github.com/user-attachments/assets/25981b50-a3b9-4d8f-81f2-0b4aa13f1c6c)

