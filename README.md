# TankMaster

A messy, semi-realistic tank terminal dataset for practicing real-world data cleaning and analysis.

## The Brief

You're a data analyst who has just joined the finance team at a bulk liquid storage company. The company operates a **tank terminal** — a facility that stores oil, fuel, and chemical products on behalf of customers before the products are shipped onward.

The operations team has sent over an export of their tank register. It's the kind of spreadsheet that's grown organically over the years: static tank details, multi-year financial forecasts, and monthly operational logs, all bolted together into one wide table by whoever needed it at the time. It works fine for them day-to-day, but it wasn't built with analysis in mind — and it shows.

Your manager needs clear answers to a handful of business questions before the next planning meeting. Before you can answer them, you'll need to make sense of the file yourself.

## What's in the File

Assume today's date is **December 2024**. Each row is one storage tank, and the columns fall into three groups:

1. **Tank details** — a tank ID, its capacity in cubic metres (m³), and the product category it's used to store (e.g. Crude, Gasoline, Diesel/Gasoil).
2. **Capital expenditure (CAPEX) forecast** — planned spend on each tank for financial years FY25 through FY34. A blank cell means no planned spend that year (treat it as 0).
3. **Operational availability, historical and forecast** — one column per month, running from several years ago through to FY34. A `1` means the tank was (or is expected to be) in operation that month; a `0` or blank means it wasn't. Don't discard the historical months — you'll need them later.

None of this is separated out for you — untangling it is your job. The questions below will guide you through reshaping the data and then using it to answer what the business actually wants to know.

## Questions

Work through these roughly in order — the first question has you reshape the data into a structure you'll reuse for everything that follows.

### 1. Reshaping the data

Before doing any analysis, restructure the dataset into something you can actually work with. The questions below will make more sense once you've done this — use them as a guide for what your reshaped data needs to support. Consider: should the CAPEX and availability data stay in the same table as the tank details, or be split out? Would a long ("tidy") format work better than the current wide one for the monthly and yearly columns? Rename columns and reset indexes however makes sense to you.

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

## Files

| File | Description |
|---|---|
| `tank.csv` | The raw, messy dataset — one row per tank. |
| `tank.ipynb` | Notebook containing the questions above, ready for you to fill in with your own analysis. |

## License

TBD.
