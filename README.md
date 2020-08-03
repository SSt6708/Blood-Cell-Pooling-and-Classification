# Blood Cell Pooling and Classification
This is a project for our Machine Learning class where we completed it in a group of 4. Counting and distinguishing white blood cells for each patient is critical for diagnosing blood diseases and it takes hours for medical professionals to examine patient's blood samples. The main goal and inspiration behind this project was to use the power of machine learning to automate this process.

The model will take a patient's blood sample as an input and outputs the number of white blood cells and classifies each white blood cells into 4 types: Eosinophil, Lymphocyte, Monocyte, and Neutrophil.

We used dataset from Kaggle.com: https://www.kaggle.com/paultimothymooney/blood-cells

We pre-processed the dataset before using it to train our model because the dataset from Kaggle only has 1 white blood cell in each picture. We want to use a picture that consists of multiple types of white blood cells. We merged random pictures from the dataset into one new picture that has multiple cells in it.

![Screen Shot 2020-08-02 at 6 02 59 PM](https://user-images.githubusercontent.com/35588693/89136835-7f377c80-d4ea-11ea-8112-fb043ede9b05.png)

Noticed that we also pre-processed the data so that in the merged picture we can see rectangular bounding boxes for each cell.
![Screen Shot 2020-08-02 at 6 06 36 PM](https://user-images.githubusercontent.com/35588693/89136958-fff67880-d4ea-11ea-8fc0-1e9a0f70ea96.png)

After we pre-processed the data and split it into training, validation and test set, we then pass it into the RCNN (Regional-Convolutional Neural Network) model to train. We used AlexNet as our CNN to generate feature and classify. 
Below is the overview of our network architecture.

![Screen Shot 2020-08-02 at 6 16 36 PM](https://user-images.githubusercontent.com/35588693/89137257-54e6be80-d4ec-11ea-9f11-fe47264d3b00.png)

We achieved an accuracy of 92% with the test data.
