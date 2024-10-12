# Bangalore Home Prices Prediction Model

This repository contains a machine learning project for predicting home prices in Bangalore using linear regression. The model is trained on various features, including location, square footage, number of bathrooms, and number of bedrooms.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Model Evaluation](#model-evaluation)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)

## Installation

To set up the project environment, make sure you have Python 3.6 or higher installed. Then, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/AmaanAhmad2025/bangalore-home-prices-prediction.git
   cd bangalore-home-prices-prediction
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Load the model**:
   The trained model can be loaded using the following code:
   ```python
   import pickle

   with open("banglore_home_prices_model.pickle", "rb") as f:
       model = pickle.load(f)
   ```

2. **Make predictions**:
   You can predict the price of a house by using the `predict_price` function. For example:
   ```python
   price = predict_price("1st Phase JP Nagar", 1000, 2, 2)
   print(f"Predicted Price: {price}")
   ```

## Model Evaluation

The model's performance is evaluated using various metrics, including:

- **R² Score**: The model achieved an R² score of approximately 0.875 on the test set.
- **Cross-Validation**: The model was validated using ShuffleSplit cross-validation with scores ranging from 0.771 to 0.850 across different folds.

## Features

- Location: Categorical variable representing different neighborhoods in Bangalore.
- Square Footage: Continuous variable representing the size of the house.
- Number of Bathrooms: Integer variable for the count of bathrooms.
- Number of Bedrooms (BHK): Integer variable for the count of bedrooms.

## Contributing

Contributions are welcome! If you have suggestions or improvements, please create a pull request or open an issue.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
