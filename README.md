# DS4002_Project_1
## Table of Contents
1. Software and Platform  
2. Documentation Map  
3. Instructions for Reproduction  

## Software and Platform
Softwares used: Google Collab and Python  
Add-ons: pandas, numpy, matplotlib.pyplot, seaborn, scikit-learn, joblib    
Platform: Windows
## Documentation Map
<img width="1067" height="1004" alt="Documentation Map" src="https://github.com/user-attachments/assets/d63e4792-510c-4072-bd9b-41373e578e12" />

## Instructions for Reproduction
1. Follow link found in DATA/accessing_raw_data and download csv.  
*Note: Steps 2-6 can be accomplished by running 1_Data_Set_Cleaning_&_EDA_Script.ipynb with the downloaded csv.*  
2. Using python, create a dataframe from the csv information. Drop all instances of Nan.
3. Separate genres for books with multiple genres listed.
4. Identify target genres and genres which should be merged.
5. Map new genres to the ones being replaced/merged.
6. Create new dataframe from cleaned data and download as csv. This csv is "cleaned_book_data.csv"  
*Note: Steps 7-14 can be accomplished by running "2_Train_Model.ipynb" on "cleaned_book_data.csv".*  
7. Import required libraries and identify desired output directories.
8. Load data and group columns into text (title and synopsis) and genre. Split genres within the column by commas.
9. Set random seed to 42. Create an 80/20 train/test split, set cross-validation folds to 5, set probability cutoff at 50%, filter out genres with fewer than 20 books.
10. Change each book's genre list into binary target matrix with one column for each genre.
11. Perform train/test split stratified by rarest genre so that all genres are represented in both the train and test group.
12. Perform 5-fold cross validation over a TD-IDF and logistic regression pipeline.
13. Predict genre probabilities for test set and apply probability cutoff.
14. Export trained components, raw test scores, cross-validation logs, test predictions, and summary metrics.  
*Note: Steps 15-19 can be accomplished by running "3_Evaluate_&_Plot.ipynb"*  
15. Import products from training script.
16. Calculate F1 score for each genre. Calculate model accuracy for a baseline (guessing most common genre), exact match, hit-rate, and top-3 hit rate.
17. Plot F1 scores and accuracy rates.
18. Identify and plot model's top genre prediction vs. true genre. 
19. Identify words that most strongly predict a genre and plot in a bar chart. 
