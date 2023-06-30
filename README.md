# Pre-trained-Image-Classifier-to-Identify-Dog-Breeds

This project is part of the AWS AI&ML Scholarship program by Udacity. The goal of this project is to use a pre-trained image classifier to identify dog breeds.

## Project Overview

In this project, you will use three different pre-trained image classifiers (ResNet, AlexNet, and VGG) to classify images of dogs and their breeds. You will also compare the performance of these classifiers and determine which one is the best for this task.

The project consists of the following steps:

- Get program inputs from the user using the `get_input_args.py` file.
- Create a `pet_images` folder and populate it with at least 40 images of dogs and other animals. The images should be labeled with the pet's name in the filename, such as `Beagle_01141.jpg`.
- Create a `dognames.txt` file that contains all the valid dog names that can be classified by the image classifiers. This file will be used to check if an image is of a dog or not.
- Use the `get_pet_labels.py` file to create a dictionary that maps each image filename to a list containing the pet's name from the filename.
- Use the `classifier.py` file to classify each image using the three pre-trained image classifiers. This file will return the model's label as a string for each image.
- Use the `adjust_results4_isadog.py` file to adjust the results dictionary to indicate if an image is of a dog or not, and if the model's label matches the pet's name or not.
- Use the `calculates_results_stats.py` file to calculate the statistics of the results, such as the number and percentage of correct and incorrect classifications.
- Use the `print_results.py` file to print out the results and statistics in a user-friendly format.

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
