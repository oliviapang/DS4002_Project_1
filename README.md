# DS4002_Project_1
## Table of Contents
1. Software and Platform  
2. Documentation Map  
3. Instructions for Reproduction  

## Software and Platform
Softwares used: Google Collab and Python 3.13.15    
Add-ons: pandas 2.2.3, numpy 2.1.3, matplotlib.pyplot 3.10.0, seaborn 0.13.2, scikit-learn 1.6.1, joblib 1.6.0    
Platform: Windows
## Documentation Map
<img width="1056" height="1004" alt="Documentation Map (1)" src="https://github.com/user-attachments/assets/41857ac5-452f-401f-836f-b1bc53cdfa5f" />

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

## References
[1] D. Bamman and N. Smith. “New Alignment Methods for Discriminative Book Summarization,” Carnegie Mellon University. https://doi.org/10.48550/arXiv.1305.1319   
[2] A. S. Fazira and E. W. Pamungkas, "Book genre classification based on titles and synopses using machine learning," in 2026 International Conference on Smart Computing, IoT, and Machine Learning (SIML), Surakarta, Indonesia, 2026, pp. 1–6, doi: 10.1109/SIML69834.2026.11621421.  
[3] S. Nadis, "New book-sorting algorithm almost reaches perfection," Wired, Feb. 20, 2025. Available: https://www.wired.com/story/new-book-sorting-algorithm-almost-reaches-perfection/   
