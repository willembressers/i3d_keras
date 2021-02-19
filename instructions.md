# Computer vision assignment

## Introduction
The goal of this assignment is to dive quickly into the field of computer vision called action recognition and build a model which solves a simple task.

## Action recognition
The goal of action recognition is to classify videos. This means given video as a sequence of frames return as output type of action which is happening in the video. The largest focus in the field is the recognition of human activities and there are several proposed architectures and datasets. Some of the state of the art backbone architectures are SlowFast, C2D and I3D.

## The dataset
The dataset consists of a random selection of 5 classes from the [UCF50](https://www.crcv.ucf.edu/data/UCF50.php) dataset. This is the [corresponding publication](https://www.crcv.ucf.edu/data/UCF50_files/MVAP_UCF50.pdf). It is a relatively old action recognition dataset and most modern architectures should help you achieve a decent classification score. 

The dataset is in the `data` folder and is already split into two subfolders, `train` and `test`. Each of those folders contains one directory for each of the 10 categories, inside which you can find the images of a video snippet.

## Solution tools suggestion
We append below a list of tools you can use to tackle this assignment. This is in order to narrow down the focus and make the duration of solving it reasonable. Nevertheless, feel free to use any library and language you feel comfortable with in order to tackle the problem.

1. Action recognition architecture: [I3D](https://arxiv.org/abs/1705.07750)
1. Implementation of I3D in Keras: [i3d_keras](https://github.com/OanaIgnat/i3d_keras)
1. Coding environment with free GPU resources: [google colab](https://colab.research.google.com)
    - Hint: Colab can be a bit clunkier than jupyter notebooks, so develop locally and upload when you really need the GPU

## Tasks
This is the list of the assignment tasks. Each task has a small hint. The idea is similar to the tools suggestion above: use the hints to save time but feel free to ignore them and follow your own path if you want to. 
- Read the image data in 4D tensors and display a couple of them as sequences of images.
    - Hint: You can read them using numpy, transform to a tensorflow tensor and pass to a tensorflow dataset.
- Load an action recognition pretrained model and write code which generates a prediction per video. Visualize a couple of outputs.
    - Hint: Load the one of the kinetics i3d models with single modality (the ones using optical flow add more complexity and work) and write a small loop which generates the predictions. You can see some example code in the `evaluate_sample.py` file of the repository.
- Choose an appropriate metric and evaluate the performance of the model on the testing dataset.
    - Hint: The classes of the two datasets are not perfectly matched. Find a good compromise to deal with that.
- Sketch the process of training the model on the train dataset using a combination of pseudocode and tensorflow functions.
    - Hint: You can use again as a template the sample code in the `evaluate_sample.py`. Use a model with only the RGB part.
- *BONUS*: Train a model on the training dataset which clearly exceeds the performance of the pre-trained model on the test dataset.
    - Hint: There will be more focus on the code of the solution rather than on the model performance, so don't spend too much time on optimizing it.

## Solution
Please send us the code of your solution together with instructions on how to run it. Good luck!
