This is a revised version of BarkNet 1.0 currently using the ResNet34 architecture
The following link is the BarkNet article https://arxiv.org/abs/1803.00949

Training Directions: 
The only variables that may need changing are help in the hyperparameters class. The primary ones to
change are N_EPOCH (number of epoch), OLD_MODEL (file location of model to start with), and NEW_MODEL (file location of model about to be trained). Once those are set running the train file will train the model for N_EPOCHs and print the time, accuracy, loss, ect of each epoch and save the model at NEW_MODEL.

Testing Directions:
The only variable to change for testing is the OLD_MODEL variable in hyperparameters. This is the file location of the model to be tested. From here running the test file will test the model and print the accuracy on the test set. The ability to test on other datasets will be added soon. 

