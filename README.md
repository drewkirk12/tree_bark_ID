This is a revised version of BarkNet 1.0 currently using the ResNet34 architecture
The following link is the BarkNet article https://arxiv.org/abs/1803.00949

The training and main testing dataset can be downloaded in 4 parts at the the following link to the BarkNet Github page:  https://github.com/ulaval-damas/tree-bark-classification
Once these files are downloaded they should be placed into 23 seperate folders each with their class abbreviation. (ie: "BOJ"). These folders should then be placed into a folder named "images". The location of this folder should be specified as the DATASET_PATH in line 1 of the hyperparameters class. (ie: DATASET_PATH = "C:/Users/drewk/OneDrive/Desktop/CS Projects/images/")

Training Directions:
To train a new model from scratch start by setting "MODEL" in the hyperparameters class on line 20 to the resnet architecture you would like (i.e. "resnet34" or "resnet50") and set OLD_MODEL on line 4 to None

If you already have a pretrained model set OLD_MODEL on line 4 of hyperparameters to the path where the model is saved (i.e. "saved_models/model_1.pth")

Now set NEW_MODEL on line 5 of hyperparameters to the path where you would like this trained model to be saved

If you wish to change the number of epochs the model trains for set N_EPOCHS on line 7 of hyperparameters to the integer value of epochs you would like

Now running "train.py" with "python train.py" in the command line will begin training your model printing the time, accuracy, and loss of every epoch

Testing Directions:
To test your model make sure that OLD_MODEL in hyperparameters on line 4 is set to the file location of the model you would like to test (i.e. "saved_models/model_1.pth")

If you already have a loaded dataset then set EXISTING_DATASET in hyperparameters line 26 to the file path of the dataset (i.e. "dataset.txt")

If you would like to test on different images then set TEST_IMAGES to the file path of the images. If the images have associated labels 

