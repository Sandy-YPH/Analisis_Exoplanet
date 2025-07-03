# Analisis_Exoplanet
Analisis exoplanet NASA untuk mencari planet paling mirip Bumi menggunakan Earth Similarity Index (ESI). Proyek ini mencakup pembersihan data, normalisasi, perhitungan skor kemiripan, clustering, dan visualisasi. Hasil utama disimpan dan divisualisasikan dalam grafik dan tabel.

# 🌍 Exoplanet Earth Similarity Index (ESI) Analysis

This project analyzes exoplanets from NASA's Exoplanet Archive to find those that are most similar to Earth based on key features such as mass, radius, orbital period, and host star characteristics. It applies the **Earth Similarity Index (ESI)** formula, clusters the planets, and visualizes the most Earth-like candidates.

## 📁 Project Structure
├── exoplanet_notebook.ipynb # Main analysis notebook
├── outputs/ # Contains all generated charts and tables
│ ├── top10_planet.csv
│ ├── top10_similarity_barplot.png
│ ├── radar_chart_<planet>.png
│ ├── full_similarity_result.csv
│ ├── cleaned_data.csv
│ └── pca_clustering.png
└── README.md


## 📊 Features Used

- `pl_bmasse`: Planet mass (in Earth masses)
- `pl_rade`: Planet radius (in Earth radii)
- `pl_orbper`: Orbital period (in Earth days)
- `st_teff`: Stellar effective temperature (in Kelvin)
- `st_rad`: Stellar radius (in Solar radii)

## 🧮 Similarity Score

We used the **Earth Similarity Index (ESI)** formula:

\[
ESI = \prod_i \left(1 - \left|\frac{x_i - x_{earth}}{x_i + x_{earth}}\right|\right)^{w_i}
\]

- Where \( x_i \) = planet feature value  
- \( x_{earth} \) = Earth's value for that feature  
- \( w_i \) = weight for feature \( i \)

### Feature Weights (based on scientific references):
| Feature     | Weight |
|-------------|--------|
| Mass        | 0.57   |
| Radius      | 0.57   |
| Orbital Period | 0.30 |
| Star Temp   | 5.58   |
| Star Radius | 0.50   |

## 📌 Key Results

- Top 10 planets most similar to Earth saved in `outputs/top10_planet.csv`
- Visualizations: bar chart, radar chart, PCA clustering
- ESI scores and clustering are based on real data from the NASA Exoplanet Archive

## 📦 Tools & Libraries

- `Pandas`, `NumPy`
- `Matplotlib`, `Seaborn`
- `Scikit-Learn` for normalization and clustering
- `SciPy` for statistical analysis

## 🌐 Live Web Visualization (Coming Soon)
A Streamlit-based modern website is being developed to:
- Display the analysis results interactively
- Allow users to explore top planets
- View visual explanations for each chart
- Visit (https://github.com/Sandy-YPH/exoplanet-esi)

## 📄 Data Source

- [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/)
- The dataset used in this project was downloaded in July 2025.

## 📚 References

- Schulze-Makuch, D., et al. (2011). *A Two-Tiered Approach to Assessing the Habitability of Exoplanets*. Astrobiology.
- [NASA Exoplanet Archive Documentation](https://exoplanetarchive.ipac.caltech.edu/docs/)

---

## ✅ How to Run

1. Upload the `.ipynb` to [Google Colab](https://colab.research.google.com/)
2. Upload your NASA CSV dataset when prompted.
3. Run all cells to process, analyze, and save results.
4. Check the `outputs/` folder for results.

---

> Created with ❤️ by Sandy Yoga Prakasa Holley  
> GitHub: [Sandy-YPH](https://github.com/Sandy-YPH)

