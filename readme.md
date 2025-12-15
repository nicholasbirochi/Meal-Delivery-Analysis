# Meal Delivery Orders Analysis — Pandas & NumPy

A study notebook that combines meal orders with a menu table to explore quantities, revenue, categories and monthly patterns. The analysis uses Pandas and NumPy, with the calculations and intermediate checks kept together in `main.ipynb`.

## Project goals

- Perform exploratory data analysis (EDA)
- Engineer new features (item revenue)
- Handle missing values (fill + drop strategy)
- Aggregate results by item and category
- Analyze trends over time
- Calculate core business KPIs (NumPy)
- (Optional) Compute percentiles with NumPy

## Datasets

This project expects two CSV files inside the `data/` folder:

- `data/pedidos.csv`
  - `Data` (order date)
  - `Item` (ordered item)
  - `Quantidade` (quantity)
  - `Preco_Unitario` (charged unit price)
  - plus identifiers like `ID_Pedido`, `Cliente_ID`
- `data/cardapio.csv`
  - `Item`
  - `Categoria` (Salgados, Bebidas, Sobremesas/Doces, etc.)
  - `Preco_Base` (base price)

### macOS extraction note (important)

If you extracted the datasets on macOS, your zip may also contain:
- `data/__MACOSX/`
- `data/__MACOSX/._pedidos.csv`
- `data/__MACOSX/._cardapio.csv`

These are **metadata artifacts** and should be ignored.
(Recommended: add `__MACOSX/` and `._*` to your `.gitignore`.)

## Tech Stack

- Python 3.x
- Pandas
- NumPy
- Matplotlib (basic chart)

## How to run

1) Install dependencies:
   pip install pandas numpy matplotlib

2) Open the notebook in Jupyter / Google Colab / VS Code Notebook.

3) Ensure your project structure matches the following (or adjust the paths inside the notebook):

```text
   .
   ├── main.ipynb
   ├── readme.md
   └── data/
       ├── pedidos.csv
       ├── cardapio.csv
       └── __MACOSX/ (optional; ignore)
           ├── ._pedidos.csv
           └── ._cardapio.csv
```

4) Run the notebook cells in order.

## What the notebook delivers

- `Receita_Item` = `Quantidade * Preco_Unitario`
- Missing values report and cleaning
- Item-level aggregation:
  - total quantity sold
  - total revenue
  - top 5 items by quantity and by revenue
- Time analysis:
  - revenue by month
  - trend plot
- Merge with menu data:
  - revenue by category
  - top revenue category
- Filters:
  - category == 'Salgados' and quantity > 10
- KPIs (NumPy):
  - Total Revenue
  - Total Items Sold
  - Average Ticket (Total Revenue / number of orders)
  - (Optional) percentiles for unit price and quantity

## License

Original code and documentation are covered by [MIT](license). Source datasets and third-party materials keep their own terms. The existing Rocketseat copyright notice is preserved in LICENSE.

MIT License

Copyright (c) Rocketseat

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

---
Made with 💜 by Rocketseat 👋
