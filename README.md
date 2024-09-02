# Fashion_recommendention_system Using CNN
Data Description

1.Dataset Overview
•	Total Images: 44,000
•	Image Resolution: 224 x 224 pixels
•	Image Channels: 3 (RGB)

2.Embeddings
Definition: Embeddings are high-dimensional feature vectors extracted from images of fashion items using a pre-trained ResNet50 model. These vectors represent the visual characteristics of the images.
Format: A numpy array of floating-point numbers, where each vector typically has a fixed length based on the model's architecture.
Purpose:
1.Similarity Search: Used to find visually similar fashion items by comparing feature vectors.
1. Storage: Efficiently store the visual representation of images for fast retrieval.
2. Normalization: Ensures that all feature vectors are of unit length, which helps in improving the accuracy of the nearest neighbors search.
3. Example: [0.045, 0.023, 0.078, ...] (an array of features extracted from an image).
   
3.Filenames
Definition: Filenames are the paths to the images of fashion items in the dataset. They link the extracted feature vectors to their corresponding images.
Format: A list of strings, where each string is the file path to an image.
Purpose:
1.Identification: Helps in identifying and displaying the actual images corresponding to the feature vectors.
2.Linking Data: Used to link the extracted features with the original images.

2. Retrieval: Facilitates the retrieval and display of images in the recommendation system.
Example: ['images/shirt.jpg', 'images/pants.jpg', 'images/dress.jpg']

Sample Input
Dataset Overview
•	Total Images: 44,000
•	Image Resolution: 224 x 224 pixels
•	Image Channels: 3 (RGB)

Preprocessing Steps
1.	Image Loading: Load images from the dataset directory.
2.	Resizing: Ensure all images are resized to the target resolution of 224 x 224 pixels.
3.	Normalization: Normalize pixel values to the range [0, 1] by dividing by 255.
4.	Augmentation: Optionally apply data augmentation techniques to enhance the training dataset.
Example:
1. Upload a Sample Image:
   The user uploads an image named sample_image.jpg.
2. Embeddings and Filenames Data:
   embeddings.pkl file contains the feature vectors (embeddings) for various fashion images.
    filenames.pkl file contains the filenames corresponding to the fashion images in the dataset.

Expected Output
The hybrid recommendation model generates a list of recommended movies for a user, 
1. Display Uploaded Image:
The application displays the uploaded image sample_image.jpg.
2. Feature Extraction:
   The application extracts features from the uploaded image using the pre-trained ResNet50 model.
   The extracted features are normalized.
3.Recommendation:
   The application finds the 5 most similar images in the dataset using the Nearest Neighbors algorithm.
   The application displays the 5 recommended images that are similar to the uploaded image.

