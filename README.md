Based on your notebook, here is a **clean, professional README.md** you can use for your project.

---

# Real Estate Data Collection and Analysis – Yerevan Apartments

## Project Overview

This mini-project demonstrates a **complete data analysis workflow**, starting from **web scraping** and ending with **exploratory data analysis (EDA)**.

The project focuses on collecting and analyzing **real estate listings of apartments for sale in Yerevan, Armenia**. The data is scraped from the Armenian real estate website **real-estate.am**, cleaned, processed, and analyzed to explore patterns in apartment prices and property characteristics.

The goal of the project is to demonstrate practical skills in:

* web scraping
* data cleaning
* data preprocessing
* exploratory data analysis
* statistical testing
* data visualization

---

# Data Source

The data was collected from:

**[https://www.real-estate.am](https://www.real-estate.am)**

This website provides current listings of apartments available for sale in different districts of **Yerevan**.

The scraper collects the following information from each listing:

* Apartment ID
* Listing link
* Location
* Price
* Number of bedrooms
* Apartment area
* Floor information

The scraper automatically visits multiple pages of listings and extracts structured information from each property card.

---

# Project Workflow

The project follows the full **data science pipeline**.

---

# 1. Web Scraping

Apartment listings were collected using **Python** with the following libraries:

* `requests`
* `BeautifulSoup`
* `pandas`

The scraper navigates through several pages of the website and extracts structured information for each listing.

The collected data includes:

* apartment ID
* property link
* location
* price
* number of bedrooms
* apartment area
* floor and building height

All collected data is saved into:

```
real-estate.csv
```

---

# 2. Data Cleaning

The raw scraped dataset contains text values, symbols, and inconsistent formatting.
The cleaning process prepares the dataset for analysis.

Cleaning steps include:

* removing rows with missing important information
* converting **price values to numeric format**
* extracting **area values from text**
* cleaning the **bedrooms column**
* splitting the **floor information** into:

  * Floor_Level
  * Total_Floors

The cleaned dataset is saved as:

```
cleaned_real_estate.csv
```

---

# 3. Data Preprocessing

In the preprocessing stage, the dataset is transformed for analysis and potential machine learning applications.

The following steps are performed:

### Feature Engineering

A new feature is created:

```
Price_per_sqm = Price / Area
```

This metric allows better comparison between properties.

---

### Handling Missing Values

Missing numeric values are filled with the **mean value of the column**.

---

### Encoding Categorical Data

The **Location** column is encoded into numeric format using:

```
LabelEncoder
```

---

### Feature Scaling

Important numerical features are standardized using:

```
StandardScaler
```

Scaled features include:

* Price
* Area
* Price_per_sqm

The final processed dataset is saved as:

```
preprocessed_real_estate.csv
```

---

# 4. Exploratory Data Analysis (EDA)

Exploratory analysis was conducted to understand patterns in the real estate market.

Libraries used:

* pandas
* matplotlib
* seaborn
* scipy

The analysis includes:

### Descriptive Statistics

Summary statistics were calculated for:

* price
* apartment area
* number of bedrooms
* floor level

---

### Price Distribution

Histogram plots were used to analyze the distribution of apartment prices.

The analysis also calculated **price skewness** to understand market distribution.

---

### Price per Square Meter Analysis

Box plots were used to explore the distribution of **price per square meter**, which is an important real estate indicator.

---

### Correlation Analysis

A correlation matrix was generated to examine relationships between numerical features:

* Price
* Area
* Bedrooms
* Floor level
* Total floors
* Price per square meter

Heatmaps were used to visualize these relationships.

---

# 5. Hypothesis Testing

A statistical hypothesis test was conducted to examine whether **high-rise buildings and low-rise buildings differ in price per square meter**.

Buildings were categorized as:

* **High-Rise** – more than 10 floors
* **Low-Rise** – 10 floors or fewer

A **Welch's T-test** was applied using `scipy.stats`.

This test determines whether the average price per square meter differs significantly between the two groups.

---

# 6. Data Visualization

Several visualizations were created to explore relationships in the dataset.

Examples include:

### Scatter Plots

* Price vs Area
* Price per square meter vs Total floors

### Bar Charts

* Number of listings by number of bedrooms

### Box Plots

* Price distribution by number of bedrooms
* Price per square meter by building type

These visualizations help reveal trends and outliers in the real estate market.

---

# Technologies Used

* Python
* Google Colab
* Requests
* BeautifulSoup
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy

---

# Project Structure

```
Mini_Project_Viktorya_Margaryan

│
├── Mini_Project_Viktorya_Margaryan.ipynb
├── real-estate.csv
├── cleaned_real_estate.csv
├── preprocessed_real_estate.csv
└── README.md
```

---

# Conclusion

This project demonstrates a complete **real-world data analysis workflow**, starting from web scraping and ending with statistical analysis and visualization.

Through this process, the project reveals important insights into the **Yerevan real estate market**, including price distributions, relationships between apartment characteristics, and statistical differences between different building types.

The project also provides a foundation for future work such as:

* predictive modeling of apartment prices
* clustering of real estate listings
* machine learning applications for property valuation.

---

If you want, I can also show you **2 small improvements that will make your project look much more professional on GitHub (like a real data science portfolio project)**.
