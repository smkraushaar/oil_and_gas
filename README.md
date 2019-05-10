# oil_and_gas

## Heel code - trying to locate the exact point of inflection from vertical to horizontal in a well, and trying to predict if a well is toe-up or toe-down.

##Random Forest Model Steps for Predicting Economic Oil Wells:
1.	Collect geologic property grids for 1 zone in Petra using petrophysical logs from vertical wells (resistivity, DPHI, net pay, water saturation, gross thickness, etc) 
a.	This is the most difficult step.
2.	Sample the grids to the horizontal wells drilled in the specific geologic zone of interest
3.	Export the dataset of horizontal wells, and associated geologic properties
4.	Compile with engineering and production data in Spotfire
5.	Load complete dataset into R software
6.	Split the data into a training and test dataset
7.	Run random forest predictive model on the training dataset.  
8.	Test effectiveness of predictive model on the test dataset – tweak model to get the best % accuracy. 
9.	Run the predictive model on the vertical wells with similar geologic properties. Set the engineering variables to a constant. 
10.	Predict which vertical wells are likely to produce an economic horizontal well (0 = <40 EUR/ft, 1 = >40 EUR/ft). The economic cutoff here is 40 barrels of oil per ft of drilled lateral well. 
11.	Export the predictive results to Petra, grid the data, and create a “drill” “don’t drill” map.  
