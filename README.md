# Cluster-Classification-WebAttack
his repository demonstrates the use of K-Means clustering to identify patterns in web traffic data and then applies a Decision Tree classifier to predict potential web threats.

## Dataset ##
The dataset consists of web traffic interactions labeled as suspicious. It contains 16 columns, but only four features were selected for training both the K-Means and Decision Tree models.  The dataset used is from the kaggle website (https://www.kaggle.com/datasets/jancsg/cybersecurity-suspicious-web-threat-interactions).

## Data Preprocessing ##
Before training, some preprocessing steps were applied:
- Source IP modification: Only the first octet of the IP address was retained.
- Country code encoding: The source IP's country code was converted into numerical categories for model training.

## Clustering ##
The K-Means algorithm was used to group the data into clusters. The Elbow Method determined that three clusters provided the best separation.

Cluster visualizations, including centroid positions, were generated for analysis.

## Decision Tree ##
The dataset was split into 75% training and 25% testing subsets. A Decision Tree classifier was trained, achieving an accuracy of 100% on the test set.

## Considerations ##
- Generalization: The model should be tested on unseen data to evaluate its performance in real-world scenarios.
- Alternative Classifiers: Exploring other classification techniques (e.g., Random Forest or SVM ).

## Summary ##
This approach helps categorize web traffic into three distinct groups, which could indicate patterns associated with potential cyber threats. If new data falls into one of these clusters, it may suggest anomalous activity, aiding in early threat detection. However, further testing on unseen data is necessary to validate the model’s effectiveness in real-world cybersecurity applications.
