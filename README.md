# Playstore-App-Review-Analysis

## ♦ Abstract

Thousands of new applications are regularly added to the Google Play Store, with designers worldwide striving for success. In this competitive landscape, developers need to ensure they are on the right track. However, the revenue model for most Play Store apps, which rely on in-app purchases, ads, and subscriptions, remains uncertain. Therefore, an app's success is typically measured by its number of installations and user ratings rather than generated revenue. The goal of this experiment is to gain insights into customer demands, aiding developers in promoting their products. We aim to uncover relationships between attributes such as app pricing, user reviews, and ratings.


![gplay](https://cdn.dribbble.com/users/1726289/screenshots/3602725/google-play-animated-game-icon.gif)

## ♦ Introduction

In the current scenario, mobile apps have become integral to individuals' lives worldwide. Given the intense global competition, it is crucial for designers to ensure they are on the right track. To maintain their market position and revenue, application designers must learn how to sustain their current standing. To analyze the Android market, we have access to a dataset containing 10,000 Play Store applications. This dataset allows us to examine various categories such as family, communication, entertainment, tools, music, and camera apps. The objective of this project is to explore the different attributes present in the dataset that impact an application's popularity. We aim to address questions such as the factors that contribute to app popularity, optimal pricing and app size considerations, and any trends in user sentiments. Our dataset consists of two CSV files for data analysis: Play Store data and User Reviews. The Play Store data contains 10,841 rows and 13 columns, while the User Reviews data consists of 64,295 rows and 5 columns. Our focus is to extract maximum insights from the data to analyze the most preferred app types and draw comparisons among different factors. Our ultimate goal is to filter the data and create relevant plots for a comprehensive exploratory data analysis (EDA) that reveals the key factors responsible for app engagement and success.

## ♦  Contents of Datasets 

## Playstore- Data 

App: It contains the name of the app with  description

Category: Category to which an app belongs. In this dataset, the apps are divided among 33 categories.

Size: The disk space required to install the respective app.

Rating: The average rating given by the users for the respective app (between 1 and 5).

Reviews: The number of users who gave a review for the respective app.

Installs: The approximate number of times the respective app was installed.

Type: It states whether an app is free to use or paid.

Price: It gives the price payable to install the app

Content rating: It states which age group is suitable for the content of the respective app.

Genres: It gives the app genre(s)

Last updated: It gives the day in which the latest update for the respective app was released.

Current Ver: It gives the current version of the app.

Android Ver: It gives the android version of the app.

## User-Review 

App: It contains the name of the app with a short description (optional).

Translated_Review: It contains the English translation of the review dropped by the user of the app.

Sentiment: It gives the attitude/emotion of the writer. It can be ‘Positive’, ‘Negative’, or ‘Neutral’.

Sentiment_Polarity: It gives the polarity of the review. Its range is [-1,1], where 1 means ‘Positive statement’ and -1 means a ‘Negative statement’.

Sentiment_Subjectivity: This value gives how close a reviewer’s opinion is to the opinion of the general public. Its range is [0,1]. Higher the subjectivity, 
closer is the reviewer’s opinion to the opinion of the general public, and lower subjectivity indicates the review is more of a factual information.


## ♦ Data Preprocessing 

♦ Data cleaning, Handling the error, duplicate and NaN values in the dataset done using statistical aproach.

♦ 13.60% of reviews were NaN values, and even after merging both the dataframes, we could not infer much in order to fill them.so we drop them.

♦ The merged data frame of both play store and user reviews, had only 816 common apps.This is just 10% of the cleaned data, we could have given more valuable analysis, if we had atleast 70% - 80% of the data available in the merged dataframes.

♦ User Reviews had 42% of NaN values, which could have been used for developing an understanding of the category wise sentiments, which would help us to fill 13.60% NaN values of the Reviews column.

♦ From data frame, we can see that all the columns except rating have the object data type but some of the columns like, reviews, size, installs and price have the numerical value. So, we have to transform them in proper data type and also remove the unwanted values from the numerical columns like ‘+’ and ‘,’ from installs and ‘$’ from price

♦ In the size column we have some values in KB and some values in MB, so we transform all the values in MB



## ♦ EDA And Visualizations

♦ Plotting bar chart for  App category and the total number of apps which fall into that category

♦ Plotting bar chart for App Category vs Number of Installs

♦ Histogram for Average Rating

♦ Visualize the relation between Size and Ratings using jointplot

♦ Visualize the relation between Price and Rating of the App using Jointplot

♦ Pie chart for popularity of Paid Apps vs Free Apps

♦ The Sentiment Polarity Distribution for Free and Paid apps



## Insights 

1 - Most popular app in the Play Store based on the number of reviews: Facebook 

2 - The median size of all apps in the play store is 12 MB.

3 - The apps whose size varies with device has the highest number average app installs.

4 - Category with  highest number of installation: Game

5- There are 20 free apps that have been installed over a billion times

6 - Category with the highest average app installs: Communication

7 - Percentage of apps that are top rated = 80%

8 - Category for paid apps which have the highest average installation fee: Finance

9 - Highest number of positive reviews =  Helix Jump

10 = Highest number of negative reviews = Angry Birds Classic

11 - Free apps = 92%

12 - Top Rated = 80%

13 - Apps with no age restrictions = 82%

14 - Most competitive category  = Family



