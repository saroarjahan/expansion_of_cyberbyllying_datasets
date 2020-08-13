Cyberbullying detection with WordNet-basedsemantic expansion and word disambiguation

# expansion_of_cyberbyllying_datasets

Our methodology includes three-stage process: data collection; data augmentation, feature engineering and classification; 
Motivated by the lack of availability of well-balanced annotated cyberbullying dataset, our methodology includes a new collected 
dataset from Ask.fm social network website and the use of the publicly Formspring dataset for comparison purpose. 
In the second phase, a data augmentation has been performed using wordnet-based sense disambiguation technique and Lesk-algorithm.  
The classification process involves a CNN model and baseline classifiers (Bayes and linear regression) whose results are contrasted 
and the data augmentation process has been duly evaluated for both ask.fm and Formspring dataset.


Our reository is composed of 8 files: 

 2 files contain results for not expanded datasets for askfm and fromspring.

 Rest of the 6 files contain results for extended datasets using method 1 (disambiguation), method 2 (synonyms with Pos tagging) and method 3 (synonyms) on both datasets (askfm and fromspring).

Due to  limitation we are not able to upload fastext word-embbeding files. please download from here and add the file to the repository.
https://drive.google.com/open?id=1SZHPIx1Bzk9744te1_t2vZdMtYGHy1bZ

Instruction about using this reository:

Each file of the 6 files contains code to create an expanded dataset from (askfm and fromspring) using one of the proposed three methods. 

1- Prepare expanded dataset using one of the methods  

2- Splitting the data (for each dataset) into training and validation sets with a percentage of 80% and 20% respectively.

3- Extraction of features: word level tf-idf, word level ngram level tf-idf and characters level tf-idf from training and testing sets.

4- Calculation of the word embbeding vectors. 

5- Traininig of the baseline classifiers (Naive Bayes and Linear Classifier) on the data, using different types of the features . Prediction and calculation of accuracy and F1 score.

6- Train of the CNN model on the data, prediction and calculation of accuracy and F1 score. Then, comparison of results obtained using CNN with results obtained using baseline classifiers.

<h3>Requirements:</h3>
<li>Python 3.7</li>
<li>Run dependencies requirements.txt by using pip install -r requirements.txt (from command line) or !pip install -r requirements.txt (inside jupyternotebook)</li>
<li>JupyterNoteBook required</li>


<h4>Produce result</h4>
<strong>Table 3:</strong> Result comparison between FastText as text classifier and FastText as word embedding withCNN for AskFm base dataset.

<li>
	<ol><strong>FastText as classifier:</strong> implementation with AskFm dataset can be found by running fastext.ipynb. This file use ask_tain.txt as train datasets and ask_test.txt as test dataset.</ol>
	<ol>
<strong>FastText as wordembedding:</strong>  For testing this result askfm_not_extended.ipynb file require to run. This file use ask_fm_data.csv as train and test dataset.</ol>
</li>







*** This file require jupyter notebook to run.
Running Command for each cell in jupiter is: ctrl+enter
