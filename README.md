# Dog Breed Recognition Model

This project utilizes the jetson-inference library to run a machine learning model on a jetson nano device. This model can distinguish the 70 different breeds that it was trained on, and it
will take in an input image of a dog and return a prediction of its breed. Knowing your dog's breed provides information on how to accomodate their lifestyles and personalities, allowing 
owners to provide them the best life possible.

Here are some image results:

![Vizsla_Result](https://github.com/user-attachments/assets/90fbd7d7-78e8-4491-b0b7-62d8f275cdfe)
![Borzoi_Result](https://github.com/user-attachments/assets/6ccb2527-4482-44a4-bbb3-32c177f30180)

## The Algorithm

This project uses a resnet-18 onnx model which was retrained on 70 different dog breeds to identify a dog's breed in any image input into the model. After calling the imagenet file from
the jetson-inference library, it returns its prediction of the dog's breed and its certainty in its prediction.

## Running this project

1. Make sure to install the python3 library beforehand in order to run this project.
2. Clone this repository in an IDE on your device.
3. Open your IDE terminal and cd into the root directory of this project.
4. To run this model 
  a. with an image from the test folder, enter "python3 dog_breed_recognition.py data/test/BREED/NUM.jpg" where BREED is one of the 70 breeds in the dataset and NUM is the number of the image.
  b. with your own image, enter "python3 dog_breed_recognition.py /path/to/image" where /path/to/image is the path to the image that you want to run through the model.
5. The result of the model's prediction and accuracy is printed as the last line in the terminal for you to view.

Here is a [video demonstration](https://youtu.be/p0pZBpEXp8w) on how to run the model after downloading the required files and library.
