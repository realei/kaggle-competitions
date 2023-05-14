Here it is found that, in both *Training* and *Test* datasets:

1. The size of Training dataset is 7613, while the Test dataset is 3263

2. About the missing value:

    * 0.8% of `keyword` is missing in both training and test set
    
    * 33% of `location` is missing in both training and test set

  Conclusion:

    * 1/3 of the `location` is missing, whild only 0.8% of the `keyword` is missing
    
    * Train and test dataset most probably taken from the same sample, the ratio of missing values in both are almost the same
    
4. The Cardinality：

    * Unique numbers of keywords in both training and test dataset are 222, and it is a small portion of the dataset
    
    * Unique numbers of Location is training dataset is: 3342, the test dataset is 1603, there are only 423 common unique `location` in both datasets
    
  Conclusion:
  
    * Locations are not automatically generated, they are user inputs. That's why location is very dirty and there are too many unique values in it. It shouldn't be used as a feature.

    * Fortunately, there is signal in keyword because some of those words can only be used in one context. Keywords have very different tweet counts and target means. keyword can be used as a feature by itself or as a word added to the text. Every single keyword in training set exists in test set. If training and test set are from the same sample, it is also possible to use target encoding on keyword.

