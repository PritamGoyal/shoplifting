# shoplifting
### Theft Detection Algorithm Report

#### 1. Data Preprocessing:
   - **Steps:** 
     - The data preprocessing involved copying video clips from the source directory to a destination directory for ease of access.
     - Each video clip was then loaded, and frames were extracted from each video.
     - Each frame was resized to a suitable size (224x224) and converted to grayscale to reduce computational complexity.
     - Histogram of Oriented Gradients (HOG) was used for feature extraction from the grayscale frames.
   - **Rationale:** 
     - Copying video clips to a separate directory made it easier to manage and access the data.
     - Resizing frames and converting them to grayscale reduced the dimensionality of the data while retaining essential information.
     - HOG was chosen for feature extraction due to its effectiveness in capturing shape and texture information, which are relevant for identifying shoplifting activities.

#### 2. Feature Engineering:
   - **Methods:** 
     - Histogram of Oriented Gradients (HOG) was used to extract features from each frame.
     - HOG computes the distribution of gradient orientations in localized portions of an image, which helps in capturing shape and texture information.
   - **Effectiveness:** 
     - HOG features proved to be effective in capturing discriminative information for identifying shoplifting activities.
     - The extracted features provided meaningful representations of the video content, allowing the machine learning model to differentiate between shoplifting and non-shoplifting instances.

#### 3. Model Selection:
   - **Selected Model:** 
     - A Support Vector Machine (SVM) classifier with a linear kernel was selected for the theft detection task.
   - **Justification:** 
     - SVMs are known for their effectiveness in binary classification tasks and have been widely used in similar applications.
     - The linear kernel was chosen for its simplicity and interpretability, making it suitable for our relatively small dataset.
   - **Hyperparameter Tuning:** 
     - No hyperparameter tuning was performed in this case, as the default parameters provided satisfactory results.

#### 4. Evaluation Results:
   - **Accuracy:** 
     - The SVM classifier achieved an accuracy of approximately 93.33% on the testing set.
   - **Precision:** 
     - The precision of the classifier, which measures the ratio of true positive predictions to total positive predictions, was approximately 92.86%.
   - **Recall:** 
     - The recall of the classifier, which measures the ratio of true positives to actual shoplifting instances in the dataset, was approximately 72.22%.
   - **F1 Score:** 
     - The F1 score, which is the harmonic mean of precision and recall, was approximately 81.25%.
   - **Confusion Matrix:** 
     - The confusion matrix provides a detailed breakdown of the classifier's performance, showing the number of true positives, true negatives, false positives, and false negatives.
       
