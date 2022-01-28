# Pump it Up: Data Mining the Water Table
## Flatiron Phase 3 Data Science Project

Brad Blackwood 

2021-01-28

##### Buisness Problem: 

The Tanzanian Ministry of Water is faced with the problem that many of the water pumps in the country require maintinance. The people of Tanzania rely on these water pumps to provide clean drinking water to their communities. The Tanzanian Ministry of Water if faced with time and resource contrainsts that they want to optimize useing a Machine Learning Model.

##### Data

~ 60,000 rows
~ 40 columns

* Primarily catagorical Data
* Target variable was determined to be multiclass (functional, functional needs repair, non functional)
* Goal was to determine pumps that required attention, so needs repair and non functional were grouped to make a binary classification.
* EDA showed that columns contained repetative/incomplete data.
* Columns were then selectively dropped to improve processing time/ decrease complexity
* Features were then One Hot Encoded to incorporte the categorical variables.

##### Modeling

The Buisness problem identified ***Recall*** as the comparision method to optimize. Providing clean drinking water to humans is the highest priority.

Time are resource constraints also led modelig ***precision*** to also be considered. 

Models considered
* Naive Bayes
* K Nearest Neighbors
* Random Forest (with hyper parameter tuning)
* XGBoost (with hyper parameter tuning)
* SVM (with hyper parameter tuning)

Best Model = Random Forest Classifier with Hyper Parameter tuning

Reasoning
* Resonable training/testing time
* Highest Recall score ~0.73
* Decent Precision ~0.80

##### Conclusion

* The RFC is better then no model/other models tested
* It is better at maximizing the resource usage (Precision)
* It misses Non Functioning pumps which should be compensated with other method.