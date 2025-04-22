Big-mart-sales-prediction
This project aims to predict the Item Outlet Sales for products sold at different Big Mart stores using a variety of features related to the product and the store. The dataset contains both product-level and outlet-level information.
Predict the sales of products at various retail outlets using machine learning models.

📌 Project Overview
This project aims to predict the Item Outlet Sales for products sold at different Big Mart stores using a variety of features related to the product and the store. The dataset contains both product-level and outlet-level information.

📂 Dataset
The dataset includes two files:

Train_UWu5bXk.csv: Contains training data with target column Item_Outlet_Sales.

Test_u94Q5KV.csv: Test data without the target, for which predictions are to be made.

🔑 Features

Column	Description
Item_Identifier	Unique product ID
Item_Weight	Weight of the product
Item_Fat_Content	Product's fat content (Low Fat / Regular)
Item_Visibility	Display area of the product in store
Item_Type	Category of the product
Item_MRP	Maximum Retail Price
Outlet_Identifier	Unique store ID
Outlet_Establishment_Year	Year of establishment
Outlet_Size	Store size (Small/Medium/High)
Outlet_Location_Type	Store's city tier
Outlet_Type	Type of store (Grocery/Supermarket)
Item_Outlet_Sales	Target variable (only in training data)
🧹 Data Preprocessing
Merged train and test datasets for uniform preprocessing.

Cleaned inconsistent labels in Item_Fat_Content.

Imputed missing values:

Item_Weight: mean imputation.

Outlet_Size: mode imputation.

Dropped unique identifiers: Item_Identifier, Outlet_Identifier.

Encoded categorical variables using One-Hot Encoding.

Split dataset into train-validation sets (80-20).

🧠 Models Used
Linear Regression

Random Forest Regressor

XGBoost Regressor

Each model is wrapped in a pipeline with preprocessing steps using scikit-learn.

📈 Evaluation Metric
RMSE (Root Mean Squared Error) on validation set.
