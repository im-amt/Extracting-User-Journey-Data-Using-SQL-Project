# Extracting-User-Journey-Data-Using-SQL-Project

Extracting User Journey Data with SQL

Overview

This project analyzes user navigation patterns on a website using SQL. By extracting and structuring data from a relational database, we can track visitor interactions, identify conversion paths, and analyze purchasing behavior. The insights gained from this project can help optimize user experience, improve marketing strategies, and increase conversions.

Objective
	•	Extract user journey data by analyzing the sequence of page visits.
	•	Identify visitor interactions on the front page, such as clicks and navigation patterns.
	•	Analyze purchasing behavior to understand conversion rates and subscription trends.
	•	Filter out test users to ensure accurate insights.

Database Structure

The database consists of three key tables:

1. front_interactions

Records all visitor activity on the front page, including page visits, clicks, and interactions.
	•	visitor_id – Unique ID of the visitor.
	•	session_id – The session number for the interaction.
	•	event_source_url – URL where the event occurred.
	•	event_destination_url – URL where the event led.
	•	event_date – Timestamp of the interaction.
	•	event_name – Internal event name (e.g., button click, scroll).

➡ This table is essential for tracking user navigation paths.

2. student_purchases

Contains records of user payments and the type of product purchased.
	•	user_id – Unique user ID (different from visitor_id).
	•	purchase_id – Unique purchase identifier.
	•	purchase_type – Subscription type (0=Monthly, 1=Quarterly, 2=Annual).
	•	purchase_price – Amount paid (test users may have $0 purchases).
	•	date_purchased – Timestamp of the purchase.

➡ This table helps analyze conversion trends and subscription behavior.

3. front_visitors

Links visitors to registered users (many visitors do not create accounts).
	•	visitor_id – ID of the visitor.
	•	user_id – Corresponding user ID (NULL if no account was created).

➡ This table connects anonymous visitors to registered users.

Project Structure
	•	User_Journey_Database.sql – SQL script to generate the database schema and tables.
	•	URL_Aliases.xlsx – A reference list mapping URLs to user-friendly names.
	•	README.md – Project documentation.

How to Use This Project
	1.	Set Up the Database
	•	Open MySQL and establish a local connection.
	•	Run User_Journey_Database.sql to create the database.
	2.	Explore the Data
	•	Query the tables to understand user interactions.
	•	Use JOIN operations to connect visitor behavior with purchases.
	3.	Extract User Journeys
	•	Analyze page sequences to track navigation paths.
	•	Identify common conversion funnels and drop-off points.
	4.	Filter Out Test Users
	•	Exclude records where purchase_price = 0.
	5.	Visualize Insights
	•	Use Tableau or Python for further data visualization (optional).

Conclusion

This project provides valuable insights into user behavior and conversion trends by analyzing customer journey data using SQL. The findings can help businesses optimize website navigation, improve user experience, and enhance marketing strategies. 🚀📊
