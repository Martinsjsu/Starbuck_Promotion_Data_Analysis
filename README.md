# Starbuck Promotion Data Analysis
A Udactiy Capstone Project
## Installation
Must runing with Python 3 with libraries of numpy, pandas, json, seaborn, matplotlib and sklearn.

## Porject Motiviation
The motivation is trying to achieve the goal to help Starbucks, while practising my own data scientist skills. The goal of this project is to help Starbucks have a better understanding of the relationship between the promotion offers and its customers by the following two questions:

**1. Which demographic groups respond best to which offer type?**

**2. What are the top 5 features that influence those offer reactions?**

## File Descriptions
The data is contained in three files:

- portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
- profile.json - demographic data for each customer
- transcript.json - records for transactions, offers received, offers viewed, and offers completed
- Here is the schema and explanation of each variable in the files:

**portfolio.json**


- id (string) - offer id
- offer_type (string) - type of offer ie BOGO, discount, informational
- difficulty (int) - minimum required spend to complete an offer
- reward (int) - reward given for completing an offer
- duration (int) - time for offer to be open, in days
- channels (list of strings)

**profile.json**

- age (int) - age of the customer
- became_member_on (int) - date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

**transcript.json**

- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since start of test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record

## Machine Learning Modelling
Two Random Forest models were built for offer viewed and offer completed. Model with offer viewed scored at 0.64, while model with offer completed scored at 0.77.

## Results
The initial two questions were anwserd in different plots and tables with the suggestion for Starbucks.  Detailed discussion **blog is [here](https://medium.com/@quanye003/two-things-starbucks-wished-to-know-before-they-send-the-promotion-offers-out-36aceec102b4).**
