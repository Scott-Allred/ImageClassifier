### ImageClassifier

**Scott Allred**

#### Executive Summary
This model automates the manual inspection process in a semiconductor environment. Wafers undergo various conditions across hundreds of fabrication steps. This script focuses on detecting and flagging defects on the backside of wafers, which is less rigorously monitored compared to the frontside.

#### Rationale
Manual image review is time-consuming and inefficient for engineering resources. This script monitors the destination folder of an image capture system and quickly identifies any backside defects. Thousands of images can be collected daily, and manual review often results in delays or missed inspections.

#### Research Question
Can machine learning be used for image classification to detect anomalies on the backside of silicon wafers in a semiconductor fab?

#### Data Sources
Images are collected from an automated, high-speed image capture system. For training and testing, images are manually labeled as "PASS" or "FAIL." Due to the rarity of defects, the Augmentor library was used to increase the number of "FAIL" images from 18 to 250. The CV2 library was used to focus on the central circular region of the wafers, where defects are typically found, excluding the outer regions that do not provide valuable diagnostic information.

#### Methodology
Various models were tested, including SVC, logistic regression, random forest, and ensemble methods with SVC, gradient boost, and voting classifiers.

#### Results
All models achieved high accuracy, F1 scores, and recall (>98%). Although this suggests potential overfitting, the significant contrast between "PASS" and "FAIL" images supports the results. The average, normalized distributions of pixel values for each class were plotted. The pixel value bins represent the intensity distribution of the grayscale images, with 0.7 indicating higher intensity (lighter pixels) and 0.1 indicating darker pixels. The difference between "PASS" and "FAIL" histograms showed that "FAIL" images have more darker pixels.

#### Next Steps
The model has been applied to a directory containing 30,000 real images, detecting 82 defective images. This model will be implemented to scan images as they are collected, and will benefit the business in the following ways:
1. Identifying wafer defects without manual review.
2. Aiding in rapid root cause analysis and near real-time process monitoring.
3. Saving hundreds of engineering hours annually.
4. Increasing yields.

#### Outline of Project
- Link to notebook 1

##### Contact and Further Information
scottyallred1@gmail.com
