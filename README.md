# Deep-Learning-Course-Team-Project
## Competition 1: Predicting News Popularity
### Description
In this competition, you are provided with a supervised dataset X consisting of the raw content of news articles and the binary popularity (where 1 means "popular" and -1 not, calculated based on the number of shares in online social networking services) of these articles as labels. Your goal is to learn a function f from X that is able to predict the popularity of an unseen news article.

This is the first competition for course CS565500 at NTHU in Taiwan.
### Evaluation
The evaluation metric is Area Under ROC. You can calculate AUC by sklearn.metrics:
<pre><code>from sklearn.metrics import roc_auc_score
auc = roc_auc_score(y_true, y_pred)
</code></pre>

The ranking shown on the leaderboard before the end of competition reflects only the AUC performance over part of test.csv. However, this is not how we evaluate your final scores. After the competition, we calculate AUC over the entire test.csv and report the final ranking thereby.

There will be two baseline results, namely, Benchmark-60 and Benchmark-80. You have to outperform Benchmark-60 to get 60 points, and Benchmark-80 to get 80. Meanwhile, the higher AUC you achieve, the higher the final score you will get.

#### Submission Format
For every news in the test.csv, submission files should contain two columns: Id and Popularity. The field Popularity is double value between [0,1] indicating the probability of news being popular.
<pre><code>Id Popularity
0    0.9
1    0.4
2    0.7
3    0.1
</code></pre>

## Competition 2:

## Competition 3:

## Competition 4:
