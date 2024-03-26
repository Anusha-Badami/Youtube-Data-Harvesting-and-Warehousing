**YOUTUBE DATA HARVESTING & WAREHOUSING**

**Problem Statement:**

The problem at hand is to develop a Streamlit application that empowers users to access and analyze data from multiple YouTube channels efficiently. The application needs to fulfill the following objectives:
Allow users to input a YouTube channel ID and retrieve comprehensive data including the channel name, subscribers, total video count, playlist ID, video ID, likes, dislikes, and comments for each video utilizing the Google API.
Enable data collection for up to 10 different YouTube channels with the capability to store them in a data lake by activating a button.
Offer the option to store collected data in either MySQL or PostgreSQL databases.
Facilitate searching and retrieving data from the SQL database through various search options, incorporating table joins to acquire detailed channel information.


**Project Objective:**

The primary aim of this project is to create a user-friendly Streamlit application that seamlessly integrates with the YouTube API to retrieve and manage data from multiple channels. The key objectives are as follows:
Develop a Streamlit app for user interaction and data display.
Utilize the YouTube API to fetch relevant data for specified channels.
Implement data storage and cleaning mechanisms, utilizing pandas DataFrames or similar structures.
Migrate collected data to a SQL data warehouse (MySQL or PostgreSQL).
Employ SQL queries to efficiently retrieve and manipulate data from the warehouse.
Integrate data visualization features within the Streamlit app to aid users in analyzing the retrieved data.



**Approach:**

The approach for accomplishing the project objectives involves several key steps:
Set up Streamlit App: Create a user interface using Streamlit where users can input YouTube channel IDs and view channel details.
Connect to YouTube API: Utilize the Google API client library in Python to access and retrieve channel and video data from YouTube.
Store and Clean Data: Use pandas DataFrames or similar structures to temporarily store and clean the retrieved data before migrating it to the data warehouse.
Migrate Data to SQL Warehouse: Transfer the collected data to a SQL database such as MySQL or PostgreSQL for long-term storage and efficient querying.
Query SQL Data Warehouse: Employ SQL queries, possibly using libraries like SQLAlchemy, to extract specific data from the warehouse based on user input and requirements.
Display Data in Streamlit App: Utilize Streamlit's data visualization capabilities to present the retrieved data in an intuitive and informative manner within the application.

By following this approach, the project aims to provide users with a robust tool for accessing, analyzing, and visualizing data from multiple YouTube channels seamlessly.






