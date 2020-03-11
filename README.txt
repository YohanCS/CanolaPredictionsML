Needs jupyter notebook to open .ipynb files
If using jupyter notebook from anaconda: 
conda install keras
conda install pd 

Step 1 - Run cell 1 of “Predictions.ipynb” - reads csv and creates a location map setting a key of region to an array of values, indeces are timestamps where we need to manually align ourselves. 

Step 2 - Run cell 2. Creates a split dataset of X and Y. Need to change dataset parameter from ‘Manitoba’ to a different region if want to use other data

Step 3 -  Run cell 3, trains model on region (so different model for each region, use model.save() if you want to keep it in persistent memory) 

Step 4 - In cell 4, input data for 12 months in 2 arrays with first one being product deliveries, second one being prices. This will be used for prediction

Step 5 - in cell 5 it will iteratively go through each t + 1, then use the t + 1 prediction to predict the next t + 1. It will print an inverse transform on the numbers we scaled down for the ML model (human readable numbers) and we will take these values as next 12 values for next year 
