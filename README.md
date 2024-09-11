### ImageClassifier

**Scott Allred**

#### Executive summary
This image classifier detects failed wafers with very good accuracy.
#### Rationale
Automated review of images is laborious and slow. This script will scan a destination folder and provide a report of any wafers flagged as failing, allowing actionable insights in near real time.
#### Research Question
Detect and classify the presence of anomalies on the backside of silicon wafers in a semiconductor fab.
#### Data Sources
Images are collected from a 15 MP camera, and manually labeled as "PASS" or "FAIL" for the model training.
#### Methodology
I will use SVC and logistic regression classifiers to determine the best method to classify these images.
#### Results
Both models had outstanding accuracy. Logitics regression took far longer to fit, thus SVC is the ideal model. Accuracy on the limited training set was very high; the confusion matrix reflected no errors
#### Next steps
I recommend expanding the training set and testing out a CNN for this application.

#### Outline of project

- [Link to notebook 1]()


##### Contact and Further Information
scottyallred1@gmail.com
