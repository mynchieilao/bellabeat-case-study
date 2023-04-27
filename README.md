# CASE STUDY 2: Bellabeat Fitness Capstone Project
#### Author: Mynchie Ilao
#### Date: September 27, 2022

Datasets used are listed below:
* https://www.kaggle.com/datasets/arashnic/fitbit

## Introduction
Bellabeat is a high-tech manufacturer of health-focused products for women. It was founded by Urška Sršen and Sando Mur in 2013 and focuses on 5 products: Bellabeat app, Leaf, Time, Spring and Bellabeat membership. Bellabeat is a small but successful company, with the potential to become a larger player in the global smart device market. Our team was asked to analyze smart device data to gain insight on how consumers use their smart devices. It will reveal any trends which could be applied to Bellabeat’s marketing strategy.

## This case study follows the data analysis process in 6 steps:

### 1. Ask
### 2. Prepare
### 3. Process
### 4. Analyze
### 5. Share
### 6. Act



## 1. Ask
Analyze Fitbit data to gain insight and help guide marketing strategy for Bellabeat to grow as a global player.

Primary stakeholders: Urška Sršen and Sando Mur, executive team members.

Secondary stakeholders: Bellabeat marketing analytics team.

## 2. Prepare

Data Source: 30 participants FitBit Fitness Tracker Data from Mobius: https://www.kaggle.com/arashnic/fitbit

This Kaggle data set contains personal fitness tracker from thirty fitbit users. Thirty eligible Fitbit users consented to the submission of personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring. It includes information about daily activity, steps, and heart rate that can be used to explore users’ habits. The dataset has 18 CSV and also follows a ROCCC approach:

Reliability: The sample size is small with just over 30 participants which has questions around potential bias. The data is from 30 FitBit users who consented to the submission of personal tracker data and generated by from a distributed survey via Amazon Mechanical Turk. Participants were chosen by responding to a survey, rather than being chosen at random.

Original: The data is from Fitbit users via Amazon Mechanical Turk.

Comprehensive: Unfortunantely, the gender of the participants is unknown in the dataset which is important to know in regards to answering our study questions. We will assume that the data gathered is applicable to Bellabeat products which are targeted mostly for women. Again, the sample size is small and most data is recorded during certain days of the week.

Current: The data is not current in which it was generated in March 2016-May 2016. 

Cited: Unknown

## 3. Process

First, examine the data, check for NA, and remove duplicates for three main tables: daily_activity, sleep_day and weight:
dim(sleep_day)
sum(is.na(sleep_day))
sum(duplicated(sleep_day))
sleep_day <- sleep_day[!duplicated(sleep_day), ]

