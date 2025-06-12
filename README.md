# stock-market-trial
# Simple Stock Price Tracker

## Project Overview

This project demonstrates the fundamental concepts of fetching real-time (or near real-time) stock market data using a public API, parsing JSON responses, and displaying key financial metrics. Built as a command-line Python application, it allows users to quickly retrieve current stock prices and daily performance for specified company ticker symbols.

**Key features:**
* Fetches current stock price, daily open, high, low, previous close, volume, and percentage change.
* Handles invalid ticker symbols gracefully.
* Provides clear, formatted output in the console.

## Technologies Used

* **Python:** The core programming language for the application logic.
* **Requests Library:** Used for making HTTP GET requests to the Alpha Vantage API.
* **Alpha Vantage API:** A free API for financial data, used to retrieve stock quotes.

## How It Works

1.  **API Key Acquisition:** An API key is obtained from Alpha Vantage to authenticate requests.
2.  **HTTP GET Request:** The Python `requests` library sends a GET request to the Alpha Vantage `GLOBAL_QUOTE` endpoint.
3.  **Parameterization:** The stock ticker symbol and API key are passed as URL parameters to specify the requested data.
4.  **JSON Parsing:** The API's JSON response is parsed into a Python dictionary.
5.  **Data Extraction & Formatting:** Relevant financial metrics (e.g., price, daily change) are extracted from the nested JSON structure and formatted for clear display.
6.  **Error Handling:** The script includes basic error handling for network issues, API errors, and invalid ticker symbols.

## Setup and Running the Project

To run this project locally, follow these steps:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/Stock-Price-Tracker.git](https://github.com/YOUR_USERNAME/Stock-Price-Tracker.git)
    cd Stock-Price-Tracker
    ```
2.  **Create a Virtual Environment (Recommended):**
    ```bash
    python -m venv venv
    # On Windows:
    .\venv\Scripts\activate
    # On macOS/Linux:
    source venv/bin/activate
    ```
3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Obtain an Alpha Vantage API Key:**
    * Visit [https://www.alphavantage.co/support/#api-key](https://www.alphavantage.co/support/#api-key)
    * Sign up for a free API key.
5.  **Configure Your API Key:**
    * Open `stock_tracker.py`.
    * Replace `"YOUR_ALPHA_VANTAGE_API_KEY"` with your actual API key:
        ```python
        API_KEY = "YOUR_ALPHA_VANTAGE_API_KEY"
        ```
6.  **Run the Application:**
    ```bash
    python stock_tracker.py
    ```

## Example Output
