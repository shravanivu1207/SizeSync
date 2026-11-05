# SizeSync — Shirt Size Bridge 👕

> Direct, zero-tape size converter across major menswear brands (Levi's, H&M, U.S. Polo Assn., Peter England).

🔗 **Live Demo:** [https://shravanivu1207.github.io/SizeSync/](https://shravanivu1207.github.io/SizeSync/)

---

## 💡 The Problem

Online apparel sizing is broken by **vanity sizing** and **inconsistent measurement grading**:
- A Medium in **Levi's** (American classic drape) fits noticeably larger than a Medium in **H&M** (European slim cut).
- Formal brands like **Peter England** use numbered collar sizing (`38, 39, 40, 42`), leaving shoppers guessing their letter equivalents.
- Asking customers to retrieve a tailor's tape measure introduces high drop-off and friction.

---

## ⚡ The Solution: "Closet-Match" Architecture

SizeSync avoids physical measuring tapes entirely:
1. **Body-Anchor Engine:** The user inputs an existing, well-fitting shirt (`Brand` + `Size` + `Fit`).
2. **Reverse Garment Ease Deduction:** The engine computes the wearer's estimated bare-chest circumference by stripping out garment wearing ease allowances.
3. **Target Calibration:** The anchor measurement is projected onto the target brand's official pattern grading to determine the optimal tag size.
4. **Fit Confidence Gauge:** Shows where the user sits within the recommended size bracket (Roomy/Lean, Optimal Center, or Borderline Snug).

---

## 🏷️ Supported Brands

| Brand | Origin / Cut Style | Sizing Scheme |
|---|---|---|
| **Levi's** | American Classic Drape | Alpha (`XS` – `XXL`) |
| **H&M** | European Tailored Silhouette | Alpha (`XS` – `XXL`) + Height Cut |
| **U.S. Polo Assn.** | Athletic Broad Chest | Alpha / Metric Collar (`38` – `46`) |
| **Peter England** | Formal Slim / Standard Torso | Indian Collar Scale (`36` – `46`) |

---

## 🛠️ Tech Stack

- **Frontend:** Vanilla HTML5, JavaScript (ES6+)
- **Styling:** Tailwind CSS (Utility-first styling, Mobile-First Dark Theme)
- **Deployment:** GitHub Pages

---

## 🚀 Running Locally

Clone the repository and open `index.html` in your browser:

```bash
git clone [https://github.com/shravanivu1207/SizeSync.git](https://github.com/shravanivu1207/SizeSync.git)
cd SizeSync
# Open index.html directly or launch via Live Server