## Image Classification Script

This script is designed for classifying images into predefined categories. It leverages a pre-trained model to predict the class of each image in a specified directory.

### Process Overview

1. **Dependencies**: The script uses TensorFlow, particularly the Keras API, for working with the neural network model, and Scipy for some additional functionality.

2. **Image Loading**: 
    - The script starts by defining parameters such as image dimensions (HEIGHT and WIDTH) and the class names extracted from the training dataset.
    - It then initializes an array to hold the images.
    - It reads each image from the 'dataset/validation/all' directory, resizes it to the required dimensions, and adds it to the array.

3. **Model Loading**: 
    - A pre-trained TensorFlow Keras model is loaded from an H5 file ('final_model_923.h5'). This model is expected to have been trained on a similar set of data.

4. **Making Predictions**: 
    - The script uses the model to predict the class of each image. 
    - For each prediction, it sorts the probabilities to find the top three predicted classes.

5. **Results Compilation**: 
    - A pandas DataFrame is created to store the results. 
    - It includes the image name and the top three predictions for each image.

6. **Displaying Results**: 
    - The script prints out the final DataFrame containing the image names and their predicted classes.

### Usage

- Ensure you have a trained model saved as 'final_model_923.h5'.
- Place the images you want to classify in the 'dataset/validation/all' directory.
- Run the script. The predictions will be printed out as a DataFrame.

### Note

- The script assumes the existence of certain directories and files (like the H5 model file).
- Make sure to adjust the paths and model file name as per your setup.

