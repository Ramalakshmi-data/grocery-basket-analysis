# Dark Store Shelf Planner

**Which grocery categories get bought together, and how should a dark store lay out its aisles so pickers walk less?**

![Dark Store Shelf Planner](images/cover.png)

I analysed **8,902 grocery order lines from 100 customers** to find which product categories are purchased together, then turned the results into two interactive tools: a correlation heatmap and a drag-and-drop aisle planner.

🔗 **Live demo:** https://ramalakshmi-data.github.io/grocery-basket-analysis/

> Independent portfolio project. Not affiliated with, or endorsed by, Woolworths or any retailer.

---

## Key findings

| Finding | Categories | Correlation (r) |
|---|---|---|
| 🍝 Strongest link in the dataset | Pasta ↔ Pasta Sauce | 0.96 |
| 🥛 Tight "breakfast basket" | Milk, Bread, Eggs | 0.61 – 0.79 |
| 👶 The "parent shop" cluster | Diapers, Wet wipes, Chocolates | 0.58 – 0.78 |
| 🌮 Weaker than expected | Nachos ↔ Salsa | 0.48 |

**What it means for a store:** categories with strong links should sit in the same or neighbouring aisles. The surprise is chocolate: it belongs near the baby aisle, not just at the checkout.

---

## The tools

### 📊 [Correlation heatmap](https://ramalakshmi-data.github.io/grocery-basket-analysis/heatmap.html)
Pearson correlation of per-customer category spend for every category pair. Hover or tab through cells for details.

### 🛒 [Drag-and-drop floor planner](https://ramalakshmi-data.github.io/grocery-basket-analysis/planner.html)
- Aisles start **seeded by clustering**, grouping categories that are bought together.
- Drag categories between aisles to try your own layout, or search for a product to find its aisle.
- A live **"togetherness score" (0–100)** shows how well the layout keeps co-purchased items close.

| Layout | Togetherness score |
|---|---|
| Data-driven (clustered) layout | **85 / 100** |
| Move Salsa into the breakfast aisle | 75 / 100 |

---

## How it was built

1. **Data preparation (Python, pandas):** cleaned 8,902 order lines and totalled each customer's spend by category.
2. **Correlation analysis:** calculated the Pearson correlation (r) between every pair of categories.
3. **Clustering:** grouped strongly linked categories to create the starting aisle layout.
4. **Interactive front end (plain JavaScript):** built the heatmap and floor planner with no frameworks or external libraries. Each page is a single self-contained HTML file.

### Accessibility
- Works on phone and desktop
- Fully usable with a keyboard
- Screen-reader friendly (WCAG AA)

---

## Tools
`Python` · `pandas` · `JavaScript` · `HTML` · `CSS`

## Project structure
```
├── index.html      # project home page
├── heatmap.html    # correlation heatmap
├── planner.html    # drag-and-drop floor planner
├── images/
│   └── cover.png   # cover image
└── README.md
```

## About me
I'm **Ramalakshmi**, a data analyst in Adelaide who turns messy data into clear dashboards and decisions.

- Portfolio: [ramalakshmi-data.github.io](https://ramalakshmi-data.github.io)
- GitHub: [github.com/Ramalakshmi-data](https://github.com/Ramalakshmi-data)
