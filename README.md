Dataset Selected:

 The report's dataset is “Features data set.csv” whichwere retrieved from
 https://www.kaggle.com/manjeetsingh/retaildataset?select=Features+data+set.csv

 ![image](https://github.com/yeejing0822/AI_SVMKNN_FeaturesDataset/assets/86753374/2b87b62f-2652-4694-973e-2b669fa31e2d)

![image](https://github.com/yeejing0822/AI_SVMKNN_FeaturesDataset/assets/86753374/5da66e7c-0011-4d40-aabc-9a207a043fb9)

![image](https://github.com/yeejing0822/AI_SVMKNN_FeaturesDataset/assets/86753374/8d5aa609-8f93-4d8d-afe9-8cb68e3d2fbf)

Analysis and Justification:

 Support Vector Machine (SVM) is used in supervised learning to train and test the data set. The
 linear SVM classifier works by drawing a straight line between two classes. All the data points
 that fall on one side of the line will be labeled as one class and all the points that fall on the other
 side will be labeled as the second. It can also be called a linear classifier. There are some
 parameters needed to be manipulated to obtain the best result. The major parameters are C
 (penalty parameter of the error term), kernel, and gamma. The C parameter tells the SVM
 optimization how much you want to avoid misclassifying each training example. The
 optimization will choose a smaller-margin hyperplane for larger values of C and will get all the
 training points classified correctly if the hyperplane does a better job. The parameters used to fit
 the model were set to default. However, this could not obtain the best result. Thus, the Grid
 Search hyperparameter optimization technique was used to optimize the results. There are 5 folds
 being fitted for each 25 candidates and there are a total of 125 fits. The best parameters are
 obtained which are C = 1000, gamma = 0.01, and the kernel = rbf. The result of prediction was
 improved and the accuracy score was increased. The testing had been carried out 3 times to get
 the accuracy.
 
 Another training method that is used is K Nearest Neighbours (KNN). KNN is a simple
 algorithm that stores all the available cases and classifies the new data or case based on a
 similarity measure. It is mostly used to classify a data point based on how its neighbours are
 classified. The accuracy of the prediction can be affected by the value k which is the number of
 nearest neighbours. The best value of k will depend on the data. Larger k values can reduce the
 effect of the noise on the classification. However, this will make boundaries between classes less
 distinct. Besides, other parameters such as weights, algorithm, leaf_size, p, metric, and n-jobs
 also can affect the results of the training. In the training of the KNN model without using
 hyperparameter optimization technique, the parameters which will affect the results were set as
 default values. The k = 5, weights = uniform, algorithm = kd_tree, leaf_size = 30, p = 2, metric =
 minkowski, and n_jobs =-1 were used. However, the result was not the best result. Therefore,
 the Grid Search hyperparameter optimization technique was also used to manipulate to obtain the
 best model and result. In the Grid Search hyperparameter optimization technique, there 3 folds
 were fitted for each 20 candidates and there are a total of 60 fits. The best parameters were
obtained for the best prediction. The metric = manhattan, n_neighbors = 5, and weights =
 distance were obtained and used for the prediction in this lab. The accuracy score of the
 prediction has been increased by using these parameters for model fitting. The testing data also
 had been carried out 3 times.
 
 In this lab, the feature data set in the Retail Data Analytics was used to train and test. The
 data were split into 60% train and 40% test. Thus, the test size is set to be 0.4 and the random
 state was set to be 1. For the SVM, the accuracy score and the cross-validation accuracy before
 the hyperparameter are 0.3202 and 0.4084 (+/- 0.1143). While for the KNN, the accuracy score
 without using hyperparameters is 0.4926 and the cross-validation accuracy is 0.3538 (+/
0.2788). Due to these results not the maximum results in both models, the Grid Search technique
 was used to maximize the accuracy. After using the Grid Search technique to maximize the
 results, the accuracy score and cross-validation accuracy have been increased to 0.8030 and
 0.5586 (+/- 0.1143) for SVM model whereas 0.6305 and 0.4107 (+/- 0.2788) for KNN model.
 The accuracy score and cross-validation accuracy obtained from the SVM model is higher than
 the results obtained from KNN model. The processing time for the SVM model is 4.59s while for
 KNN model is 5.85s. The processing time for the SVM model is lower than the KNN model
 because KNN training methods are required to calculate the distance of each data. It involved
 finding the closest neighbor in the prediction. This will lower the speed of the prediction by
 KNN model. Thus, the time increased. The KNN model is also affected by the curse of
 dimensionality heavily.
 
 Moreover, precision is defined as how many of the correctly predicted events actually turned
 out to be positive. It is using the true positive value that divides the sum of true positive value
 and false positive value. Besides, the recall is defined as how many of the actual positive events
 are able to predict correctly in our model. It is using true positive value to divide the sum of true
 positive value and false negative value. When comparing these 2 classification models’ precision
 depends on weighted average, the best model is the support vector machine (SVM) which after
 hyperparameter optimization has the highest precision compared to K Nearest Neighbours model
 (KNN) which is 0.81 means 81% of the correctly predicted events had changed to be positive
 events. Besides, when comparing these 2 classification models’ recall depends on weighted
 average after hyperparameter optimization, the best model is the support vector machine (SVM)
which has the highest recall between the classification models which is 0.80 means 0.80% of the
 positives were predicted successfully by the model. In the nutshell, based on all of the analysis
 and justification above, it is obvious that the support vector machine (SVM) is a more accurate
 classification method for this data sample than the K Nearest Neighbours model (KNN)
