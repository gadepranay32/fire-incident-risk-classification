# fire-incident-risk-classification
Here’s a `README.md` file you can use for your GitHub project:

---

# Fire Incident Risk Classification

This project provides a machine learning model for classifying fire incidents into risk levels (Low, Medium, High) based on factors such as fire size, response time, and number of casualties. It uses a decision tree algorithm and includes training, evaluation, and prediction for new data.

## Features
- Train a decision tree model on fire incident data.
- Evaluate the model's performance using a test dataset.
- Predict risk levels for new fire incident data.
- Save and load the trained model for reuse.

## Prerequisites
- R programming language installed on your machine.
- The following R packages:
  - `tidyverse`
  - `caret`
  - `rpart`
  - `rpart.plot`

Install the required packages using:
```R
install.packages(c("tidyverse", "caret", "rpart", "rpart.plot"))
```

## Project Files
- **`fire_incident_risk_classification.R`**: The main R script containing the complete code for training and prediction.
- **`fire_risk_model.rds`**: The saved model file (generated after training).
- **`README.md`**: Documentation for the project.

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/fire-incident-risk-classification.git
   ```
2. Open the R script `fire_incident_risk_classification.R` in R or RStudio.
3. Run the script step-by-step:
   - Train the model on simulated or real data.
   - Save the trained model (`fire_risk_model.rds`).
   - Predict risk levels for new data.

4. Modify the `new_data` section in the script to include your own data for predictions.

## Sample Output
For the following new data:
```R
new_data <- data.frame(
  IncidentType = as.factor(c("Residential", "Commercial")),
  FireSize = c(2.5, 7.8),  # Fire size in hectares
  ResponseTime = c(15, 10),  # Response time in minutes
  NumberOfCasualties = c(1, 3)  # Number of casualties
)
```

The output risk levels might look like:
```R
  IncidentType FireSize ResponseTime NumberOfCasualties PredictedRisk
1 Residential     2.5           15                  1           Low
2  Commercial     7.8           10                  3          High
```

## Visualizing the Decision Tree
The model generates a visual representation of the decision tree using the `rpart.plot` package. This helps in understanding the classification process.

## License
This project is licensed under the MIT License. Feel free to use and modify it.

---
