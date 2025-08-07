# Reddit Subreddit Scraper

This Python script uses the PRAW (Python Reddit API Wrapper) library to scrape data from specified subreddits. It extracts key information about posts and saves the data into a structured CSV file for analysis.

## Features

- Scrapes the top 'n' posts from any public subreddit.
- Extracts post title, score, ID, URL, number of comments, creation date, and author.
- Saves the collected data into a clean CSV file.
- Handles API credentials securely via a configuration file.

## Installation & Setup

Follow these steps to get the scraper up and running.

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your-username/your-reddit-scraper.git](https://github.com/your-username/your-reddit-scraper.git)
    cd your-reddit-scraper
    ```

2.  **Create and activate a virtual environment:**
    * On macOS/Linux:
        ```sh
        python3 -m venv venv
        source venv/bin/activate
        ```
    * On Windows:
        ```sh
        python -m venv venv
        venv\Scripts\activate
        ```

3.  **Install the required libraries:**
    ```sh
    pip install -r requirements.txt
    ```

4.  **Set up your Reddit API credentials:**
    * You need to get a `client_id` and `client_secret` from Reddit. To do this, go to your [Reddit apps preferences](https://www.reddit.com/prefs/apps).
    * Click "are you a developer? create an app...".
    * Fill out the form:
        * Choose the "**script**" app type.
        * Set a `redirect uri` (e.g., `http://localhost:8080`). This is required but won't be used for a script.
    * Once your app is created, you will see your `client_id` (under the app name) and your `client_secret`.
    * In the project folder, rename `config.example.ini` to `config.ini`.
    * Open `config.ini` and paste your credentials into the appropriate fields.

## Usage

To run the scraper, use the `main.py` script from the command line.

```sh
python src/main.py --subreddit learnpython --limit 100 --output results.csv
```

**Arguments:**
- `--subreddit`: The name of the subreddit you want to scrape (e.g., `learnpython`).
- `--limit`: The number of posts to scrape (e.g., `100`).
- `--output`: The name of the output CSV file (e.g., `results.csv`).

## Disclaimer

This tool is intended for educational and research purposes only. Please respect Reddit's API Terms of Service and be mindful of the number of requests you make. Do not use this tool for spam or any malicious activities.

## License

Distributed under the MIT License. See `LICENSE` file for more information.
