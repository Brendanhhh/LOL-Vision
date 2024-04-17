# League of Legends Data Collector (WIP)

The aim of this project is to provide an open source available to all program that collects and aggregates League of Legends summoner data and match data for data analysis purposes.

## Disclaimer
Deprecated version provided to show what the new project is being built on. It is not intended for use and takes very long to run. CSV files obtained from the deprecated version are provided in the repository

## System Requirements

- Python 3.6+
- MongoDB
- Riot Games API Key

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Brendanhhh/LOLVision
 
2. **Setup MongoDB:**
Ensure MongoDB is running on your system. You can download it from [MongoDB Official Site](https://www.mongodb.com/try/download/community).

3. **Obtain RiotAPI key**
Signup for an account https://developer.riotgames.com/ and obtain a personal api key or register a product

4. **Configuration:**
Update the `[remove_this_text]api_key.py' and `mongodb_url` in the main scripts to match your environment and Riot Games API key.


## Components

### 1. RiotAPI Class

Handles all interactions with the Riot Games API. It supports methods for making HTTP requests and handling API rate limits.

### 2. SummonerDataCollector Class

Responsible for fetching summoner data from the Riot API and storing it in MongoDB. This includes summoner IDs along with their respective tier and division.

### 3. PUUIDConverter Class

Converts stored summoner IDs to PUUIDs and saves the PUUID along with the summoner's rank information back to MongoDB.

### 4. MatchRetriever Class

Uses PUUIDs to fetch match histories and stores the match IDs in MongoDB. It's set up to handle retrieval based on the collected PUUIDs and can be expanded to include more match details.


