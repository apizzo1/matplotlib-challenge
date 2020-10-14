# matplotlib-challenge

## Challenge Details

This challenge assumed that an anti-cancer drug company, Pymaceuticals Inc., has requested an indepth investigation into a recent study performed: 249 mice with squamous cell carcinoma (SCC) were studied over 45 days while being treated with different drug regimens. The study measured the change in growth of the tumors on each mouse. The attached analysis simulates a technical report that would be given to the company to determine if their drug of interest, Capomulin, stands out from the other drugs in the study.

The focus of this challenge was to utilize both the Python libraries Pandas and Matplotlib to visualize the results of the investigation.

### Cleaning the data

The data was checked for any mouse ID with duplicate time points -  all data associated with that mouse ID was removed, as the correct measurements to be used could not be verified.

### Analysis 

* 2 summary statistics tables consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen were created.
    * One method involved creating series and combining them together.
    * The other method involved using groupby.aggregate feature.
    * All numbers in these tables match except for the variance and standard deviation columns, which differ slightly. This is because the method combining series uses ddof=0 for variance and std dev. Meanwhile, the aggregate feature has a default ddof = 1. 
* A bar plot was generated using both Pandas's DataFrame.plot() and Matplotlib's pyplot - it shows the number of total mice for each treatment regimen throughout the course of the study. These plotting methods generate the same output.
* A pie plot was generated using both Pandas's DataFrame.plot() and Matplotlib's pyplot that shows the distribution of female or male mice in the study. These plotting methods generate the same output.
* The final tumor volume of each mouse across four of the most promising treatment regimens was calculated: Capomulin, Ramicane, Infubinol, and Ceftamin. The quartiles and IQR were also calculated. From this information, it was noted that only Infubinol showed an outlier.
* A box and whisker plot of the final tumor volume for all four treatment regimens was generated, and potential outliers in the plot were identified by changing their color and style. After plotting, it can again be seen that Infubinol shows an outlier, as expected from the above calculations.
* Mouse i557, treated with Capomulin, was selected a line plot of time point versus tumor volume was generated.
* A scatter plot of mouse weight versus average tumor volume for the Capomulin treatment regimen was generated.
* The correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment was calculated. The linear regression model was then plotted on top of the previous scatter plot, along with the linear regression equation.

### Analyses Performed

There is a great deal of information contained in this investigation. Three observations can be found at the top of the jupyter notebook.

### Files Included
* pymaceuticals_AP - jupyter notebook file containing all analyses
* data folder - contains the 2 csv files used in this challenge
