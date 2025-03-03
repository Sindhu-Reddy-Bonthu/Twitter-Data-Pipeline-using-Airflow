# Twitter-Data-Pipeline-using-Airflow

## Overview
This project builds an end-to-end Twitter data pipeline using **Apache Airflow**. The pipeline extracts data from Twitter, processes it, and stores it in a database for further analysis. It demonstrates the use of **ETL (Extract, Transform, Load)** principles and workflow orchestration with **Airflow**.

## Features
- **Data Extraction**: Retrieves tweets from the Twitter API.
- **Data Processing**: Cleans and refines raw tweet data.
- **Storage**: Saves processed data into a PostgreSQL database.
- **Automation**: Leverages Apache Airflow for task scheduling and monitoring.
- **Logging & Monitoring**: Logs pipeline execution and captures errors for debugging.

## Technologies Used
- **Apache Airflow**: Orchestrates workflows and schedules tasks.
- **Python**: Implements data extraction, transformation, and loading.
- **Twitter API**: Fetches real-time tweet data.
- **PostgreSQL**: Stores structured tweet data.
- **Docker**: Ensures containerized execution of Airflow components.

## Installation & Setup
### Prerequisites
Ensure you have the following installed:
- Docker & Docker Compose
- Python 3.11
- PostgreSQL

### Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/Sindhu-Reddy-Bonthu/Twitter-Data-Pipeline-using-Airflow.git
   cd Twitter-Data-Pipeline-using-Airflow
   ```
2. Set up the virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. Configure Twitter API credentials in a `.env` file:
   ```
   TWITTER_API_KEY=your_api_key
   TWITTER_API_SECRET=your_api_secret
   TWITTER_ACCESS_TOKEN=your_access_token
   TWITTER_ACCESS_SECRET=your_access_secret
   ```
4. Start Airflow services using Docker:
   ```bash
   docker-compose up -d
   ```
5. Access the Airflow UI at: `http://localhost:8080`

## Usage
- Modify `dags/twitter_etl.py` to update API parameters or processing logic.
- Start the Airflow scheduler and trigger the DAG manually in the UI.
- Query the PostgreSQL database to analyze stored tweets.

## License
This project is licensed under the MIT License.
