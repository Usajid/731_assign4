
Major Leagues (Assignment # 04- EECS 731)
==============================


### Quick Note:
If you are interested in only looking at notebook, please access the notebook in **/notebooks/majorLeague.ipynb**.

/notebooks: Contains the notebook of this assignment.

/data: Contains the data csv file (nfl_games.csv)

### Objective:

<ul>
<li>Pick one dataset from given various leagues like NFL, MLB, NBA and Soccer</li>
<li>Do feature engineering as a pre-process for regression modeling</li>
<li>Do regression based modeling to determine scores of each team</li>
</ul>

### Dataset:

I used the NFL dataset for this regression modeling assignment. (Data csv file is in /data/nfl_games.csv)

### Process:

<ul>
<li>First I did feature engineering. Main feature engineering includes combining/addition of features, and removing redundant/irrelevant features. Please refer to notebook for more details.</li>
<li>Divided the dataset into training/testing split of 80/20 percentage.</li>
<li>Trained three regression models separately on the training dataset.</li>
<li>Finally, evaluated above trained models on testing dataset under three evaluation metrics.</li>
</ul>

### Discussion and Results:
Since we have to regress scores for both teams (multi-output regression), so I used MultiOutputRegressor module of scikit-learn. Using this module, it outputs multiouput regression values using given Regression model. For this assignment, I trained and evaluated three regression models as follows:

<ul>
<li>Random Forest Regressor</li>
<li>XGBoost Regressor</li>
<li>Linear Regessor</li>
</ul>

Once above regressors were trained, we evaluted them separately on three evluation metrics,as follows:

<ul>
<li>Mean Absolute Error (MAE)</li>
<li>Mean Squared Error (very good in telling about the variance in result values, so more desirable metric)</li>
<li>Scikit Regression Score (Maximum value = 1.0f) </li>
</ul>

The evaluation results for three regressors are as follows:

**Random Forest Regressor:**

MAE: 4.54832675696375

MSE: 36.48255827784976

Multi Target Output Random Forest Based Regressor Score: 0.701

**XGBoost Regressor:**

MAE: 6.956283390349816

MSE: 77.05458382962796

Multi Target Output XGBoost based Regressor Score: 0.37

**Linear Regressor:**

MAE: 7.233133556966823

MSE: 82.39727180323428

Multi Target Output Linear Regressor Score: 0.326

After training and evaluating three regression models (Random Forest, XGBoost, Linear Regressor), in MultiouputRegressor mode, we found that Random Forest based approach performs the best on all three evaluation metrics (**Mean Absolute Error (MAE):4.54832675696375, Mean Squared Error:36.48255827784976, Regression Score:0.701**). Feature Engineering, including combining and removing different features, also played an important role in improving the overall effectiveness of the system. Please see /notebooks/majorLeague.ipynb for more details.






