# Spotify_Data_Analysis
This is the link to see the Rpubs page:

https://rpubs.com/evabeyebach/1125086

I have developed an analysis comparing different classification and regression models to **predict wether a song is going to be popular or not.**

### Introduction
* The data shows  general metadata around songs from Spotify's API. It shows the song's popularity and other parameters such as acousticness, danceability, energy, speechiness, valence, key, genres and subgenres...

* We want to answer the question:
* What characteristics of a song can determine its popularity?
* Which genres and subgenres predict usually the most popular songs?

### Data Preparation

* We will examine our data doing the following:
* look ad duplicates
* look at missing values
* data types
* summary statistics 

### Exploratory Data Analysis

* Different ways that we could look at the Data to answer our questions could be **histograms**, to learn about the distribution of variables
* **boxplots**, to find outliers and see which genres are most popular
* **scatterplots** to interpret the variables based on `track_popularity` and **correlation matrix** to find out the correlation between variables.

### Modelling

* The plan is to analyze relationship between popularity and different features of the song to predict future popularity of a song with data modelling. We plan on using models such as **linear regression**, **knn**, **logistic regression**, **SVM** and **Tree Models** and compare which one performs better and see which one predicts better if a song is going to be popular or not.

### Conclusion

From the visualizations and the models we saw that:

* The Models had different variables but we can agree on `instrumentallness`, `speechiness` and `liveness` being the variables that best predict `track_popularity`.
* `Loudness` and `Energy` were not the best predictors as one would think.
* From visualizations and models, all agreed that `pop` predicted popularity the most.
* `dance pop` was the best predictor as far as subgenre.

From **Data Modeling** we concluded the following:

* In **LM** only `key` was the only varaibled that did not predict popularity.
* **OUT-Of Sample MSE** was the best in the model with categorical values (485.8) when comparing LM to Knn and improved when adding an interaction.
* The R^2 was still to low for it to be a good model.

When comparing **Trees** , **SVM** and **logistic**:
* **SVM** third model had the best AUC in training (0.715), but the weights are very distributed to 1 and this model is not easy to interpret visually.
* **Logistic Regression** was the best model for this dataset because its AUC was high and Mr not too low.
* **Logistic Regression** is better than **SVM** becasue we did not have to distribute any weights and the coefficients and estimates are interpretable.

Our predictions before doing modelling were that **lm** and **Classification Tree** would be the best models.
However **Logistic Regression** performed better than **Tree**, and we did not have to put in in any weights. **Lm** had a too high **MSE** and **R^2** for it to be a good model. 
* Therefore **Regression Tree** is the best model for this dataset. 











