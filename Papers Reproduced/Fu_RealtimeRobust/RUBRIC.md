# Do Your Homework Rubric #

## Paper Title ##: Realtime Robust Malicious Traffic Detection via Frequency Domain Analysis
## Authors ##: Chuanpu Fu, Qi Li, Meng Shen, and Ke Xu

### <strong>DATASET</strong> ###

* What is the data they use to train?( Brief description)
    * 3 datasets from the MAWI website having 42 malicious attacks.
* Can you immediately Download the Dataset?
    * Yes 
    * If yes, is the dataset in a CSV or folder? 
        * Yes
    * If no, do they have any method for obtaining the data? (e.g., “request access to data from …” or “make an account at …”)
        * N/A
* Is the Data Described?
    * Do they provide a paragraph description of their data?
        * Yes
    * If data is featurized, Do they provide all of the features or columns of the data? 
        * Yes
    * If they created the dataset, Do they list where they collected it?
        * Yes, MAWI Website. -> http://mawi.wide.ad.jp/mawi/
    * Do they list the size of the dataset? (Total Samples)
        * 2.45 GB + 2.72 GB + 1.43 GB respectively.
    * Do they describe the range of each feature?
        * No.
* How many datasets are used? (If more than one, provide citation if not created)
    * 3 datasets.
    MAWI 2020.06.10 -> http://mawi.wide.ad.jp/mawi/samplepoint-F/2020/202006101400.html
    MAWI 2019.1.2 -> http://mawi.wide.ad.jp/mawi/samplepoint-F/2019/201901021400.html
    MAWI 2020.1.1 -> datasets
    http://mawi.wide.ad.jp/mawi/samplepoint-F/2020/202001011400.html
    * If a dataset is included from different work, Can you download that dataset?
        * Yes
* Do they describe any preprocessing steps? (PCA, scaling, normalziation)
    *  min-max normalization operation on the frequency domain features
    *  Adam optimizer is used for gradient descent.
    *  Sigmoid activation function is used with the autoencoder.
* Do they split their data into training/validation/test?
    * Yes, Data of 6 attacks is used in the validation set.
    * If yes, do they use a separate distinct set for a test set?
        * Yes, Data of 13 attacks is used as the test set.
    * Do they use any cross-validation?
        * No.
    * Is the downloaded data separated into train/val/test?
        * No.
    * If not, do they provide a random seed for their splitting?
        * No.

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
        * Not mentioned
    * Do they list the parameters with which a search was performed? (Range of features)
        * Yes
* Do they describe the method of the model in the paper?
    * Yes
* Is there a visualization of the model? 
    * Yes
* Do they describe the types of layers they use? (Convolutional, LSTM, Dense)
    * No
* What is their activation function? (ReLU, Sigmoid, Tanh, etc)
    * Sigmoid
* What is their loss function?
    * Averaged L2-norm 
* Do they provide how long it was trained for? (Epochs not time)
    * 200 epochs
* How long did it take to train their model? (hours, days, …)
    * Not mentioned
* Do they provide justification for how long it was trained? (Earlystopping, chose arbitrary # of epochs)
    * No
* Do they describe the computing resources they used?
    * Yes
* What are the batch sizes they use?
    * 128
* Do they say how their batches are generated (randomly sampled, special technique)?
    * No
* Do they use batch normalization?
    * Not mentioned
* If there is code:
    * Does the repository have any code in it?
        * Yes
    * Can you download it?
        * Yes
    * Is there a README.md?
        * Yes
    * Is there an environment saved?
        * No
    * Do they list all libraries and versions of the library needed?
        * Yes
    * Is there a saved model?
        * No 
    * Is their code commented?
        * Yes
    * Do you need to re-train/further train the model?
        * Not sure
    * Can you run a command to start training?
        * Not sure
    * Can you run a command to predict on the old data?
        * Not sure
    * Can you predict one new sample?
        * Not sure
    * Do they include all relevant code? (Model training, preprocessing, predicting)
        * Yes
    * If alternate data formats (jpg vs png, flac vs wav), does the code handle new data format?
        * Not sure
    * Is their code optimized for GPU?
        * Not sure
    * When running their code on the dataset, do you get the same results reported in the paper?
        * Not sure













