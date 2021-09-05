# stackoverflow_keyword_extraction

### DESCRIPTION:
Stack Overflow is the largest, most trusted online community for developers to learn, share their programming knowledge, and build their careers.

Stack Overflow is something which every programmer use one way or another. Each month, over 50 million developers come to Stack Overflow to learn, share their knowledge, and build their careers. It features questions and answers on a wide range of topics in computer programming. The website serves as a platform for users to ask and answer questions, and, through membership and active participation, to vote questions and answers up or down and edit questions and answers in a fashion similar to a wiki or Digg. As of April 2014 Stack Overflow has over 4,000,000 registered users, and it exceeded 10,000,000 questions in late August 2015. Based on the type of tags assigned to questions, the top eight most discussed topics on the site are: Java, JavaScript, C#, PHP, Android, jQuery, Python and HTML.

### PROBLEM STATEMENT
The task is to predict the tags (a.k.a. keywords, topics, summaries), given only the question text and its title. The dataset contains content from disparate stack exchange sites, containing a mix of both technical and non-technical questions.
 
 ### DATA DESCRIPTION:
 All of the data is in 2 files: Train and Test.

Train.csv contains 4 columns: Id,Title,Body,Tags

Id - Unique identifier for each question
Title - The question's title
Body - The body of the question
Tags - The tags associated with the question (all lowercase, should not contain tabs '\t' or ampersands '&')
Test.csv contains the same columns but without the Tags, which you are to predict.

The questions are randomized and contains a mix of verbose text sites as well as sites related to math and programming. The number of questions from each site may vary, and no filtering has been performed on the questions (such as closed questions).

#### DOWNLOAD DATA FROM:
Source: https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/data

### EVALUATION:
The evaluation metric is  Mean F1-Score.  The F1 score, commonly used in information retrieval, measures accuracy using the statistics precision p and recall r. Precision is the ratio of true positives (tp) to all predicted positives (tp + fp). Recall is the ratio of true positives to all actual positives (tp + fn).


The evaluation metric for this competition is Mean F1-Score.  The F1 score, commonly used in information retrieval, measures accuracy using the statistics precision p and recall r. Precision is the ratio of true positives (tp) to all predicted positives (tp + fp). Recall is the ratio of true positives to all actual positives (tp + fn). The F1 score is given by:


The F1 metric weights recall and precision equally, and a good retrieval algorithm will maximize both precision and recall simultaneously. Thus, moderately good performance on both will be favored over extremely good performance on one and poor performance on the other.

To receive credit, the tag you predict must be an exact match, regardless of whether you believe the tags are synonyms.  Why aren't synonyms counted?

Giving out a list of candidate synonyms is a potential source of leakage
Synonyms are subjective, and there are "subjectively many" synonyms for a given tag
Participants are equally penalized for predicting a synonym of a correct tag, so the task can be framed as not only predicting a tag, but also modeling the distribution(s) of potential synonyms

### EXTRA RESOURCES:
Research paper : https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/tagging-1.pdf
Research paper : https://dl.acm.org/citation.cfm?id=2660970&dl=ACM&coll=DL

### COMMENTS:
It is a multi-label classification problem.
Predict as many tags as possible with high precision and recall.
Accuracy matters more because incorrect tags could impact customer experience on StackOverflow.
No strict latency constraints.
