******YOUTUBE DATA HARVESTING & WAREHOUSING******



***Problem Statement:***

The problem at hand is to develop a Streamlit application that empowers users to access and analyze data from multiple YouTube channels efficiently. The application needs to fulfill the following objectives:
* Allow users to input a YouTube channel ID and retrieve comprehensive data including the channel name, subscribers, total video count, playlist ID, video ID, likes, dislikes, and comments for each video utilizing the Google API.
* Enable data collection for up to 10 different YouTube channels with the capability to store them in a data lake by activating a button.
* Offer the option to store collected data in either MySQL or PostgreSQL databases.
* Facilitate searching and retrieving data from the SQL database through various search options, incorporating table joins to acquire detailed channel information.



***Project Objective:***

The primary aim of this project is to create a user-friendly Streamlit application that seamlessly integrates with the YouTube API to retrieve and manage data from multiple channels. The key objectives are as follows:
* Develop a Streamlit app for user interaction and data display.
* Utilize the YouTube API to fetch relevant data for specified channels.
* Implement data storage and cleaning mechanisms, utilizing pandas DataFrames or similar structures.
* Migrate collected data to a SQL data warehouse (MySQL or PostgreSQL).
* Employ SQL queries to efficiently retrieve and manipulate data from the warehouse.
* Integrate data visualization features within the Streamlit app to aid users in analyzing the retrieved data.




  ***Project Flow:***

* 1.Importing Libraries: The code starts by importing necessary libraries such as build from googleapiclient.discovery, pymongo, psycopg2, pandas, and streamlit. These libraries are used for various purposes such as interacting with Google's APIs, working with databases, handling data, and creating a web application interface using Streamlit.
* 2.API Key Connection: The Api_connect() function establishes a connection to the YouTube Data API using a provided API key (Api_Id). It creates a service object (youtube) to interact with the YouTube API.
* 3.Fetch Channel Information: The get_channel_info() function retrieves information about a specific YouTube channel based on its ID. It makes use of the channels().list() method of the YouTube API to fetch details like channel name, subscribers, views, etc.
* 4.Fetch Video IDs: The get_videos_ids() function retrieves the IDs of all videos uploaded to a specific channel. It queries the YouTube API to get the list of videos associated with the channel ID.
* 5.Fetch Video Information: The get_video_info() function retrieves detailed information about each video using its video ID. It fetches data such as video title, description, views, likes, comments, etc.
* 6.Fetch Comment Box Information: The get_comment_info() function fetches comments associated with each video. It retrieves details like comment ID, text, author, etc.
* 7.Fetch Playlist Information: The get_playlist_details() function retrieves details of playlists associated with a given channel.
* 8.Function to Upload to MongoDB: The channel_details() function aggregates all the fetched information about a channel, its videos, playlists, and comments into a MongoDB document and uploads it to a MongoDB database.
* 9.Functions to Create Tables for Channels, Videos, Playlists, and Comments: These functions are responsible for creating tables in a PostgreSQL database to store the fetched data in a structured format.
* 10.Functions to Populate Tables: These functions extract data from the MongoDB database and populate the corresponding PostgreSQL tables.
* 11.Functions to Show Tables: These functions retrieve data from the PostgreSQL database and display it using Streamlit.
* 12.Streamlit Code: This section contains the Streamlit interface code, including text inputs, buttons, and radio buttons to interact with the application. It allows users to trigger data collection, migration to SQL, and view various tables.
* 13.SQL Connection: Finally, the code establishes a connection to the PostgreSQL database and executes SQL queries based on user-selected questions to retrieve and display specific information from the database.
Overall, the code aims to collect data from YouTube channels, store it in a MongoDB database, migrate it to a PostgreSQL database, and provide a user interface to query and view the stored data.




***Approach:***

The approach for accomplishing the project objectives involves several key steps:
* Set up Streamlit App: Create a user interface using Streamlit where users can input YouTube channel IDs and view channel details.
* Connect to YouTube API: Utilize the Google API client library in Python to access and retrieve channel and video data from YouTube.
* Store and Clean Data: Use pandas DataFrames or similar structures to temporarily store and clean the retrieved data before migrating it to the data warehouse.
* Migrate Data to SQL Warehouse: Transfer the collected data to a SQL database such as MySQL or PostgreSQL for long-term storage and efficient querying.
* Query SQL Data Warehouse: Employ SQL queries, possibly using libraries like SQLAlchemy, to extract specific data from the warehouse based on user input and requirements.
* Display Data in Streamlit App: Utilize Streamlit's data visualization capabilities to present the retrieved data in an intuitive and informative manner within the application.

By following this approach, the project aims to provide users with a robust tool for accessing, analyzing, and visualizing data from multiple YouTube channels seamlessly.






