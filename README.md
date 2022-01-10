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

## Competition 2: Object Detection
### Description

In this competition, you have to train a model that recognizes objects in an image. Your goal is to output bounding boxes for objects.
Given an image(shape = [undefined, undefined, 3]), you need to output a list of bounding boxes (xmin, ymin, xmax, ymax, classlabel, confidencescore) for objects showed in image and its class.

### Evaluation

The evaluation metric for this competition is comparing your mean Average Precision on the different packs of testing data with the ground truth results(mean squared error). The ranking on the leaderboard is 50% of the testing packs. Your final score will be decided by the rest of 50% after the end of the competition.

There are two baseline results, Benchmark-60 and Benchmark-80. You have to outperform Benchmark-60 to get 60 points, and Benchmark-80 to get 80. Meanwhile, the lower point(error) you achieve, the higher the final score you will get.

## Competition 3: Reverse Image Caption
### Description

In this work, we are interested in translating text in the form of single-sentence human-written descriptions directly into image pixels. For example, "this flower has petals that are yellow and has a ruffled stamen" and "this pink and yellow flower has a beautiful yellow center with many stamens". You have to develop a novel deep architecture and GAN formulation to effectively translate visual concepts from characters to pixels.

More specifically, given a set of texts, your task is to generate suitable images with size 64x64x3 to illustrate each of the texts.

You will compete on the modified release of Oxford-102 flower dataset and its paired texts.

### Evaluation

In this competition, we use both inception score and cosine distance as our final score to evaluate quality and diversity of generated images. You can find more details about inception score in this article. The final score is based on:

* Similarity of images and the given contents. How similar are the generated images and the given texts?
* KL divergence of generated images. Are the generated images very diverse?<br>The ranking on the public leaderboard is about 50% of the testing packs. Your final score(private leaderboard) will be decided by the rest of 50% after the end of the competition.

There are two baseline results, Benchmark-60 and Benchmark-80. You have to outperform Benchmark-60 to get 60 points, and Benchmark-80 to get 80. Meanwhile, the lower point(error) you achieve, the higher the final score you will get.

## Competition 4:
### Description

In this work, we try to crack the unlearnable dataset which proposed by Neural Tangent Generalization Attacks (NTGA) ICML'21

Authors of NTGA propose the generalization attack, a new direction for poisoning attacks, where an attacker aims to modify training data in order to spoil the training process such that a trained network lacks generalizability. They devise Neural Tangent Generalization Attack (NTGA), a first efficient work enabling clean-label, black-box generalization attacks against Deep Neural Networks.

NTGA declines the generalization ability sharply, i.e. 99% -> 15%, 92% -> 33%, 99% -> 72% on MNIST, CIFAR10 and 2- class ImageNet, respectively.

### Evaluation

We will calculate categorizationaccuracy with true label!