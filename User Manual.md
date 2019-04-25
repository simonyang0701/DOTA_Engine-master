# User Manual

## DOTA Recommendation Engine(  6_Heroes_Recommendation.ipynb)
### First Pick: please read 3_Data_Analysis for help
Here is part of the result. For current game version, Viper and Ursa are you best chioces
### Second Pick: please read 4_Frequency_Pattern for help
For second pick of 4th pick, your team have chance to pick two heroes. Here are some heroes combinations have hign win rate. It will help you to make decision
- Win rate of Crystal Maiden and Viper is	 64.41929133858267%
- Win rate of Viper and Lifestealer is	 64.04328578455485%
- Win rate of Lifestealer and Bounty Hunter is	 58.32780358327804%

### Later Pick: please read 5_Prediction_Models for help

Once you know some pick information, for example, more than 5 people have picked heroes. You can use our model to find your best choice

-   Logistic Regression:Accuracy 64%,Very Fast
-   KNN: Accuracy 62%, Very Slow
-   Random Forest: Accuracy 61%, Fast
-   XGBoost: Accuracy 66%, Fast
-   SVM: Accuracy 64%, Slow

Here we will use XGBoost as our recommendation model, you can also change it to other models

Give a team in format of a list of 10 number. The number is the heroes ID. 0 means this player hasn't pick a hero. The name of 0 is empty
```
team=[2,65,12,54,0,54,65,112,43,56]
Axe
Batrider
Phantom Lancer
Lifestealer
empty
Lifestealer
Batrider
Winter Wyvern
Death Prophet
Clinkz
```
Give your team called Radiant. If you are in Radiant team, Radiant = True. If you are in Dire team, Radiant = False
```
Radiant=True
```
Then DOTA Engine will give you the recommended Hereoes and the win probability
```
The win probability of Disruptor is 75.8919358253479%
The win probability of Viper is 71.5608537197113%
The win probability of Ursa is 71.49288654327393%
The win probability of Tidehunter is 71.03862762451172%
The win probability of Underlord is 70.16506791114807%
The win probability of Chaos Knight is 69.14011240005493%
The win probability of Razor is 68.83906126022339%
The win probability of Riki is 68.3645248413086%
The win probability of Warlock is 68.2816207408905%
The win probability of Bounty Hunter is 68.27802062034607%
```





## 1_Get_Match_Data.ipynb

This this the first part which is used to get the DOTA data. Basically, in this part you will use requests, steam API and match ID to get the detail of the match in JSON format.

### Here are some information you should notice

-   **Key**  is the steam dev API, you can use mine,but it's better to apply your own key.
-   The range(4479300000,4479300100) is the range of Match ID. Here is an example. To get more data, the range should be large. In my project, I spend more than 24 hours to get 120000 matches.
-   Please make sure you have a `data` directory.


## 2_Read_Match_Data_and_Generate_Dataframe
 This part is used to read and decode the JSON data to a dataframe.
Do some data cleaning. Including omitting NaN and removing robot played match. Add a column called win_score.
Read match data and heroes data to df_match and df_heroes. Contat df_match and df_heroes. Then save the dataframe to "out.csv"

## 3_Data_Analysis.ipynb

 This part is to do data analisis. Including win_rate, duration, high win_rate heroes. We use bokeh to visualize the data.


## 4_Frequency_Pattern.ipynb

This part will show you which combination of heroes has high win rate or low win rate.
Use apriori find the frequency parttern, then calculate the win rate of these patterns.


## 5_Prediction_Models.ipynb

This part is to train the prediction model. We use Logistic Regression, KNN, Random Forest, XGBoost and SVM to train models.

First, build feature vectors. Translate Heroes ID to Vector. Then build training dataset and test dataset

### Here are the results of 5 kinds models
- Logistic Regressio: Accuracy is 64%, Very fast
- K Nearest Neighbors: Accuracy 62%, Very  slow
- Random Forest: Accuracy 61%, Fast
- XGBoost Model: Accuracy 66%, Fast
- Support Vector Machine: Accuracy 64%, Slow






## Authors
- **Wenyu Yang**: wenyuyang@gwu.edu
- **Tianyu Yang**

## License

   
This project is licensed under the MIT License. You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0


## Acknowledgments
This project is for CSCI 6443 Data Mining, Spring 2019.
Our group is guided by **[Abdelghani Bellaachia](mailto:bell@gwu.edu)** 
