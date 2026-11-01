# resturent-management# Restaurant Management System

A simple Streamlit app for managing a restaurant: menu, orders, customers, tables,
inventory, and sales reports. Prices are in PKR.

## Features

- **Dashboard** – revenue, order counts, low-stock alerts, daily/monthly sales, best sellers
- **Menu** – add, edit, delete, search, and export items; link items to ingredients
- **Orders** – create orders with discount and tax, track status, view bills
- **Customers** – register, edit, view order history and total spend
- **Tables** – manage seating; tables are released when an order completes or is cancelled
- **Inventory** – stock in/out, minimum-stock alerts; stock is deducted on order and restored on cancel
- **Reports** – date-range sales, weekly/monthly trends, category sales, CSV export

## Run locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

The app opens at http://localhost:8501.

## Deploy to Streamlit Community Cloud

1. Push `app.py`, `requirements.txt`, and `README.md` to a GitHub repository.
2. Go to https://share.streamlit.io and choose **New app**.
3. Select the repository, branch, and set the main file to `app.py`.
4. Click **Deploy**.

## Data storage

Data is saved to `restaurant_data.json` next to `app.py`, created automatically on
first run. On Streamlit Community Cloud this file can be erased whenever the app
restarts, so use the CSV export buttons for backups, or move to a hosted database
(for example Supabase or Google Sheets) if you need permanent storage.

## Project structure

```
app.py             # the whole application
requirements.txt   # Python dependencies
.gitignore         # keeps the local data file out of git
README.md          # this file
```
