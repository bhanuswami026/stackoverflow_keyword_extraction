# stackoverflow_keyword_extraction

### DESCRIPTION:
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

### EVALUATION:
The evaluation metric is  Mean F1-Score.  The F1 score, commonly used in information retrieval, measures accuracy using the statistics precision p and recall r. Precision is the ratio of true positives (tp) to all predicted positives (tp + fp). Recall is the ratio of true positives to all actual positives (tp + fn).


The evaluation metric for this competition is Mean F1-Score.  The F1 score, commonly used in information retrieval, measures accuracy using the statistics precision p and recall r. Precision is the ratio of true positives (tp) to all predicted positives (tp + fp). Recall is the ratio of true positives to all actual positives (tp + fn). The F1 score is given by:


The F1 metric weights recall and precision equally, and a good retrieval algorithm will maximize both precision and recall simultaneously. Thus, moderately good performance on both will be favored over extremely good performance on one and poor performance on the other.

To receive credit, the tag you predict must be an exact match, regardless of whether you believe the tags are synonyms.  Why aren't synonyms counted?

Giving out a list of candidate synonyms is a potential source of leakage
Synonyms are subjective, and there are "subjectively many" synonyms for a given tag
Participants are equally penalized for predicting a synonym of a correct tag, so the task can be framed as not only predicting a tag, but also modeling the distribution(s) of potential synonyms
