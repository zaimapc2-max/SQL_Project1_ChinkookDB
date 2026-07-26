
# Sales Data SQL Analysis — Chinook Database

A SQL + pandas analysis of the Chinook database (a digital music store dataset), answering 10 real business questions using SQL queries executed against a SQLite database.

## About the Project

This project demonstrates the ability to turn raw relational data into business answers using SQL — the core skill behind data analysis work. Using the Chinook sample database, I explored customer spending, revenue by genre and country, sales trends over time, catalog performance, and employee sales — the kind of questions a real e-commerce or media business would ask of its data.

## Dataset

**[Chinook Database](https://github.com/lerocha/chinook-database)** — a sample database representing a digital media store, modeled after a real iTunes-style music catalog.

Key tables used:
- `Customer` — customer details
- `Invoice` / `InvoiceLine` — orders and line-item purchases
- `Track` / `Album` / `Artist` — the music catalog
- `Genre` / `MediaType` — track classification
- `Employee` — sales support reps

## Business Questions Answered

1. Which 5 genres generate the most revenue overall?
2. Who are the top 5 customers by total amount spent?
3. Which artist has the most tracks in the database?
4. What's the monthly sales trend over time?
5. Which country generates the most revenue?
6. What is the average invoice value, and which invoices are above average?
7. Which employees have the highest total sales through their supported customers?
8. Which tracks have never been purchased?
9. Which customers made only one purchase (never repeated)?
10. What's the most popular media type by number of tracks sold?

## Key Findings

- **Rock** is by far the top-earning genre, generating **$826.65** — more than double the next closest genre (Latin, $382.14).
- **Helena Holý** is the top spender at **$49.62**, closely followed by three other customers in the $45–48 range — spending is fairly concentrated at the top rather than dominated by one outlier.
- **Iron Maiden** has the most tracks in the catalog by a wide margin, at **213 tracks**.
- The **USA** is the highest-revenue market at **$523.06**, roughly 70% more than second-place Canada ($303.96).
- **Jane Peacock** is the top-performing sales rep, with **$833.04** in total sales through her supported customers.
- A striking **1,519 tracks** — a large share of the catalog — have never been purchased even once, suggesting a long tail of low-demand inventory.
- No customers made only a single purchase — every customer in the dataset has repeat orders, reflecting Chinook's relatively small, active customer base (59 customers, 412 invoices).
- **MPEG audio files** dominate sales by a huge margin (1,976 tracks sold) compared to all other media types combined.

## Tools Used

- **Python**
- **pandas** — for running SQL queries and displaying results as DataFrames
- **sqlite3** — for connecting to the Chinook SQLite database
- **Jupyter Notebook** — for combining queries, results, and explanations in one readable document

## How to Run

1. Clone this repository
2. Ensure you have `pandas` installed (`pip install pandas`)
3. Make sure `Chinook_Sqlite.sqlite` is in the same folder as the notebook (download it from the [Chinook database repo](https://github.com/lerocha/chinook-database) if not included)
4. Open `p1_notebook.ipynb` in Jupyter and run all cells

## Files

- `p1_notebook.ipynb` — the full analysis: 10 business questions, each with its SQL query, result, and a plain-English explanation
- `Chinook_Sqlite.sqlite` — the SQLite database used for analysis
- `README.md` — this file
