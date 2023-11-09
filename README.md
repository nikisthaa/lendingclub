# Lending Club

## Problmen Domain
Banking/Finance

## Problem Statement
You work for a consumer finace company which specializes in lending various types of loans to urban customers.
- Data engineering team should clean the data so the other team can use them.
- Should also calculate risk score on whoch company can approve or disapprove the loan request.

This is important for the following two reasons:
- If applicant is likely to pay, but the company disappropves, then its a business loss for the company.
- If applucant is unlikely to pay, but the company approves, then its a financial loss to the company.

## Datased Used
- Lending club dataset (1.7 gb), 1 csv file, 118 columns and 2+ million records.
- [Link to data source] (https://www.kaggle.com/datasets/wordsforthewise/lending-club/)

## Data Source Mock Up
- In real world, the fintech dataset is generally large, and have muliple files. In order to simlate that, I have divided the single csv file, into the following datasets:
1. customers
2. loans
3. loan repayments
4. loan defaulters
- All are in csv format

## Data Preprocessing
- The raw data in each csv file is processed and cleaned. Some usual cleaning strategies applied are:
1. Changing to suitable datatype 
2. Renaming columns
3. Removing null values
4. Adding ingestion date
- Stored cleaned data to datalake

## Data Processing
- Created external tables for each type of data, so that other team can use them.
- Created a view that gived a single overview of complete loan datas
- Created a table for the single overview of complete loan data. This table is created by a script that runs weekly. This was done so that some poople can get the required data in the fastest way possible.
- Calculated loan scores using loan repayment history, loan defaulters history, and customer's financial health data.
