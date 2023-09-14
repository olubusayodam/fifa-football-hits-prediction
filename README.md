# Fifa  Football Hits Prediction


----
## Project Objective:
The Fifa Football team is preparing for the next games season and has requested assistance in cleaning and preprocessing their data. The ultimate goal is to predict the number of hits by each player. This project involves data cleaning, preprocessing, feature engineering, and building a prediction model.



-----
## Data Sourcing
The dataset was obtained from an online football player database. It consists of detailed information about football players, including various attributes, contract statuses, playing positions, and performance metrics. The dataset was initially messy and required extensive cleaning. The data set is attached to this repository.
### Data Cleaning
The data cleaning process involved several crucial steps:
1. Player Name Extraction: Player names were extracted from the PlayerUrl column to create a new column named Player Name. This step was essential for better data understanding and analysis.
2. Player Status: A new column called Player Status was created based on the CONTRACT column. Player statuses were categorized into three labels: 'Active' for players with active contracts, 'Free' for free agents, and 'On Loan' for players on loan.
3. Position Unpacking: The POSITIONS column was unpacked into separate columns for each playing position, and Boolean values were assigned to indicate each player's positions.
4. Data Type Conversion: Several columns, including Weight, Height, W/F (Weak Foot), SM (Skill Moves), and IR (International Reputation), were converted to integers for consistency and easier analysis.
5. Value, Wage, and Release Clause: Columns related to financial aspects, such as Value, Wage, and Release Clause, were converted to floating-point numbers to facilitate numerical operations.
6. HITS Column: The HITS column was inspected and ensured to be in float format to prepare it as the dependent variable for prediction.
7. Outlier Detection and Treatment: Outliers in the data were identified and treated appropriately. Any extreme or erroneous values were adjusted or removed to prevent them from unduly influencing the predictive model.
8. Column Dropping: Some columns that were deemed irrelevant or redundant for predicting hits were dropped from the dataset to streamline and improve modeling efficiency.


----
### Data Transformation
To prepare the data for modeling, additional transformations were performed:
1. Feature Selection: Relevant features (independent variables) were selected for predicting the HITS column. This involved choosing attributes that could potentially influence a player's hits.
2. Data Splitting: The dataset was split into training and testing sets using a 70-30 split ratio. This allowed for model training and evaluation.
3. Regression Model Selection: A Linear Regression model was chosen for predicting the number of hits. This model was used as a starting point, but other regression models could be explored for potential improvement.
4. Model Training: The selected model was trained using the training dataset, with hits as the target variable and selected features as inputs.
5. Model Evaluation: The model's performance was evaluated using several metrics, including Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R2). The model achieved an MSE of 0.82, MAE of 0.76, and an R2 of 0.33.




----
## Findings & Recommendations
The project's key findings and recommendations are as follows:
Findings:
- The prediction model achieved a moderate level of accuracy, with an R-squared (R2) value of 0.33.
- The Mean Squared Error (MSE) was 0.82, indicating the model's predictive capabilities.
- The Mean Absolute Error (MAE) was 0.76, suggesting that the model's predictions are, on average, approximately 0.76 hits away from the actual values.
Recommendations:
- Further feature engineering and selection may improve prediction accuracy. Exploring additional features or external data sources could be beneficial.
- Consider experimenting with different regression models to identify one that provides better predictions.
- Regularly update the dataset to ensure that player information remains current and relevant.

This README provides an overview of the Fifa Football Hits Prediction project, from data sourcing and cleaning to modeling and evaluation. It serves as a documentation resource for anyone interested in understanding the project's objectives, processes, and outcomes.
