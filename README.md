# Business-Analysis

# Project description 
You've done beautifully in the Practicum course, and you've been offered an internship in the analytical department at Y.Afisha. Your first task is to help optimize marketing expenses. 

You have:
- Server logs with data on Y.Afisha visits from January 2017 through December 2018
- Dump file with all orders for the period
- Marketing expenses statistics

You are going to study: 
- How people use the product
- When they start to buy
- How much money each customer brings
- When they pay off

# Instruction for the project
**Step 1.** Download the data and prepare it for analysis
Store the data on visits, orders, and expenses in variables. Optimize the data for analysis. Make sure each column contains the correct data type. 
File paths:
- /datasets/visits_log_us.csv. 
- /datasets/orders_log_us.csv. 
- /datasets/costs_us.csv. 

**Step 2.** Make reports and calculate metrics:
1. Product
    - How many people use it every day, week, and month?
    - How many sessions are there per day? (One user might have more than one session.)
    - What is the length of each session?
    - How often do users come back?
2. Sales
    - When do people start buying? (In KPI analysis, we're usually interested in knowing the time that elapses between registration and conversion — when the user becomes a customer. For example, if registration and the first purchase occur on the same day, the user might fall into category Conversion 0d. If the first purchase happens the next day, it will be Conversion 1d. You can use any approach that lets you compare the conversions of different cohorts, so that you can determine which cohort, or marketing channel, is most effective.)
    - How many orders do they make during a given period of time?
    - What is the average purchase size?
    - How much money do they bring? (LTV)
3. Marketing 
    - How much money was spent? Overall/per source/over time 
    - How much did customer acquisition from each of the sources cost?
    - How worthwhile where the investments? (ROI)

Plot graphs to display how these metrics differ for various devices and ad sources and how they change in time.

**Step 3.** Write a conclusion: advise marketing experts how much money to invest and where.

What sources/platforms would you recommend? Back up your choice: what metrics did you focus on? Why? What conclusions did you draw after finding the metric values?

# Data Description

Tabel `visits` (log/catatan server yang memuat data kunjungan ke situs web):
- `Uid` — user's unique identifier
- `Device` — user's device
- `Start Ts` — session start date and time
- `End Ts` — session end date and time
- `Source Id` — identifier of the ad source the user came from

**All dates in this table are in YYYY-MM-DD format.**

Tabel `orders` (data terkait pesanan):
- `Uid` — unique identifier of the user making an order
- `Buy Ts` — order date and time
- `Revenue` — Y.Afisha's revenue from the order

Tabel `costs` (data terkait pengeluaran pemasaran):
- `source_id` — ad source identifier
- `dt` — date
- `costs` — expenses on this ad source on this day
