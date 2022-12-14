This is a revised version of BarkNet 1.0 currently using the ResNet34 architecture
The following link is the BarkNet article https://arxiv.org/abs/1803.00949

The training and main testing dataset can be downloaded in 4 parts at the the following link to the BarkNet Github page:  https://github.com/ulaval-damas/tree-bark-classification
Once these files are downloaded they should be placed into 23 seperate folders each with their class abbreviation. (ie: "BOJ"). These folders should then be placed into a folder named "images". The location of this folder should be specified as the DATASET_PATH in line 1 of the hyperparameters class. (ie: DATASET_PATH = "C:/Users/drewk/OneDrive/Desktop/CS Projects/images/")

Training Directions:
To train a new model from scratch start by setting "MODEL" in the hyperparameters class on line 20 to the resnet architecture you would like (i.e. "resnet34" or "resnet50") and set OLD_MODEL on line 2 to None

If you already have a pretrained model set OLD_MODEL on line 2 of hyperparameters to the path where the model is saved (i.e. "saved_models/model_1.pth").

Now set NEW_MODEL on line 3 of hyperparameters to the path where you would like this trained model to be saved

If you are training on a images other than those which you have locally loaded into "dataset.txt" then make line 27 of hyperparameters "EXISTING_DATASET = None" This will have the generate_dataset class create a new dataset and save it at "dataset.txt". If you would
like to reuse the dataset saved in "dataset.txt" change line 27 of hyperparameters to EXISTING_DATASET = 'dataset.txt' or the filepath 
of the dataset.

If you wish to change the number of epochs the model trains for set N_EPOCHS on line 8 of hyperparameters to the integer value of epochs you would like

Now running "train.py" with "python train.py" in the command line will begin training your model printing the time, accuracy, and loss of every epoch

Testing Directions:
To test your model make sure that OLD_MODEL in hyperparameters on line 2 is set to the file location of the model you would like to test (i.e. "saved_models/model_1.pth")

If you already have a loaded dataset then set EXISTING_DATASET in hyperparameters line 27 to the file path of the dataset (i.e. "dataset.txt") otherwise set it to None and a new dataset will be generated based on hyperparameters line 1 IMAGE_PATH. By default this new dataset will be split into 75% training images and 25% testing images. To alter this split change hyperparameters line 19 "TEST_SPLIT" (i.e. 0.25 = 25% of images are used for testing)

If you would like to test on different images then set IMAGE_PATH on line 1 of hyperparameters to the file path of the images. If the images have associated labels set HAS_LABELS on line 5 to True

If you would like to record the predictions in a file put the path of the txt file where would would like the predictions as PREDICTION_PATH in hyperparmeters line 6

