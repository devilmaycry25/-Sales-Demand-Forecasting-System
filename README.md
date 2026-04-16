# -Sales-Demand-Forecasting-System

📝 Project Overview
This project is a machine learning-based solution designed to help businesses transition from "guessing" to data-driven planning. By analyzing historical purchase data and external calendar events, the system predicts future sales demand to optimize operational efficiency.

Core Business Objectives
Plan Inventory: Ensure the right amount of stock is available for holiday peaks.

Manage Cash Flow: Predict revenue cycles to make better financial investments.

Prepare Staffing: Anticipate high-volume periods to scale customer support and warehouse teams.

Minimize Losses: Reduce costs associated with overstocking or missing sales due to stockouts.

🛠️ System Components
The project consists of two specialized forecasting modules:

1. Holiday-Impact Forecaster (holiday_sales_forecast.py)
This module uses the holidays_events.csv dataset to understand how external national and local events drive consumer behavior.

Logic: It identifies specific dates in the calendar that historically cause sales "spikes."

Key Features: National/Local holiday flags, monthly seasonality, and day-of-week trends.

Business Value: Critical for marketing teams to time their seasonal promotions and for supply chain managers to prepare for holiday rushes.

2. Ticket-Based Demand Forecaster (ticket_demand_forecast.py)
This module uses the customer_support_tickets.csv dataset, treating every recorded purchase as a demand signal.

Logic: It aggregates individual purchase records into daily volume metrics to identify organic growth trends.

Key Features: Moving averages, purchase frequency, and product-specific demand cycles.

Business Value: Vital for operations managers to predict when a surge in sales will lead to a proportional surge in customer support inquiries.

📊 Data Features & Engineering
To achieve high accuracy, the system transforms raw date data into actionable intelligence:

Temporal Features: Extraction of Month, Day, and Day of Week (Weekend vs. Weekday).

Event Flags: Binary mapping of is_holiday based on the provided holiday database.

Aggregation: Conversion of row-level support tickets into daily time-series counts.

🚀 Installation & Setup
Prerequisites
Ensure you have Python 3.8+ installed along with the following libraries:

Bash
pip install pandas numpy matplotlib scikit-learn


<img width="1200" height="600" alt="image" src="https://github.com/user-attachments/assets/b9003b33-a25e-4c30-b149-cd3b9f72f500" />

Execution
Place holidays_events.csv and customer_support_tickets.csv in the project root.

Run the individual modules to generate forecasts and visuals:

Bash
python holiday_sales_forecast.py
python ticket_demand_forecast.py
