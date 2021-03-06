# CSE408-Twitter-Sentiment-Analysis

A repo for our project in explainable twitter sentimental analysis. For more information, please visit https://www.kaggle.com/kazanova/sentiment140.

## Instruction of running code
  1. In order to run the code, please use google colab plateform, change the code "df = pd.read_csv("/content/drive/MyDrive/CSE 408/Data/training.csv", encoding =DATASET_ENCODING , names=DATASET_COLUMNS)" to the filepath which you put training.csv on. All the download needed package are in command lines in jupyter notebook.
  2. Since Github has issue to show the ipynb file here, please download the sentimentAnalysis.ipynb file to your local computer, then upload to github to test the code. 
  
## Implementation Details
  1. We use the famous benchmark sentiment140 datasets which contains 1.6 millions tweets, the tweets are labeled either positive or negative sentiment. See the data foler training.zip file to extract the csv dataset file. The datasets are balanced which means it contains 800000 positive tweets and negative tweets and no missing values, the team also replace the target “0”, “4” to “NEGATIVE” and “POSITIVE”. 
  
  2. After we remove the stop words, special symbols, and transfer all strings to lowercase, we did the Exploratory Data Analysis(EDA) work for the whole datasets, we plot the Word Cloud for positive and negative tweets, we also plot the frequency of most common word in positive and negative tweets, finally, we plot the distribution of words for the tweets texts.
  
  3. Due to the machine limited, we will use 25000 tweets as training dataset and 3000 tweets as testing datasets instead of splitting 1.6 millions. For the training dataset, we use nlpaug and textattack data augmentation technologies, we use the SynonymAug to generate 5000 similar texts and merge them into training dataset, the goal is to generate more sentiment words to avoid overfitting problems.
 
  4. We develop Deep Learning model by fine tuning hyperparameters from existing state-of-art model architectures(LSTM).
  
## References
  1. Nlpaug: https://nlpaug.readthedocs.io/en/latest/
  2. TextAttack: https://textattack.readthedocs.io/en/latest/
  3. Kaggle Twitter Sentiment Analysis: https://www.kaggle.com/paoloripamonti/twitter-sentiment-analysis/output
  4. Twitter Feature Extraction: https://www.kaggle.com/tanulsingh077/twitter-sentiment-extaction-analysis-eda-and-model/data
  5. Model Training LSTM: https://www.kaggle.com/arunrk7/nlp-beginner-text-classification-using-lstm


