### ImageClassifier

**Scott Allred**

#### Executive summary
The intent of this model is to automate a manual inspection in a semiconductor environment. Wafers experience a variety of conditions across the hundreds of steps in there fabriction. The focus of this script is to process and flag defects on the backside of wafers, which is tracked much less robustly than the frontside.
#### Rationale
Manual review of images is time consuming and a poor use of engineering resources. This script will monitor the destination folder of an image capture system and determine whether any backside defects are present rapidly after this scan. On a single day, thousands of images can be collected, and the subsequent manual review results in many images that either aren't reviewed promptly or aren't reviewed at all.   
#### Research Question
Use machine learnign for image classification to detect the presence of anomalies on the backside of silicon wafers in a semiconductor fab.
#### Data Sources
Images are collected from an automated, high-speed image capture system. For the train/test images, I've manually labeled the images as either "PASS" or "FAIL". The number of examples of FAIL data is very low (rare to have defects) thus I used the Augmentor library to generate more images for training. To simplify the image processing. To reduce the amount of redundant data processed, I used CV2 library to reduce the images to a small circle in the center of the wafers. This region is where the defects are present, the outer region does not contain valuable diagnostic information for the model.
#### Methodology
I fit a variety of models including: SVC, logistic regression, random forest, and then ensemble methods with SVC, gradient boost and voting classifiers. 
#### Results
All models had very high accuracy (99% or better). While I recognize this indicates overfitting, 
#### Next steps
I recommend expanding the training set and testing out a CNN for this application.

#### Outline of project

- [Link to notebook 1]()


##### Contact and Further Information
scottyallred1@gmail.com
