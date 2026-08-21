# TankMaster

Using this repo to share what data cleaning and analysis looks like in real-life for people to practice data interviews etc.   

This is based on my personal experience since I was actually given this task during one of my projects. It's the kind of messy spreadsheet that people have worked with organically over the years without proper data handling practices in mind.

In the repo you will find a messy, semi-realistic (redacted to the best of my abilities) tank terminal dataset. The dataset is meant to be messy (less messy than the original thank God), and your job is to untangle it. The questions below will guide you through reshaping and operationalising the data, then using it to answer real business questions.

## The Brief

You're an analyst who has just joined a bulk liquid storage company. The company operates a **tank terminal** — a facility that stores oil and fuel products on behalf of customers.

The operators have sent over an export of their tank register. Your manager has a set of business questions and needs your help. Before you can answer them, you'll need to make sense of the dataset yourself.

### Files

| File | Description |
|---|---|
| `tank.csv` | Raw dataset |
| `tank.ipynb` | Notebook with pre-filled questions so you can work on it directly |
| `answer.html` | My go at answering the questions |

### What's in the Dataset

Assume today's date is **December 2024**. Each row is one storage tank, and the columns include:

1. **Basic tank details** — tank ID, capacity (m³), and type of product the tank stores (e.g. Crude, Gasoline, Diesel/Gasoil).
2. **Capital expenditure (CAPEX) forecast** — planned spend on each tank from FY25 through FY34. A blank cell means no planned spend that year.
3. **Operational availability** — a `1` means the tank was (or is expected to be) in operation that month, whereas a `0` or blank cell means out of operation. The historical data will be needed later.

## Questions

Work through the questions in order.

### 1. Reshaping/Restructure the data

Before doing any analysis, restructure the dataset into something you can actually work with. The questions below will make more sense once you've done this — use them as a guide for what your reshaped data needs to support. Rename columns, split the dataset, or reset indexes - whichever makes the most sense to you.

### 2. Product mix

2.1. Visualise the product split two ways: by number of tanks, and by total capacity.

2.2. Which product category has the most tanks? By how much, in absolute terms, compared to the other categories?

2.3. Which product category has the largest total capacity? By how much, in percentage terms, compared to the other categories?

### 3. CAPEX spending

3.1. What is the total CAPEX spend planned across the whole FY25–FY34 forecast period?

3.2. Which financial year has the highest planned CAPEX spend?

3.3. What percentage of total tank capacity receives CAPEX spend at some point during the forecast period?

3.4. Which 10 tanks have the highest CAPEX spend per m³ of capacity?

3.5. How many tanks receive CAPEX spend in each year? Which year spreads spend across the most tanks?

### 4. Operational status

4.1. How many tanks are currently operational, as of December 2024?

4.2. You also have historical availability data for each tank. Using it, how many tanks went offline in each month, historically?

4.3. How many tanks are forecast to be available (in operation) in each month of the forecast period?

4.4. What total tank capacity is available in each month?

4.5. Break the available capacity from 4.4 down by product category.

4.6. Take this further: aggregate available capacity by quarter and by year, averaging across each period's months based on tank availability.
