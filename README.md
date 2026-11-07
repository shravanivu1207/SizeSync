# SizeSync (Version 1.0)

A lightweight, deterministic web utility designed to solve apparel sizing inconsistencies across major clothing retail brands. The application maps proprietary brand metrics (such as flat half-chest measurements and collar scales) to a normalized "To-Fit Body Chest" standard, providing cross-brand size recommendations for men's woven button-down shirts.

---

## Live Demo
Check out the live application: **[https://shravanivu1207.github.io/SizeSync/](https://shravanivu1207.github.io/SizeSync/)**

---

## The Problem
E-commerce fashion sizing suffers from inconsistent reference standards:
- Some brands report **body circumference** (e.g., to-fit 38"–40").
- Others report **flat garment dimensions** (e.g., pit-to-pit half-chest in cm).
- Formal labels rely on **numeric collar neck sizing** (e.g., 38, 39, 40, 42).

Shoppers typically need a tape measure or must fill out lengthy multi-step surveys to find their size, resulting in sizing confusion and high return rates.

---

## Engineering Solution
Instead of requiring physical measurements or invasive body profiling questionnaires, this engine operates as a direct brand-to-brand converter:
1. **Reference Size Input:** Accepts a known, well-fitting shirt size from a reference brand.
2. **Intermediate Normalization:** Resolves the source tag to a normalized **To-Fit Body Chest Midpoint** (in inches) by accounting for woven fabric ease.
3. **Fit Ease Translation:** Adjusts the target chest profile based on the selected silhouette (`Slim`, `Regular`, `Relaxed`).
4. **Target Matching:** Maps the target body chest to the destination brand's sizing intervals and displays fit confidence (sweet spot vs. borderline/snug edge).

---

## Supported Brands (Version 1.0)

| Brand | Measurement Standard | Size System |
| :--- | :--- | :--- |
| **Levi's** | Garment Half-Chest / Body Range | Alpha (`XS` – `XXL`) |
| **H&M** | European Body Chest & Length Split | Alpha (`XS` – `XXL`) + Regular/Long |
| **U.S. Polo Assn. (USPA)** | Body Circumference | Alpha (`S` – `XXL`) |
| **Peter England** | ABFRL Neck / Garment Chest | Numeric Collar (`38` – `46`) |
| **Allen Solly** | ABFRL Finished Garment Circumference | Numeric / Fit Split (`38` – `46`) |

---

## Tech Stack
- **HTML5 & CSS3:** Responsive UI with custom styling and confidence indicators.
- **Vanilla JavaScript (ES6):** Deterministic normalization engine, dynamic DOM selectors, and boundary-matching algorithms.
- **Hosting:** GitHub Pages.

---

## How to Run Locally

1. Clone the repository:
   ```bash
   git clone [https://github.com/shravanivu1207/SizeSync.git](https://github.com/shravanivu1207/SizeSync.git)