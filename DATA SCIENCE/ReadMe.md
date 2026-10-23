NAME AND SURNAME: LETLOTLO KUAHO
FIELD OF STUDY: BSC IT
YEAR OF STUDY: 1
ASSIGNMENT DUE DATE 23/10/26                   DATE SUBMITTED 22/10/26


PROJECT OVERVIEW:
The objective of this assignment was to build and end-to-end data pipeline to analyze book catalogue trends and predict the pricing patterns. The dataset was acquired by scraping 200 books from the "BOOKS TO SCRAPE" practice website. 

PROJECT DELIVERABLES 
"books_analysis.ipynb"; the complete Jupiter Notebook containing the web scraping, data cleaning, visualizations and the machine learning model.
"raw_book.csv": The raw, unstructured dataset exactly as it was scraped from the website.
"cleaned_books.csv": The cleaned, structured dataset used for data exploitation and modelling.

METHODOLOGY
1) Data Acquisition: Utilised requests and beautifulsoup to scrape 200 books across 10 pages. Extracted features include Title,Price, Star Rating and stock availability.
2) Data Cleaning: Processed the raw data using pandas. Removed currency symbols (e.g £) and hidden encoding artifacts to convert prices to numerical floats. Handled missing values and dropped duplicates. Engineered a new feature (stock_Qty) to extract numerical stock quantities.
3) Data visualization: Used matplotlib and seaborn to generate 5 distinct visualizations exploring pricing distribution, rating frequencies and relationship between price and rating.
4) Predictive Modelling: Built a Linear Regression model using "scikit-learn" to predict book prices based on their star ratings. Evaluated using mean Squared Error (MSE), Root MSE, and the R-squared(R^2) score.

KEY INSIGHT
-The average price of book in the database is "£34.80".
-star rating is a poor predictor of price. The Linear Regression model yielded an R-Squared score very close to 0 , indicating no strong Linear relationship between a book's rating ang its price.
-Books across all rating levels (1-star to 5-star) share very similar price ranges . publishers and retailers likely base pricing on other factors (such as format, genre or length) rather than customer reviews

REQUIREMENTS TO RUN 
To run the Jupyter Notebook locally, you will need the following python libraries:
pip install requests beautifulsoup4 pandas matplotlib seaborn scikit-learn

GITHUB LINK
[InternetShortcut]
URL=https://github.com/Letlotlo15/Books-to-Scrap-Analysis#books-to-scrap-analysis
