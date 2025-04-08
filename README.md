# Rice vs Chips Image Classifier

**Image-Based Dish Classification: Rice vs Chips (MLEnD Yummy Dataset)**

This project aims to build an image classification system that identifies whether a given dish image contains rice or chips. The goal is to assist food-related applications in recognizing dish types based on visual attributes using traditional machine learning techniques and feature extraction.

## Dataset
MLEnD Yummy Dataset

Contains labeled food images with dish attributes

Labelled as:

0 → Chips

1 → Rice

Accessed via the download_yummy() function from the mlend module

## Machine Learning Pipeline

Stage	                         Description

1. Data Collection	           Mounted Google Drive to access the MLEnD dataset
   
2. Preprocessing	             Cleaned conflicting rows, created custom label column, removed irrelevant info
   
3. Feature Extraction	         Used yellow pixel component + GLCM (texture) features
   
4. Class Imbalance             Handling	Applied SMOTE to balance training data
   
5. Data Augmentation	         Applied transformations (random rotation, flip) for generalization
   
6. Model Training	             Trained a Decision Tree Classifier (tuned max_depth & min_samples_split)
   
7. Evaluation	                 Evaluated on both training & test sets using accuracy and confusion matrix
   
8. Random Testing	             Built a function to randomly select and predict dish types on unseen images

## Input & Output

Input: Raw image of a dish (chips or rice)

Output:

0 → Chips

1 → Rice


## Project Structure

```

Image-food-classifier\

├── Rice_Chips_Food_Image_classification.ipynb

├── README.md

```

## Model Performance

Training Accuracy:  0.7142857142857143

Test Accuracy: 0.6655405405405406

Confusion matrix used to interpret false positives/negatives

## Conclusion

-This project demonstrates the use of classical machine learning techniques for image-based dish classification using the MLEnD Yummy Dataset. While the model performs well overall, there are several areas for further enhancement:

-The dataset was imbalanced, and SMOTE was applied to address this. However, other techniques like undersampling or class-wise weighting could be explored.

-The model showed lower precision and recall for the “Chips” class, indicating room for improvement in feature extraction or data representation.

-Exploring alternative feature extraction methods beyond GLCM and color analysis could yield better performance.

-In addition to data augmentation, feature engineering could be applied to extract more meaningful patterns from the image data.

-Finally, testing other models such as Random Forest, SVM, or even lightweight CNN architectures may lead to improved classification accuracy.
