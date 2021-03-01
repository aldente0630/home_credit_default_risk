# Automated Feature Engineering with *FeatureTools*
* The goal is to do automated feature engineering with [FeatureTools](https://www.featuretools.com).
* A dataset of Kaggle Competition, [Home Credit Default Risk](https://www.kaggle.com/c/home-credit-default-risk/overview/description) was downloaded for testing. The dataset consists of 4 tables, and the relationship diagram is as follows. Various derived variables could be created automatically using *FeatureTools*.
* I referenced [Will Koehrsen's post](https://towardsdatascience.com/automated-feature-engineering-in-python-99baf11cc219 ) and [his code on Kaggle](https://www.kaggle.com/willkoehrsen/feature-engineering-using-feature-tools).
  
![Relationship Diagram](https://aldente0630.github.io/assets/home_credit.png)  

* A dataset with 2,221 features for 356,255 customers was finally created. Saved as a CSV file, it is about 4GB.
* The whole process took 3 hours and a half on my iMac with 6 cores and 16GB of memory.

# Automated Modeling with *autogluon*
* The goal is to do automated modeling with [AutoGluon](https://auto.gluon.ai/stable/index.html#). 
* *AutoGluon* makes it easy to automatically experiment with a variety of algorithms, from tree ensembles to deep learning and even model stacking.


* The model stacking technique achieved the highest predictive performance. This was 0.78149 for the Kaggle public board and 0.78391 for the private board as measured by AUROC.
* This process took about 1 day and 6 hours to train using 64 cores and 256GB of memory on an AWS m4.16xlarge EC2 instance, and about an hour and a half to infer.
