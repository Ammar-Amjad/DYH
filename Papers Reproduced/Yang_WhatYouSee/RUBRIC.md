# Do Your Homework Rubric #

## Paper Title ##: What You See is Not What the Network Infers: Detecting Adversarial Examples Based on Semantic Contradiction

## Authors ##: Yijun Yang∗, Ruiyuan Gao∗, Yu Li∗, Qiuxia Lai†, and Qiang Xu∗

### <strong>DATASET</strong> ###

* What is the data they use to train? ( Brief description)
    * MNIST, GTSRB and CIFAR-10.
* Can you immediately Download the Dataset?
    * Yes
    * If yes, is the dataset in a CSV or folder? 
        * Data is in .png format.
    * If no, do they have any method for obtaining the data? (e.g., “request access to data from …” or “make an account at …”)
        * Yes.
* Is the Data Described?
    * Yes
    * Do they provide a paragraph description of their data?
        * Yes 
    * If data is featurized, Do they provide all of the features or columns of the data? 
        * Yes
    * If they created the dataset, Do they list where they collected it?
        * Yes
    * Do they list the size of the dataset? (Total Samples)
        * Yes.
            * MNIST has 10 classes with 50,000 + 10,000 images used.
            * GTSRB has 43 classes with 35,288 + 12,630 images used.
            * CIFAR-10 has 10 classes with 50,000 + 10,000 images used.
    * Do they describe the range of each feature?
        * Yes
* How many datasets are used? (If more than one, provide citation if not created)
    * 3 datasets.
    * If a dataset is included from different work, Can you download that dataset?
        * Yes, 
        * -> MNIST(http://yann.lecun.com/exdb/mnist/) 
        * -> GTSRB(https://sid.erda.dk/public/archives/daaeac0d7ce1152aea9b61d9f1e19370/published-archive.html) 
        * -> CIFAR-10 datasets(https://www.cs.toronto.edu/~kriz/cifar.html).
* Do they describe any preprocessing steps? (PCA, scaling, normalziation)
    * Conditional Batch Normalization (CBN) technique is used on cGAN.
    * Adam optimizer is employed.
    * ReLU is used as the activation function.
    * Each of DMM, Dis, and SSIM have their own loss functions.
* Do they split their data into training/validation/test?
    * They don't have a validation set but have a train and test set.
    * If yes, do they use a separate distinct set for a test set?
        * Yes 
    * Do they use any cross-validation?
        * No
    * Is the downloaded data separated into train/val/test?
        * No
    * If not, do they provide a random seed for their splitting?
        * No

###<strong>CODE</strong>###

* Is the Code linked in the paper?
    * Yes
* Is the Code linked to author website? (Github)
    * Yes
* Do they link a compiled app?
    * No
* Did they do hyperparameter tuning?
    * Yes
    * If yes: Did they perform a gridsearch or random search?
        *  No 
    * Do they list the parameters with which a search was performed? (Range of features)
        * Yes
* Do they describe the method of the model in the paper?
    * Yes
* Is there a visualization of the model? 
    * Yes
* Do they describe the types of layers they use? (Convolutional, LSTM, Dense)
    * Yes, Convolutional.
* What is their activation function? (ReLU, Sigmoid, Tanh, etc)
    * ReLU
* What is their loss function?
    * Loss functions made from combinations of Deep Metric Model’s loss (Cross-Entropy), Discriminator’s loss (LDis = ReLU (1−Dis(x))), SSIM and ℓ2
* Do they provide how long it was trained for? (Epochs not time)
    * 15 epoch
* How long did it take to train their model? (hours, days, …)
    * No
* Do they provide justification for how long it was trained? (Earlystopping, chose arbitrary # of epochs)
    * No
* Do they describe the computing resources they used?
    * No
* What are the batch sizes they use?
    * 128
* Do they say how their batches are generated (randomly sampled, special technique)?
    * No
* Do they use batch normalization?
    * Yes, Conditional Batch Normalization (CBN) is used.
* If there is code:
    * Yes
    * Does the repository have any code in it?
        * Yes
    * Can you download it?
        * Yes
    * Is there a README.md?
        * Yes
    * Is there an environment saved?
        * Not sure
    * Do they list all libraries and versions of the library needed?
        * Yes -> https://github.com/cure-lab/ContraNet/blob/main/whitebox_attacks/environment.yaml
    * Is there a saved model?
        * Yes
    * Is their code commented?
        * Yes but very little or in Chinese.
    * Do you need to re-train/further train the model?
        * Not sure
    * Can you run a command to start training?
        * Yes
    * Can you run a command to predict on the old data?
        * Yes
    * Can you predict one new sample?
        * Yes
    * Do they include all relevant code? (Model training, preprocessing, predicting)
        * Yes
    * If alternate data formats (jpg vs png, flac vs wav), does the code handle new data format?
        * Not sure
    * Is their code optimized for GPU?
        * Not mentioned
    * When running their code on the dataset, do you get the same results reported in the paper?
        * Havnt checked yet.













