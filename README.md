# Berkeley_11.1
## Used Cars
This project was used to examine a dataset of used car information. The goal of this was to see which attributes contributed to a higher priced used car. Below you will be able to see the workflow that led me to my final results.

### Analysis
We started off with a lot of data that was incomplete and missing which makes the analysis quite difficult. I started off by taking care of the top 4 columns that didn't have great numbers.

![Null Counts](./images/count_of_nulls_by_column.png)

As you can see here out of the ~427,000 records size was missing over 300k of its values. Cylinders, condition, and VIN also made good candidates to get rid off. 

The next step was to see out of the number columns that we were given off the bat, what kind of correlation do we see. Price, Year, and Odometer

![Initial Numbers](./images/initial_number_corr.png)

This doesn't show a great correlation between the initial numbers but that paired with a describe() on the data you can get a sense of why and that is there seems to be a stretch in outliers that could be affecting it.

Getting a good sense of the affect that prices have on the other attributes is the next step. I went through and analyzed the difference of prices based on type, manufacturer, and state to name a few.

### Preparation
From there I went through and dropped the unnecessary columns (size, VIN, region, cylinders, and condition). Region was one that had data for every record but is made redundant by the fact that we already have state.

We trimmed out the outliers found within both price and odometer readings which allowed me to focus on the majority of the data without the risk of outliers influencing too much of the prediction.

Lastly was to implement encoding into the fields that were alpha-numeric.

### Modeling
After the data was prepared and ready I went through and ran multiple types of regressions both on different subsets but also regression algorithms such as LinReg, Lasso, and Ridge.

