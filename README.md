# Artist-identification-of-a-painting

Problem Statement :- 
Identify Van Gogh's painting from a given dataset of paintings(Images). This can help in verification/identification of artist of the painting from a given image. Similar approach can also be used for signature verification.

Dataset Link :- 
https://figshare.com/articles/From_Impressionism_to_Expressionism_Automatically_Identifying_Van_Gogh_s_Paintings/3370627

To solve this task following steps were followed.

For train data, we will 
	Create 10 patches of each image i.e. Divide each image into 10 different patches 
	Extract features of these patches using any pretrained model like VGG16, VGG19, ResNet, InceptionNet.
	Train a logistic regression or svm on these extracted features.

For test set, we will 
	Take each image create its 10 patches
	Extract features of these 10 patches using above models
	Classify the patches into 1/0 using the logistic regression or svm model, we train above.
	For each image we will have 10 predictions, we will take mean of these 10 predictions to predict that the complete image  belongs to Class 1 or 0.
