# CRM Sales & Pipeline Analysis Dashboard in Power BI

Hello! Welcome to my CRM Sales Analysis project. I built this interactive dashboard in Power BI to analyze a company's sales pipeline, track key performance metrics, and identify opportunities for growth. This project showcases a complete workflow from raw data to actionable business insights.

---

##  Dashboard Preview

Here's a look at the three main pages of the dashboard:

### 1. Sales Performance Overview
This page provides a high-level summary of the most important sales KPIs, including total revenue, win rate, average deal size, and sales cycle duration. It also tracks monthly revenue trends and breaks down revenue by product.

![alt text](<Sales Performance Overview-1.png>)

### 2. Pipeline Analysis
This view dives into the health of the sales funnel. It visualizes the number of deals at each stage (Prospecting, Engaging, Won, Lost) and provides a list of open deals currently being worked by the sales team.

![alt text](<Pipeline Analysis -1.png>)

### 3. Sales Rep Performance
This page focuses on individual and team performance. It includes a leaderboard ranking sales agents by total revenue and win rate, allowing for a clear view of top performers.
![alt text](<Sales Rep Performance-1.png>)


---

##  Project Objectives

The main goal of this project was to answer critical business questions:
- What is our total revenue and how is it trending over time?
- What is the overall health of our sales pipeline?
- Which products are driving the most revenue?
- Who are our top-performing sales agents?
- What is our average sales cycle, and can we shorten it?

##  Key Insights & Findings

After digging into the data, I uncovered several key insights:

- **Strong Revenue Performance:** The company generated **$10M in total revenue** from 4.2K won deals.
- **Healthy Win Rate:** With a **48.2% win rate**, the sales team is effectively converting leads into customers.
- **Top Performers Identified:** **Darcel Schlicht** is the top sales agent, bringing in over **$1.15M** in revenue.
- **Product Concentration:** The **GTX Pro** and **MG Advanced** product lines account for over 74% of total revenue, suggesting a strong market fit for these products.
- **Active Pipeline:** There are over 2,100 deals currently in the "Engaging" or "Prospecting" stages, representing significant future revenue potential.

## Tools & Techniques

- **Tool:** Microsoft Power BI
- **Data Source:** [Maven Analytics CRM Sales Opportunities Dataset](https://mavenanalytics.io/data-playground)
- **Data Cleaning:** Used Power Query to handle missing values, correct data types, and ensure data integrity.
- **Data Modeling:** Built relationships between the sales, products, accounts, and sales teams tables. Created a dedicated Date table for time intelligence.
- **DAX (Data Analysis Expressions):** Wrote several measures to calculate key metrics like Total Revenue, Win Rate, Average Deal Size, and Sales Cycle.

### Example DAX Measure (Sales Cycle):
```dax
Sales Cycle (Days) = 
AVERAGEX(
    FILTER('Sales Pipeline', 'Sales Pipeline'[Deal Stage] = "Won"),
    DATEDIFF('Sales Pipeline'[Engage Date], 'Sales Pipeline'[Close Date], DAY)
)
```

##  How to Use This Project

1. **Download** the `.pbix` file from this repository.
2. **Open** it in Power BI Desktop.
3. **Interact** with the slicers and filters to explore the data for yourself!

---

Thanks for checking out my project! Feel free to connect with me if you have any questions or feedback.
