# Pre-trained-Image-Classifier-to-Identify-Dog-Breeds

This project is part of the AWS AI&ML Scholarship program by Udacity. The goal of this project is to use a pre-trained image classifier to identify dog breeds.

## Project Overview

In this project, three different pre-trained image classifiers (ResNet, AlexNet, and VGG) used  to classify images of dogs and their breeds. Also, performance of these classifiers compared the  and determined which one is the best for this task.

## Project Instructions

To run this project, you will need Python 3 and the following libraries:

- argparse
- os
- time
- torch
- torchvision

You can install these libraries using pip or conda.

To execute the project, run the following command in your terminal:

```bash
python check_images.py --dir pet_images/ --arch vgg --dogfile dognames.txt
```

You can change the arguments as follows:

- `--dir`: The directory that contains the images to be classified. The default is `pet_images/`.
- `--arch`: The pre-trained image classifier to be used. The options are `resnet`, `alexnet`, or `vgg`. The default is `vgg`.
- `--dogfile`: The file that contains all the valid dog names. The default is `dognames.txt`.

The output of the program will be printed on the terminal and also saved in text files in the same directory as the images. The text files will have names such as `vgg_pet-images.txt`, indicating the classifier and the image folder used.

## Project Results

The following table summarizes the results of running the program with different classifiers and image folders.

| Classifier | Image Folder | Number of Images | Number of Dog Images | Number of Not-a Dog Images | % Correct Dogs | % Correct Breed | Time |
|------------|--------------|------------------|----------------------|---------------------------|----------------|-----------------|---------------------|
| ResNet     | pet_images   | 40               | 30                   | 10                        | 100.0          | 90            | 0:0:4               |
| AlexNet    | pet_images   | 40               | 30                   | 10                        | 100.0          | 80.0            | 0:0:2               |
| VGG        | pet_images   | 40               | 30                   | 10                        | 100.0          | 93.3            | 0:0:11               |

Based on these results, we can conclude that ResNet and VGG are better than AlexNet for this task, as they have higher accuracy for both dog breed identification and not-a-dog detection. ResNet and VGG also have higher percentage of label matches than AlexNet.
