# DSCI100-individual-Planning-Stage
Data Science Project: Planning Stage (Individual)

Author: Xiaohan An

Course:DSCI_V 100 

Instructor:Eugenia Yu

Last Edit Date: 2025/11/11

This repository contains my individual planning report for the DSCI 100 project.  

# Introduction:

The project explores if a player’s experience level, playtime, and age are related to whether they would love to subscribe game-related news with ggplot graph, and classification prediction.


# Commit 1: Data Import and Inspection

The data "players.csv" contains many observations and 7 variables describing player experience, age, gender, and subscription status.After importing the data using read_csv(), I tried to make it better with function glimpse() and summary(). Changing the missing numbers to NA. And I did a deeper organizing to make the variables "experience", "gender", and "subscribe" converted into factors for classification.

# Commit 2: Data Summary and Exploration

Descriptive statistics showed that the average player age was about 21 years (SD = 7.4).In addition, the mean playtime was around 5.85 hours, though it ranged widely and may come up to 223 hours. For experience, there are 3 types, which is new players, normal and pro. By using count() and summarise().I found that subscribers played longer on average than non-subscribers. So this tells us that playtime and experience and growth can influence if they want to subscribe or not. People around 21, with longer playtime and pro subscribe more often.

# Commit 3 : Visualization

In this part, by using ggplot2, which provides me a clear view to have a look at the informations, I find out the relationships with different variables. Histogram of "played hours" showed that most players spent little time on the server. The bar plot shows that players with higher experience levels were more likely to subscribe. In addition，boxplots compares playtime and age by subscription status shows that subscribers are willing to play longer time and are a little bit older.

# Commit 4: Classficaiton 

I use classfication model. The dataset was split into 80% training and 20% testing with initial_split(). And for controlling the reproducibility. I use set.seed(2025) (I use this one becasue it's year 2025). For the detail part, I use recipe for helping me build the connection with the variables. I use Five-fold cross-validation and use nearest_neighbor for prediction. In addition, the result shows an accuracy of around 74%.

# Commit 5: Final Evaluation

For a better accuracy, I did the final evaluation, and fit. The model provides me an accuracy of 72.5%. To get this answer, I predicts about three-quarters of players’ subscription outcome. This one ensures my guess that experience, age and playtime has a highly effect on the subscription. But I found there are some problems with my method, which is I can't predict motivations. However, with the given information, we can still konw that people with higher experience, age around 20 and longer playtime are more likely to subscribe.

