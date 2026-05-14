# Customer Analytics, Segmentation & Price Elasticity Modelling

## Project Overview
End-to-end customer analytics pipeline covering descriptive analysis, 
behavioural segmentation and price elasticity modelling on retail 
purchase data. Built to identify high-value customer segments and 
generate actionable pricing and marketing recommendations.

## Business Objective
- Identify distinct customer segments based on purchase behaviour
- Profile each segment by revenue contribution and brand preference
- Model purchase probability and price sensitivity at segment level
- Generate targeted pricing and promotional recommendations

## Project Structure
| Notebook | Description |
|----------|-------------|
| 01_Descriptive_Analysis.ipynb | Exploratory analysis, segment profiling, descriptive statistics |
| 02_Segmentation.ipynb | PCA dimensionality reduction and K-Means clustering |
| 03_Modelling.ipynb | Price elasticity, purchase probability and simulation |

## Technical Approach

### Segmentation
- Applied PCA for dimensionality reduction
- Used K-Means clustering to identify distinct customer groups
- Profiled segments by proportion, revenue, brand value and 
  behavioural differences

### Price Elasticity Modelling
- Built Purchase Probability model using Logistic Regression
- Built Purchase Quantity model using Linear Regression
- Modelled Brand Choice at segment level
- Ran Own Price and Cross Price Elasticity simulations
- Evaluated impact of Promotions on Purchase Probability 
  across segments

## Tools & Libraries
- Python
- Pandas, NumPy, SciPy
- Scikit-learn
- Matplotlib, Seaborn

## Key Insights
- Identified customer segments with distinct price sensitivity profiles
- High value segments showed lower price elasticity confirming 
  brand loyalty
- Promotional effectiveness varied significantly across segments
- Segment level simulations enabled targeted pricing recommendations

## Author
**Manzoor Syiemlieh**  
Data Scientist | Fraud & Risk Analytics | 7+ Years Fintech @ PayPal  
[LinkedIn](https://www.linkedin.com/in/manzoor-syiemlieh)
