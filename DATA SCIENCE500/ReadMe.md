# Books to Scrape: Data Science Analysis

## Project Deliverables
*   **`book_analysis.ipynb`**: The complete Jupyter Notebook containing the web scraping, data cleaning, visualizations, and the machine learning model.
*   **`raw_books.csv`**: The raw, unstructured dataset exactly as it was scraped from the website.
*   **`cleaned_books.csv`**: The cleaned, structured dataset used for data exploration and modelling.
*   **`project_report.pdf`**: The professional report detailing the methodology, insights, and recommendations.

## Methodology
1.  **Data Acquisition**: Utilised `requests` and `BeautifulSoup` to scrape 200 books across 10 pages. Extracted features include Title, Price, Star Rating, and Stock Availability.
2.  **Data Cleaning**: Processed the raw data using `pandas`. Removed currency symbols (e.g., £) and hidden encoding artifacts to convert prices to numerical floats. Handled missing values and dropped duplicates. Engineered a new feature (`Stock_Qty`) to extract numerical stock quantities.
3.  **Data Visualization**: Used `matplotlib` and `seaborn` to generate 5 distinct visualizations exploring pricing distributions, rating frequencies, and the relationship between price and rating.
4.  **Predictive Modelling**: Built a Linear Regression model using `scikit-learn` to predict book prices based on their star ratings. Evaluated using Mean Squared Error (MSE), Root MSE, and the R-squared (R²) score.

## Key Insights
*   The average price of a book in the dataset is **£34.80**.
*   **Star Rating is a poor predictor of Price**. The Linear Regression model yielded an R-squared score very close to 0, indicating no strong linear relationship between a book's rating and its price. 
*   Books across all rating levels (1-star to 5-star) share very similar price ranges. Publishers and retailers likely base pricing on other factors (such as format, genre, or length) rather than customer reviews.

## Requirements to Run
To run the Jupyter Notebook locally, you will need the following Python libraries:
```bash
pip install requests beautifulsoup4 pandas matplotlib seaborn scikit-learn
