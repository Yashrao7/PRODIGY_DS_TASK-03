📘 Project Description: The objective of this project is to build a machine learning model that can accurately predict whether a customer will complete a purchase on an e-commerce platform based on their demographic characteristics and online behavioral patterns.

We utilize the publicly available Online Shoppers Purchasing Intention Dataset, which captures real-world user session data from an e-commerce website. The dataset consists of over 12,000 sessions and includes a variety of features such as:

Behavioral Data:

Number of administrative, informational, and product-related pages visited

Duration spent on each type of page

Bounce rate and exit rate

Page value and special day indicators

Demographic & Temporal Features:

Month of the session

Whether the session occurred on a weekend

Visitor type (e.g., returning visitor or new)

Target Variable:

Revenue: A boolean value indicating whether the user ultimately completed a purchase (1 for yes, 0 for no)

🔧 Methodology: Data Preprocessing:

Checked for and handled missing values (dataset was clean)

Converted categorical variables (Month, VisitorType, Weekend) into numerical format using label encoding

Converted the target variable Revenue to integer for binary classification

Feature Engineering:

All 17 features in the dataset were used, including behavioral metrics, visitor type, and timing information

No additional feature creation was needed due to the rich nature of the original dataset

Modeling:

The dataset was split into training and testing sets (70%/30%) using stratified sampling to preserve class distribution

A Decision Tree Classifier was trained with a maximum depth of 5 to prevent overfitting and improve interpretability

Hyperparameters such as max depth and split criteria can be tuned further for optimization

Model Evaluation:

The model's performance was evaluated using accuracy, precision, recall, F1-score, and a confusion matrix

The decision tree was visualized using sklearn.tree.plot_tree() to provide a clear interpretation of the decision paths

📈 Results: The decision tree classifier was able to predict customer purchase intent with good accuracy, offering interpretable rules for determining the likelihood of a purchase.

Features such as PageValues, ExitRates, and ProductRelated_Duration were found to be the most informative indicators of customer intent.

The model demonstrated a balance between performance and explainability, making it suitable for use in decision-support systems within marketing and UX teams.

🎯 Applications: This model can be integrated into real-time recommendation engines or customer segmentation systems to:

Target high-intent customers with personalized offers or retargeting ads

Identify and assist at-risk users who are likely to abandon the session

Improve conversion rates by adapting content dynamically based on session behavior
