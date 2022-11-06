# Ocean Protocol :: Energy Efficiency Data Challenge

## Files description

- README.md - task and files description.
- REPORT.md - solution description.
- data/ - folder with input and preprocessed data (more details about the preprocessed data you can find in the scripts below).
- pictures/ - folder with the pictures for solution description.
- startup.py - initial script that executed in every notebook when started.
- 0_Data_exploration.ipynb - script with the general input data exploration.
- 1_Geodata_parsing.ipynb - working with geographical data: 
    - parsing postcodes, towns, countries from  https://www.townscountiespostcodes.co.uk
    - downloading shapefiles of Scotland countries and maps drawing
-  2_Data_preprocessing.ipynb - scripts with data cleaning and preprocessing:
    - data types convertion and features generation and elimination
    - analyzing textual features from input data, unpivot them and save to separate files
    - merging parsed geo data with input data    
- 3_Get_ratings_geo.ipynb - calculation of the geographical rankings (points 1-8 from the Rankings below).
- 4_Analyzing_wall.ipynb - analyzing wall description and creating rankings and correlations (point 9 from the Rankings and 1 from the Algorithms below).
- 4_Analyzing_roof.ipynb - analyzing roof description and creating rankings and correlations (point 10 from the Rankings and 2 from the Algorithms below).
- 5_Modelling_cost.ipynb - build an algorithm that takes as input the characteristics of a building (any field of the dataset except those related to costs) and outputs the total cost of energy of the building over a 3-year period.
- 6_Recommendations.ipynb - build an algorithm that takes as input the characteristics of a building (any field of the dataset) and outputs recommendations on the elements of the house to be modified to improve its energy performance or total energy cost (points 4 and 6 from Algorithms).

---
## Task description

### Details

- The challenge dataset originates from the Scottish Energy Performance Certificate Register (http://www.scottishepcregister.org.uk/), which is the data repository for energy performance data used in the production of Energy Performance Certificates in Scotland.
- We ask you to create context around the data by generating rankings and visualizations that illustrate how and why the data is valuable. Then, we ask you to build algorithms that facilitate innovation and improvement. Lastly, we ask you to write a concluding report that presents your findings in a quantitative and qualitative analysis containing suggestions and recommendations.
- Participants can access the dataset provided for this challenge from the Ocean Market by clicking the following link: https://bit.ly/3g5tr4s and downloading the published data asset. The data asset is a ZIP archive containing data in CSV format and data description in PDF format. For this challenge, we will consider data collected in the year 2021, as provided in the dataset.

### Challenge
You are asked to perform three types of tasks: 
- (1) generate rankings and create top-5 lists; 
- (2) build algorithms that find correlations between given attributes, and algorithms that generate specific output given specific input 
- (3) write a report that summarizes your findings from the first two tasks. 
- There is an opportunity to earn bonus points by performing specific tasks on the Ocean Market.

### Rankings (20 points) - Generate the following rankings:
1. Rank Towns by current efficiency rating - (2 points)
2. Rank Towns by potential energy efficiency rating - (2 points)
3. Rank Towns by current environmental impact rating and note if there have been periods where houses were more or less environmentally friendly- (2 points)
4. Rank Towns by potential environmental impact rating - (2 points)
5. Rank Towns by Current Emissions (T.CO2/yr) - (2 points)
6. Rank Towns by Potential Reduction in Emissions (T.CO2/yr) - (2 points)
7. Rank Towns by potential savings in heating costs (£) over three years - (2 points)
8. Rank Towns by potential savings in hot water costs (£) over three years - (2 points)
9. Rank the top 5 wall descriptions (wall materials) by CO2 emissions current per floor area and wall energy efficiency (create a single rating combining CO2 emissions and wall energy efficiency) - (2 points)
10. Rank the top 5 roof descriptions by CO2 emissions current per floor area and roof energy efficiency (create a single rating combining CO2 emissions and roof energy efficiency) - (2 points)

### Algorithms (60 points) - Build the following algorithms:
1. Build and algorithm to find correlations between CO2 emissions current per floor area vs wall description and wall energy efficiency - (5 points)
2. Build and algorithm to find correlations between CO2 emissions current per floor area vs roof description and roof energy efficiency - (5 points)
3. Build and algorithm to find correlations between construction age band vs current energy efficiency and current emissions (T.CO2/yr) - (5 points)
4. Build an algorithm that takes as input the characteristics of a building (any field of the dataset) and outputs recommendations on the elements of the house to be modified to improve its energy performance - (15 points)
5. Build an algorithm that takes as input the characteristics of a building (any field of the dataset except those related to costs) and outputs the total cost of energy of the building over a 3-year period - (15 points)
6. Build an algorithm that takes as input the characteristics of a building (any field in the dataset) and outputs recommendations on which elements of the house should be modified to most effectively decrease the total energy cost of the building over a 3-year period - (15 points)


### Report (20 points) - Submit a report describing the above findings. 
Make sure to include qualitative insights in addition to the quantitative ones and make recommendations for future improvements in building construction. Reports will be evaluated on presentation structure, approach, content, and completeness.

### Bonus (30 points) - Perform any of the following tasks for additional points:
- Publish your report for free use on the Ocean Market (use Polygon Network) - (5 points)
- Publish the dataset used (the CSV file from the ZIP downloaded) on the Ocean Market and make it available for Compute-to-Data (use Polygon Network) - (10 points)
- Publish your algorithms on the Ocean Market so any users can run them for free on the dataset you published in task 2 above (use Polygon Network) - (15 points)