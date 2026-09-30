🛒 Market Basket Analysis & Product Recommendation System

An end-to-end Market Basket Analysis and Product Recommendation System built using Python, FP-Growth, Association Rule Mining, and Streamlit.

The project analyzes retail transaction data to discover products that are frequently purchased together and uses the discovered association rules to generate product recommendations.

🚀 Live Demo

👉 **[Open the Live Application](https://market-basket-analysis-nytangbjikqbbgmyiyvwsi.streamlit.app/)**

📌 Project Overview

Market Basket Analysis is a data mining technique used to identify relationships between products based on customer purchasing behavior.

This project processes retail transaction data, creates transaction baskets, applies the FP-Growth algorithm to identify frequent itemsets, generates association rules, and integrates the results into an interactive Streamlit web application.

The application provides:

- Product recommendations
- Association rule analysis
- Product quantity analysis
- Product revenue analysis
- Confidence and lift analysis
- Interactive dashboard visualizations

🎯 Objectives

- Clean and preprocess retail transaction data.
- Create product baskets from invoice-level transactions.
- Convert transactions into a one-hot encoded format.
- Discover frequent itemsets using FP-Growth.
- Generate association rules using Support, Confidence, and Lift.
- Build a product recommendation system.
- Visualize important market basket insights.
- Deploy the application as an interactive web application.

🔄 Project Workflow

```text
Retail Transaction Dataset
            ↓
       Data Cleaning
            ↓
     Transaction Filtering
            ↓
      Basket Creation
            ↓
      One-Hot Encoding
            ↓
        FP-Growth
            ↓
   Frequent Itemsets
            ↓
    Association Rules
            ↓
 Recommendation Rules
            ↓
   Streamlit Dashboard
            ↓
     Online Deployment
🧹 Data Processing

The original retail transaction data was cleaned and prepared before performing Market Basket Analysis.

The final cleaned dataset contained:

524,878 records
4,338 customers
8 relevant columns

The transaction processing resulted in:

19,150 transactions
3,884 unique products

Products were grouped using InvoiceNo to create individual shopping baskets.

Duplicate products within the same basket were removed before one-hot encoding.

🤖 Algorithm
FP-Growth

The project uses the FP-Growth (Frequent Pattern Growth) algorithm to identify frequently occurring product combinations.

FP-Growth is used to efficiently mine frequent itemsets from the transaction data.

After obtaining frequent itemsets, association rules are generated to identify relationships between products.

📊 Association Rule Metrics
Support

Support measures how frequently an itemset occurs in the complete transaction dataset.

Confidence

Confidence measures how often the consequent product is purchased when the antecedent product is purchased.

Lift

Lift measures the strength of association between two products compared with their independent occurrence.

The project uses these three metrics to evaluate and rank product relationships.

📈 Model Results

The final rule set produced:

Metric	Result
Association Rules	669
Products with Rules	235
Maximum Confidence	90.94%
Maximum Lift	56.58
MBA Transactions	19,150
MBA Products	3,884
🛍️ Example Recommendation
Input Product

REGENCY SUGAR BOWL GREEN

Recommended Product

REGENCY MILK JUG PINK

Metric	Value
Support	1.05%
Confidence	78.29%
Lift	56.58

Another tested example:

VINTAGE SNAP CARDS

→ VINTAGE HEADS AND TAILS CARD GAME

Support: 1.17%
Confidence: 32.56%
Lift: 13.80
🖥️ Streamlit Application

The application contains three main sections:

🔎 Recommendations

Users can select a product and choose the number of recommendations to generate.

The application displays recommended products along with their association metrics.

📊 Analytics

The Analytics page provides:

Dataset overview
Association rule statistics
Top 10 products by quantity
Top 10 products by revenue
Strongest product associations
Top rules by confidence
Top rules by lift

Revenue is calculated using:

Revenue = Quantity × UnitPrice
ℹ️ About Project

Provides information about:

Project objective
Methodology
FP-Growth
Support
Confidence
Lift
Model statistics
🛠️ Technology Stack
Programming Language
Python
Libraries & Frameworks
Pandas
NumPy
MLxtend
Streamlit
Development Tools
VS Code
Jupyter Notebook
Version Control
Git
GitHub
Deployment
Streamlit Community Cloud
📁 Project Structure
Market-Basket-Analysis/
│
├── dashboard/
│   └── app.py
│
├── data/
│   ├── processed/
│   └── raw/
│
├── models/
│   └── recommendation_rules.csv
│
├── notebooks/
│   └── market_basket_analysis.ipynb
│
├── outputs/
│
├── src/
│
├── requirements.txt
└── .gitignore
⚙️ Installation & Setup

Clone the repository:

git clone https://github.com/jd-tarun/Market-Basket-Analysis.git

Navigate to the project:

cd Market-Basket-Analysis

Create and activate a virtual environment:

python -m venv venv

Windows:

venv\Scripts\activate

Install dependencies:

pip install -r requirements.txt

Run the Streamlit application:

streamlit run dashboard/app.py

The application will open locally in your browser.

🔗 Project Links
Live Application

https://market-basket-analysis-nytangbjikqbbgmyiyvwsi.streamlit.app/

GitHub Repository

https://github.com/jd-tarun/Market-Basket-Analysis

📚 Dataset

The project uses the Online Retail Dataset from the UCI Machine Learning Repository.

Dataset source:

https://archive.ics.uci.edu/dataset/352/online+retail

The dataset contains retail transaction records used for performing Market Basket Analysis.

🔮 Future Scope

Possible future improvements include:

More advanced recommendation strategies
Real-time recommendation generation
Personalized recommendations based on customer history
Improved rule filtering
Larger and more recent datasets
Integration with retail/e-commerce platforms
Additional interactive visualizations