🌧️ Rainfall Data Imputation using Random Forest (RFD)

This project applies a **Random Forest Regressor** to impute missing rainfall values in a dataset.  
The model leverages **date-based features** (day of year, month, and day of month) and uses **hyperparameter optimization** with `RandomizedSearchCV` to achieve accurate predictions.

---

📌 Features
- Cleans and preprocesses the dataset (handles missing rainfall values).
- Extracts date-based features for better predictive performance.
- Uses **Random Forest Regression** to predict missing rainfall values.
- Performs **hyperparameter tuning** with `RandomizedSearchCV`.
- Evaluates model performance with **Mean Absolute Error (MAE)**.
- Outputs an **imputed dataset** (`data_imputed.xlsx`) with no missing rainfall values.


📂 Project Structure
```
.
├── randomforest(rfd).py    # Main Python script
├── Kurudamannil_RFD.xlsx   # Input dataset (not included in repo for privacy)
├── data_imputed.xlsx       # Output dataset after imputation (generated)
└── README.md               # Documentation

```

## ⚙️ Requirements
Install the required Python libraries:

```bash
pip install pandas numpy scikit-learn openpyxl
````

🚀 Usage

1. Place your rainfall dataset (Excel file) in the project directory.
   Example: `Kurudamannil_RFD.xlsx`

2. Run the script:

   ```bash
   python randomforest(rfd).py
   ```

3. The script will:

   * Preprocess the dataset
   * Train and tune the Random Forest model
   * Impute missing rainfall values
   * Save the completed dataset as `data_imputed.xlsx`


📊 Model Evaluation

The model evaluates imputation accuracy using **Mean Absolute Error (MAE)**:

* Training MAE ≈ *9.28*
* Validation MAE ≈ *10.38*

This indicates reasonable performance for rainfall data imputation.


🛠️ Techniques Used

* **Random Forest Regressor** (`sklearn.ensemble`)
* **Hyperparameter Optimization** (`RandomizedSearchCV`)
* **Evaluation Metric**: Mean Absolute Error (MAE)
* **Excel I/O** (`pandas`, `openpyxl`)


📌 Notes

* Accuracy may vary depending on the variability of rainfall data.
* Domain expertise is recommended for setting acceptable MAE thresholds.
* The script is optimized for **daily rainfall datasets** with a `Date` and `Rainfall` column.


📜 License

This project is licensed under the MIT License – feel free to use and modify it.


```

---

Would you like me to also **add usage examples with sample input/output tables** (showing before & after imputation) inside the README, so it’s clearer for new users?
```
