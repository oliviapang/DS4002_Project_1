## Metadata
### Data Summary
The dataset used to train and test our model is contained in a csv file with the title, genre, and synopsis of 10,000 books. The file can be found by going to "accessing_raw_data". In some cases, the genre column contains more than one genre, and the synopsis column contains full paragraphs of text.
### Provenance
The information in this dataset was originally scraped from Wikipedia articles for a study done by researchers at Carnegie Mellon University [1]. Their text file contains titles, authors, genres, publication dates, and synopses for each book. We used this information but pared it down to just what is necessary for our project: title, genre, and synopsis. Google Gemini was used to help parse the data and organize it into a csv.
### License
The information in this dataset comes from Wikipedia, so it is available under the Creative Commons Attribution-ShareAlike 4.0 International License. This allows users to copy or modify the content as long as its authors are acknowledged and the modified version is available to the public under the same terms as the original content.
### Data Dictionary
| Variable | Type | Description |
|:---:|:---:|:---:|
Title | Text | Title of the book
Genre | Text | Book genre; there are 203 genres listed
Synopsis | Text | Synposis of the book
### Explanatory Plots
<img width="598" height="548" alt="image" src="https://github.com/user-attachments/assets/0348b0f2-001e-489e-ab44-60dd33dd1de0" />

<img width="1060" height="979" alt="image" src="https://github.com/user-attachments/assets/a379a91d-cffe-433d-b5f3-ecf8e2bf0a29" />

### References
[1] D. Bamman and N. Smith. “New Alignment Methods for Discriminative Book Summarization,” Carnegie Mellon University. https://doi.org/10.48550/arXiv.1305.1319 
