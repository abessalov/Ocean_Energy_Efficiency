<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

# Report of Ocean Protocol :: Energy Efficiency Data Challenge

## 1. Data cleaning and preprocessing
_More details you can find in the scripts 0_Data_preprocessing.ipynb and 1_Geodata_parsing.ipynb_
- Correct some data types of the features.
- Create new date-time features.
- Remove band features because they are just a groups generated based on the ratings.
- Textual features describing the dwelling we unroll, remove from the initial dataset and analyze separately.
- Parse postcodes, towns, countries from https://www.townscountiespostcodes.co.uk and merge it with input data.

## 2. Rankings and correlations

### Number or dwellings by countries (rank number on the map)
#### Countries rankings barplot and the map
![Screenshot](pictures/map0.PNG)
- The most popular regions are in the center part of Scotland like Glasgow or Edinburgh.
- The most unpopular regions are in the north part of Scotland and also regions near the center.

### 2.1. Rank Towns by current efficiency rating
#### Countries rankings barplot and the map
![Screenshot](pictures/map1.PNG)
- The most energy efficient regions are concentrated in the center part of Scotland. 
- The least energy efficient regions are in the north part.
#### TOP-10 Town rankings table (len is the number of dwellings in that town and mean is the average value)
![Screenshot](pictures/tab1.PNG)
<br><br><br><br><br><br><br>

### 2.2. Rank Towns by potential energy efficiency rating
#### Countries rankings barplot and the map
![Screenshot](pictures/map2.PNG)
- The most efficient regions are concentrated in the north because they are currently the worst. 
- The least potentially effective regions are in the center part because they are already currently the most effective.
#### TOP-10 Town rankings table (len is the number of dwellings in that town and mean is the average value)
![Screenshot](pictures/tab2.PNG)
<br><br><br><br><br><br>

### 2.3. Rank Towns by current environmental impact rating
#### Countries rankings barplot and the map
![Screenshot](pictures/map3.PNG)
- The most environmental impact regions are concentrated in the center part of Scotland.
- The least currently environmental impact regions are in the north part especially in Shetland isles.
#### TOP-10 Town rankings table (len is the number of dwellings in that town and mean is the average value)
![Screenshot](pictures/tab3.PNG)
<br><br><br><br><br><br>

### 2.4. Rank Towns by potential environmental impact rating
#### Countries rankings barplot and the map
![Screenshot](pictures/map4.PNG)
- The most environmental impact regions are concentrated in the center and south part of Scotland.
- The least potentially environmental impact regions are Shetland isles and Argyll and Bute.
#### TOP-10 Town rankings table (len is the number of dwellings in that town and mean is the average value)
![Screenshot](pictures/tab4.PNG)
<br><br><br><br><br><br>

### 2.5. Rank Towns by Current Emissions (T.CO2/yr)
#### Countries rankings barplot and the map
![Screenshot](pictures/map5.PNG)
- The most currently polluting in CO2 measurements regions are concentrated in the center part of Scotland. 
- The least currently polluting in CO2 measurements regions are in the north part.
#### TOP-10 Town rankings table (len is the number of dwellings in that town and mean is the average value)
![Screenshot](pictures/tab5.PNG)
<br><br><br><br><br><br>

### 2.6. Rank Towns by Potential Reduction in Emissions (T.CO2/yr)
#### Countries rankings barplot and the map
![Screenshot](pictures/map6.PNG)
- The most potentially polluting in CO2 measurements regions are concentrated in the center part of Scotland. 
- The least potentially polluting in CO2 measurements regions are in the north part.
#### TOP-10 Town rankings table (len is the number of dwellings in that town and mean is the average value)
![Screenshot](pictures/tab6.PNG)
<br><br><br><br><br><br>

### 2.7. Rank Towns by potential savings in heating costs (£) over three years
#### Countries rankings barplot and the map
![Screenshot](pictures/map7.PNG)
- The best regions by potential savings in heating costs are in the north and south part of Scotland.
- The least regions by potential savings in heating costs are in the center part of Scotland.
#### TOP-10 Town rankings table (len is the number of dwellings in that town and mean is the average value)
![Screenshot](pictures/tab7.PNG)
<br><br><br><br><br>

### 2.8. Rank Towns by potential savings in hot water costs (£) over three years
#### Countries rankings barplot and the map
![Screenshot](pictures/map8.PNG)
- The best regions by potential savings in hot water costs are in the north part of Scotland. 
- The least regions by potential savings in hot water costs are in the center part of Scotland. 
#### TOP-10 Town rankings table (len is the number of dwellings in that town and mean is the average value)
![Screenshot](pictures/tab8.PNG)
<br><br><br><br><br>

### 2.9. Rank the top 5 wall descriptions (wall materials) by CO2 emissions current per floor area and wall energy efficiency (create a single rating combining CO2 emissions and wall energy efficiency)
- We have transformed the unique wall description values to Wall Type and Wall Insulation features (more details you can find in the script).
- We have created CO2 rating based on the relevant CO2 values (inverse dependency and values from 1 to 5) 
- Wall rating have been created from the WALL_ENERGY_EFF field with replacing of the word rankings to the values: 
        very poor: 1,
        poor: 2,
        average: 3,
        good: 4,
        very good: 5
- Total rating is the simple average between wall and CO2 ratings.
#### Features popularity
![Screenshot](pictures/wall1.PNG)
#### Features average ratings
![Screenshot](pictures/wall2.PNG)
<br><br><br><br><br><br><br>
#### Features heatmaps (Wall Type on Wall Insulation)
![Screenshot](pictures/wall3.PNG)
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### 2.10. Rank the top 5 roof descriptions (roof materials) by CO2 emissions current per floor area and roof energy efficiency (create a single rating combining CO2 emissions and roof energy efficiency)
- We have transformed the unique roof description values to Roof Type and Roof Insulation features (more details you can find in the script).
- We have created CO2 rating based on the relevant CO2 values (inverse dependency and values from 1 to 5) 
- Wall rating have been created from the ROOF_ENERGY_EFF field with replacing of the word rankings to the values: 
        very poor: 1,
        poor: 2,
        average: 3,
        good: 4,
        very good: 5
- Total rating is the simple average between roof and CO2 ratings.
#### Features popularity
![Screenshot](pictures/roof1.PNG)
#### Features average ratings
![Screenshot](pictures/roof2.PNG)
<br><br><br><br><br>
#### Features heatmaps (Roof Type on Roof Insulation)
![Screenshot](pictures/roof3.PNG)
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### 2.11. (BONUS) Rank the top 5 floor descriptions (floor materials) by CO2 emissions current per floor area
- We have transformed the unique floor description values to Floor Type and Floor Insulation features (more details you can find in the script).
- We have created CO2 rating based on the relevant CO2 values (inverse dependency and values from 1 to 5) 
#### Features popularity
![Screenshot](pictures/floor1.PNG)
#### Features average ratings
![Screenshot](pictures/floor2.PNG)
#### Features heatmaps (Floor Type on Floor Insulation)
![Screenshot](pictures/floor3.PNG)

### 2.12. (BONUS) Rank the top 5 windows descriptions by CO2 emissions current per floor area and windows energy efficiency (create a single rating combining CO2 emissions and windows energy efficiency)
- We have preprocessed the field WINDOWS_DESCRIPTION (more details you can find in the script).
- We have created CO2 rating based on the relevant CO2 values (inverse dependency and values from 1 to 5) 
- Windows rating have been created from the WINDOWS_ENERGY_EFF field with replacing of the word rankings to the values: 
        very poor: 1,
        poor: 2,
        average: 3,
        good: 4,
        very good: 5
- Total rating is the simple average between windows and CO2 ratings.
#### Feature popularity
<img src="pictures/windows1.PNG" alt="drawing" width="60%"></img>
#### Feature average ratings
<img src="pictures/windows2.PNG" alt="drawing" width="60%"></img>

### 2.13. (BONUS) Rank the top 5 mainheat descriptions by CO2 emissions current per floor area and mainheat energy efficiency (create a single rating combining CO2 emissions and mainheat energy efficiency)
- We have preprocessed the field MAINHEAT_DESCRIPTION (more details you can find in the script).
- We have created CO2 rating based on the relevant CO2 values (inverse dependency and values from 1 to 5) 
- Mainheat rating have been created from the MAINHEAT_ENERGY_EFF field with replacing of the word rankings to the values: 
        very poor: 1,
        poor: 2,
        average: 3,
        good: 4,
        very good: 5
- Total rating is the simple average between mainheat and CO2 ratings.
#### Feature popularity
![Screenshot](pictures/mainheat1.PNG)
#### Feature average ratings
![Screenshot](pictures/mainheat2.PNG)

### 2.14. (BONUS) Rank the top 5 mainheatcont descriptions by CO2 emissions current per floor area and mainheatcont energy efficiency (create a single rating combining CO2 emissions and mainheatcont energy efficiency)
- We have preprocessed the field MAINHEATCONT_DESCRIPTION (more details you can find in the script).
- We have created CO2 rating based on the relevant CO2 values (inverse dependency and values from 1 to 5) 
- Mainheatcont rating have been created from the MAINHEATCONT_ENERGY_EFF field with replacing of the word rankings to the values: 
        very poor: 1,
        poor: 2,
        average: 3,
        good: 4,
        very good: 5
- Total rating is the simple average between mainheatcont and CO2 ratings.
#### Feature popularity
![Screenshot](pictures/mainheatcont1.PNG)
#### Feature average ratings
![Screenshot](pictures/mainheatcont2.PNG)

---
## 3. Algorithms

### 3.1. Build an algorithm to find correlations between CO2 emissions current per floor area vs wall description and wall energy efficiency
- Create a splittings by the unique combinations of cleaned features values. Wall description and wall energy efficiency in our case have transformed into 3 features: WALL_TYPE, WALL_INS, Wall_rating. Collect CO2 emissions current per floor area values in each group.
- If in one of the group we have less then 100 observations let's replace them as OTHER. In total we have received 56 unique number of groups. 
- Plot box-plot to have ability to vizual compare distributions of CO2 values in each group. On the picture below we can see that there is a strong differences between distributions of that feature in the groups.
- Conduct ANOVA statistical test to have numerical value of similarity between these variables. We calculated F_statistics = 1244.40 and pvalue = 0 and can conclude that there is high dependance between these features.
#### Boxplots of CO2 values by the groups:
![Screenshot](pictures/wall4.PNG)

### 3.2. Build an algorithm to find correlations between CO2 emissions current per floor area vs roof description and roof energy efficiency
- Create a splittings by the unique combinations of cleaned features values. Roof description and roof energy efficiency in our case have transformed into 3 features: ROOF_TYPE, ROOF_INS, Roof_rating. Collect CO2 emissions current per floor area values in each group.
- If in one of the group we have less then 100 observations let's replace them as OTHER. In total we have received 36 unique number of groups. 
- Plot box-plot to have ability to vizual compare distributions of CO2 values in each group. On the picture below we can see that there is a strong differences between distributions of that feature in the groups.
- Conduct ANOVA statistical test to have numerical value of similarity between these variables. We calculated F_statistics = 1153.09 and pvalue = 0 and can conclude that there is high dependance between these features.
#### Boxplots of CO2 values by the groups:
![Screenshot](pictures/roof4.PNG)

### 3.3. Build an algorithm to find correlations between construction age band vs current energy efficiency and current emissions (T.CO2/yr)
- Convert age band to it's maximum value in the range to have the numerical feature
- Calculate average features values of each age construction group.
- Draw points to vizually understand the dependancies.
- Calculate Pearson correlation coefficient between feature and age value.
#### Correlation coefficients with construction age and features:
![Screenshot](pictures/age1.PNG)
#### Dependencies of average feature value by construction age:
![Screenshot](pictures/age2.PNG)

### 3.4. Build an algorithm that takes as input the characteristics of a building (any field of the dataset) and outputs recommendations on the elements of the house to be modified to improve its energy performance
_More details you can find in the script 6_Recommendations.ipynb_
- We are using different building ratings as input features (details how to generate that ratings are in 4_Analyzing scripts):
    - Hot_water
    - Lighting
    - Wall
    - Roof
    - Floor
    - Windows
    - Mainheat
    - Mainheatcont
- Ratings could be float then we convert them to the integer values from 1 to 5.
- In each categorical rating value we calculate average value of a target variable (energy costs or energy performance).
- Based on that matrix we calculate the maximum target improvement for each dwelling owner under the assumption that the owner can improve his feature rating only on 1.
#### Heatmap of the average energy performance value by the rating value (1-5) and the input features:
![Screenshot](pictures/reco1.PNG)
#### After we got recommendation for each dwelling we have the following statistics:
![Screenshot](pictures/reco1_res.PNG)


### 3.5. Build an algorithm that takes as input the characteristics of a building (any field of the dataset except those related to costs) and outputs the total cost of energy of the building over a 3-year period
_More details you can find in the script Modelling_cost.ipynb_
- Create validation set as 20% random sample from initial dataset.
- Preprocess input features and choose not duplicated and potentially usefull for modeling.
- Train Boosting models (Xgboost, LightGBM) and Random Forest model.
- Evaluate models on the validation set by the following metrics: mean absolute error, mean squared error, mean absolute percentage error, symmetric mean absolute percentage error.
#### As we can see in the table below all models give us sufficiently good resuls:
![Screenshot](pictures/models.PNG)
#### Feature importances of Xgboost model:
![Screenshot](pictures/imp_xgb.PNG)
#### Feature importances of LightGBM model:
![Screenshot](pictures/imp_lgb.PNG)
#### Feature importances of Random Forest model:
![Screenshot](pictures/imp_rf.PNG)

### 3.6. Build an algorithm that takes as input the characteristics of a building (any field in the dataset) and outputs recommendations on which elements of the house should be modified to most effectively decrease the total energy cost of the building over a 3-year period
_More details you can find in the script 6_Recommendations.ipynb_
- We are using different building ratings as input features (details how to generate that ratings are in 4_Analyzing scripts):
    - Hot_water
    - Lighting
    - Wall
    - Roof
    - Floor
    - Windows
    - Mainheat
    - Mainheatcont
- Ratings could be float then we convert them to the integer values from 1 to 5.
- In each categorical rating value we calculate average value of a target variable (energy costs or energy performance).
- Based on that matrix we calculate the maximum target improvement for each dwelling owner under the assumption that the owner can improve his feature rating only on 1.
#### Heatmap of the average energy cost value by the rating value (1-5) and the input features:
![Screenshot](pictures/reco2.PNG)
#### After we got recommendation for each dwelling we have the following statistics:
![Screenshot](pictures/reco2_res.PNG)
