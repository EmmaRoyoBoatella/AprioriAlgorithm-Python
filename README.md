# Apriori-Based Association Rule Mining on Retail Transactions

## 1. Introduction
   This project applies the Apriori algorithm to a real-world market-basket dataset (`market_basket.csv`) containing 7 500 customer transactions, each with up to 20 items drawn from 120 unique products. By mining frequent itemsets and extracting high-confidence association rules, the analysis uncovers product affinities that can inform cross-selling and promotional strategies.

## 2. Project Structure

   * **Library Imports:** Load `pandas`, `numpy`, `mlxtend`, `matplotlib` and `scikit-learn` for data handling, algorithm implementation and visualization.
   * **Dataset Loading & Parsing:** Read `market_basket.csv` as a list-of-lists—each row represents one basket of variable length—and identify the 120 distinct product names.
   * **One-Hot Encoding:** Transform the list-of-lists into a binary transaction matrix (7 500 × 120), where each column indicates the presence or absence of a product in a given basket.
   * **Exploratory Analysis:** Compute basket-size distributions, plot item-frequency histograms, and analyze co-occurrence counts to guide selection of support and confidence thresholds.
   * **Apriori Implementation:** Generate all frequent itemsets above a user-specified minimum support; then derive association rules filtered by minimum confidence and lift.
   * **Parameter Tuning & Evaluation:** Systematically vary support and confidence parameters, evaluate rule sets by lift and rule count, and select settings that balance rule quality with interpretability.
   * **Results Visualization:**

     * Scatter plot of support vs. confidence for all discovered rules.
     * Bar chart of the top 20 rules sorted by lift.
     * Heatmap showing support, confidence and lift for a selected subset of rules.
   * **Business Insights:** Interpret the strongest rules to recommend product-bundling and targeted promotions.

## 3. How to Run the Project

   * **Environment:** Python 3.8+ (Jupyter Notebook or any standard Python interpreter).
   * **Dependencies:**

     ```bash
     pip install pandas numpy mlxtend matplotlib scikit-learn
     ```
   * **Execution:**

  1. Clone the repository and install dependencies via `pip install -r requirements.txt` or just download the Notebook `AprioriAlgorithm.ipynb`.
  2. Upload the datasets `market_basket.csv`.
  3. Launch `AprioriAlgorithm.ipynb` and run all cells sequentially.

Feel free to change the hyperparameters in order to find the best SOM!

## 4. Dataset Availability

   * **Raw Transactions:** `market_basket.csv` (7 500 baskets, up to 20 items each).
   * **Original Source & Licensing:** See `README.md` for provenance and usage terms.
