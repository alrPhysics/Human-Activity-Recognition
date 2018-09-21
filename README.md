## Determine Activity Based on Data Collected From Smarthphone
### Data Info Summary
All details concerning this dataset can be found [here](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones).
* Data was collected using the embedded acclerometer and gyroscope of a Samsung Galaxy S II.
* Contains 561 features.
* Features are normalized between [-1,1].
* Data was donwloaded from the UCI Repository (link above) and the given training and test sets were used.
### Processing Data
* PCA was implemented to reduce the dimensionality of the data.
* The explained variance ration was plotted against the number of PCs in order to guide PC selection.  
* The first 10 PCs were visualized using Seaborn's pairplot in order to make predictions on classifier performance.
* Classifiers were trained on 10, 50, and 100 PCs.
### Classification
* Compared the performance of LinearDiscriminantAnalysis, LogisticRegression, MLPClassifier, and KNeighborsClassifier.
* Visualized the confusion matrices using Seaborn's heatmap.
* Attempted to optimize classifiers using GridSearchCV.
### Results
Top performers:
* 10 PCs - MLPClassifier with an accuracy of 87.4%
* 50 PCs - LogisticRegression with an accuracy of 92.6%
* 100 PCs - LogisticRegression with an accuracy of 95%
