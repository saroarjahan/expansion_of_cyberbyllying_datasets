Cyberbullying detection with WordNet-based semantic expansion and word disambiguation

# expansion_of_cyberbyllying_datasets

Our methodology includes three-stage process: data collection; data augmentation, feature engineering and classification; 
Motivated by the lack of availability of well-balanced annotated cyberbullying dataset, our methodology includes a new collected 
dataset from Ask.fm social network website and the use of the publicly Formspring dataset for comparison purposes. 
In the second phase, a data augmentation has been performed using a wordnet-based sense disambiguation technique and Lesk-algorithm.  
The classification process involves a CNN model and baseline classifiers (Bayes and linear regression) whose results are contrasted 
and the data augmentation process has been duly evaluated for both ask.fm and Formspring dataset.


Our repository is composed of 25 files: 

Among two files contain datasets namely askfm and fromspring, one requirement.tx for libraries requirements, one readme.md for instruction, and rest of the files contain results for extended datasets using method 1 (disambiguation), method2 (synonyms with Pos tagging) and method 3 (synonyms) on both datasets (askfm and fromspring), fastext classifier implementaion and mixup augmentaion.

Due to limitation, we are not able to upload FasText word embedding files. Please download from here and add the file to the repository.
https://drive.google.com/open?id=1SZHPIx1Bzk9744te1_t2vZdMtYGHy1bZ

Instruction about using this repository:

Some scenarios of the work:

1- Prepare expanded dataset using one of the methods  (M1, M2 or M3) 

2- Splitting the data (for each dataset) into training and validation sets with a percentage of 80% and 20%, respectively. We have also tested with other percentages, but we have kept a consistency in the papers.

3- Extraction of features: word level tf-idf, word level ngram level tf-idf and characters level tf-idf from training and testing sets.

4- Calculation of the word embbeding vectors. 

5- Traininig of the baseline classifiers (Naive Bayes and Linear Classifier) on the data, using different types of the features . Prediction and calculation of accuracy and F1 score.

6- Train of the CNN model on the data, prediction and calculation of accuracy and F1 score. Then, comparison of results obtained using CNN with results obtained using baseline classifiers.

7- Implementation of Fastest as classifier.

8- Implementation of mixup as an augmentation technique.

9- Experiment with different corpus datasets as training and testing.

<h3>Requirements:</h3>
<li>Python 3.7</li>
<li>Run dependencies 'requirements.txt' by using  command:'pip install -r requirements.txt' (from command line) or '!pip install -r requirements.txt' (inside jupyternotebook)</li>
<li>JupyterNoteBook required, Running Command for each cell in jupiter is: <strong>ctrl+enter</strong></li>

<h3>Datasets:</h3>
There are two dataset files- AskFm (ask_fm_data.csv)  and FromSpring (formspring_all.csv).


<h3>Produced results-</h3>
<strong>Table 3:</strong> Result comparison between FastText as text classifier and FastText as word embedding withCNN for AskFm base dataset.

<ol>
	<li><strong>FastText as classifier:</strong> implementation with AskFm dataset can be found by running 19 number file name fastext.ipynb. This file use 'ask_tain.txt' as train datasets and 'ask_test.txt' as test dataset.</li>
	<li>
<strong>FastText as wordembedding:</strong>  For testing this result 9 number file name 'askfm_not_extended.ipynb' should be run. This file use ask_fm_data.csv as train and test dataset.</li>
</ol>


<strong>Table 4: </strong> Classifier Accuracy (%) and F1 scores (%) for AskFm not expanded dataset,  and its underlying expanded datasets using method 1, 2 and 3 respectively.

<ol>
	<li>For testing file 9 to 12 should be run.</li>
</ol>


<strong></strong>Table 5: Classifier Accuracy (%) and F1 scores (%) of CNN classification using word embedding representation for original and expanded datasets. Cross dataset1 consists in creating a training set from AskFm and test set from FormSpring and Cross dataset2 consists in creating a training set from Formspring and test set from AskFm

<ol>
	<li>there are 8 file rename from (1-8) for experiemnting difeerent training and test experiemnt. we have test Askfm(train) vs FromSpring(test), and FromSpring(train) Vs AskFm(test).</li>

</ol>


<strong>Table 6:</strong> Result comparison with Mixup technique, random word dataset, and using training and test dataset from different corpus.

<ol>
	<li>Mixup implentation:</li> for testing mixup 'mixup.ipynb' file 18 should be run. It will get Askfm dataset as mixup augmentation.
	<li>Random word dataset:</li> for testing  'askfm_extended_Datasets_with_random_word.ipynb' file number 20 should be run.
	<li>Different train and testing:</li>  fortesting file number 1- 8 should be run.
</ol>




