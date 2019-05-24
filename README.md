# DOTA Engine

Dota2 is the most played game on steam. Every day, millions of players worldwide enter battle as one of over a hundred DotA heroes. We thought it would be fun to analyze some Dota2 games using Python and give players some advices to win the battle. Then we decide to build a recommendation system which is helpful for players to have a better performance on this game.

The project was to see if we could build a recommendation system that would give user some guidance on a competitive DotA match by using data from other matches. By mining these history data, we can recommend some heroes and equipment. We believe data will make us stronger in the battles.


## Data Source

Data is collected through the Steam WebAPI. To get the data, you need a steam dev API. You can use mine,but it's better to apply your own key

## Instructions
### Install via source
First Install the dependencies below, based on your operating system, and then finally download the DOTA Engine source, e.g.
```
git clone https://github.com/wenyuyangpku/DOTA_Engine.git
```
Install  [Anaconda](https://docs.anaconda.com/anaconda/install/), which we will use as the environment manager. To install the requirements using [conda](http://conda.pydata.org/), run the following at the command-line:
```
$ conda install --file requirements.txt
```
To create a stand-alone environment named  `DOTA`  with Python 3.5 and all the required package versions, run the following:
```
conda env create -f environment.yml
conda activate DOTA
```

## Running the notebook
- 1_Get_Match_Data.ipynb
-  2_Read_Match_Data_and_Generate_Dataframe.ipynb
-  3_Data_Analysis.ipynb
-  4_Frequency_Pattern.ipynb
-  5_Prediction_Models.ipynb
-  6_Heroes_Recommendation.ipynb


## Authors
- **Wenyu Yang**: wenyuyang@gwu.edu
- **Tianyu Yang**: tyyang@gwu.edu

## License

   
This project is licensed under the MIT License. You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0


## Acknowledgments
This project is for CSCI 6443 Data Mining, Spring 2019.
Our group is guided by **[Abdelghani Bellaachia](mailto:bell@gwu.edu)** 
