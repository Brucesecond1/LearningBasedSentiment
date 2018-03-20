# LearningBasedSentiment
**Sentiment Classifier** based on traditional Maching learning methods, eg. Bayes, SVM ,DecisionTree, KNN and Deeplearning method like MLP, CNN, RNN(LSTM).

## Requirements
All code in this project is implemented in [Python3.6+](https://www.python.org/downloads/).  
And all the essential packages are listed in `requirements.txt`, you can install them by 
`pip install -r requirements.txt -i https://pypi.douban.com/simple/`  
[Anaconda](https://docs.anaconda.com/anaconda/) or [virtualenv + virtualenvwrapper](http://www.jianshu.com/p/44ab75fbaef2) are strongly recommended to manage your Python environments.

# 预处理
1、语料  
电影评论，训练集合20000（正向10000，负向10000）  
电影评论，测试集合20000（正向3000，负向3000）  
2、语料处理  
使用jieba进行分词  
3、输入向量化  
使用预先训练的wordvector.bin文件进行向量化  
对于传统机器学习算法，要求输入的是N维向量， 采用句子向量求和平均  
对于CNN，RNN深度学习算法，要求输入的是N*M维向量，分别对应查找并生成向量  

# 训练与对比（准确率）

| Algorithm | Accuracy |
| --- | --- |
| DecisionTree | 0.6907302434144715 |
| Bayes | 0.7437479159719906 |
| KNN | (n=14)0.7909303101033678 |
| SVM | 0.8302767589196399 |
| MLP | (20epoches) 0.8359 |
| CNN | (20epoches) 0.8376 |
| LSTM | (20epoches) 0.8505 |
