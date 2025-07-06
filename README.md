 House Price Predictor
 Features

 Predict house prices using features like:

  * Overall Quality
  * Living Area (in sq. ft)
  * Garage Capacity
  * Total Basement Area
 Interactive and user-friendly web interface
 Trained with a real dataset (`train.csv`)
 Model evaluation using Mean Squared Error (MSE)
 Deployment-ready with Flask

Tech Stack

 Frontend: HTML, CSS
 Backend: Flask (Python)
 Model: RandomForestRegressor (scikit-learn)
 Libraries: Pandas, NumPy, Joblib, scikit-learn

 Project Structure

```
├── app.py                  # Flask application
├── house_price_model.pkl   # Trained Random Forest model
├── train.csv               # Training dataset
├── templates/
│   └── index.html          # Frontend page with form
├── static/                 # (Optional) For additional CSS/JS if needed
└── README.md               # Project documentation
```

Model Training

The model is trained using the following features from the dataset:

 `OverallQual`: Overall material and finish of the house
 `GrLivArea`: Above ground living area (sq. ft)
 `GarageCars`: Size of garage in car capacity
 `TotalBsmtSF`: Total square feet of basement area

 Steps:

1. Load dataset using `pandas`
2. Select relevant features and handle missing values
3. Split into training and test sets
4. Train the model using `RandomForestRegressor`
5. Evaluate using `mean_squared_error`
6. Save the model using `joblib`

---

Running the Web App

Prerequisites

Python 3.x
Required packages:

  ```bash
  pip install flask pandas scikit-learn joblib numpy
  ```
 Run the App

```bash
python app.py
```

Visit `http://127.0.0.1:5000` in your browser.

---

How It Works

Users enter house features in the web form.
The Flask backend loads the trained model.
The input is processed and passed to the model.
The predicted house price is displayed on the same page.


UI Preview

![House Price Predictor UI](https://user-images.githubusercontent.com/placeholder/house-ui-preview.png) <!-- Replace with actual image or remove -->


Dataset

The model was trained using a subset of the **[Kaggle House Prices Dataset](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)**.

---

Future Enhancements

Add more features to improve prediction accuracy
Integrate model versioning and tracking
Deploy using Heroku or Docker
Include visual analytics of predictions

---

