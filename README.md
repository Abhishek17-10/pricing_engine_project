# 💰 Dynamic Pricing Engine

This project adjusts product prices based on stock levels and recent sales to optimize revenue while ensuring a minimum profit margin.

---

## 📂 Input Files

- `products.csv` – Product details: SKU, current price, cost price, stock.
- `sales.csv` – Sales data: SKU and quantity sold (last 30 days).

---

## 📊 Pricing Rules

Applied in this order:

1. **Low Stock, High Demand**: stock < 20 and quantity_sold > 30 → price ↑ 15%
2. **Dead Stock**: stock > 200 and quantity_sold == 0 → price ↓ 30%
3. **Overstocked**: stock > 100 and quantity_sold < 20 → price ↓ 10%
4. **Minimum Profit**: Ensure final price ≥ 120% of cost price

---

## 📤 Output

- `updated_prices.csv` – Contains:
  - `sku`
  - `old_price` (₹)
  - `new_price` (₹)

---

## 🧪 How to Run

Run the Jupyter notebook `pricing_engine.ipynb` after placing `products.csv` and `sales.csv` in the same folder.

---
