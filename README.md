# Project on :Simple_and_Multiple_Linear_Regression_Model
Here I build simple and multiple linear models using the Food_Texture Data. I have covered different possibilities in building the model.
### Introdunction:
In this project we do slightly different type of project work. Here we consider or work with the Food_Texture data. This data can be obtained from the website given <https://openmv.net/info/food-texture>

Here we first do some manipulations to ready our required data set and then we build Simple and Multiple Linear Regression Models using Response and Predictor variables.

### Project Explanation:
This includes the below details:
#### 1. Installing and loading required packages:
First we install and load the required package **tidyverse** and **car** in the R environment.After that we load the packages given follows:
* tidyverse
* dplyr
* car

#### 2. Reading the data set:
Then we read the **Food_Texture_Data.csv** file using the **read.csv()** function that comes under readr library and tidyverse package. Remember we place the file in the working directory where R is stored. So we do not need to mention its path in the code written.

#### 3. Data Manipulation:
Then we do some data manipulation in the data set. First we mutate a column called Price so that it can become our Response variable. The other variables will be predictor variable. We also add a categorical column called Cost at last to check the Linear Regression Model for categorical variables. We also eliminate the column called X which gives the product names.

#### 4. SLRM Building:
Then we build five SLRM using Price as Response variabel and the other factors such as Density, Oil_Percentage, Crispy,Hardness and fracture as predictor variable. We use the lm() function to build the model and summary() function to get the results of the model.

#### 5. MLRM Building:
After building SLRM, we build an MLRM where Price is the response variable which is regressed upon the other variables. Here we consider the other variables together to build the MLRM.

#### 6. Correlation Coefficient Matrix:
After that we build the correlation coefficient matrix to check the respective effect of the predictor variables over the Response variable. The coefficient always ranges from -1 to +1. +1 means positively correlated, -1 means negatively correlated and 0 means no corrleation.

#### 7. Checking the VIF:
The term VIF stands for Variance Inflation Factor. To determine this we use the pre-installed and pre loaded car package and car library. It gives five values from 5 Respone variables. The values which is grater than 10 (typically) can be rejected in building the model.

#### 8. Checking collinearity:
To check collinearity we create another column called Density_in_hundred which is nothing but Density/100. Observe that the columns Density and Density_in_hundred are dependent to each other. So on making a model by taking the above two columns as Predictor we always get NA object corresponding to the Density_in_hundred variable.

#### 9. Creating model for categorical variable:
The primary data set has to categorical column. We create a categorical column that contains values Yes and No, that indicates a product is Costly or not. Here No is set as refernece (0 level). So in the result we observe a dummy variable called CostlyYes that corresponds the result of the model.

**Note: We are also interested in the conclusion of the project. we discussed them in different Rmd file named Conclusions, which is also attached with the files in the repository. Please do check the file to undertsand the in detailed conclusions and intrepretations and basic terminologies.**
