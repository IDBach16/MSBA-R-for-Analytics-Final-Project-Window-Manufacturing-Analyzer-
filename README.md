# MSBA-R-for-Analytics-Final-Project-Window-Manufacturing-Analyzer-
Window Manufacturing Analyzer

Business Problem Framing
Summit City Glass is a Fort Wayne based glass manufacturer with four suppliers. Summit City Glass wishes to reduce its breakage rate by 1%, reducing cost in the form of lower lost productivity, lower material waste and lower salvage/disposal cost of material waste. It estimates that if yield can be maintaned, a 1% reduction in breakage would save the company between $500 and $1000 dollars a day

Analytics Problem Framing
Our tool performs analysis on a user uploaded data file containing production given within a given window. It creates a linear regression model, splitting the supplied data into a data training and data testing model, allowing it to both teach itself to predict breakage rates, and test its effectiveness against known data. Using this tool, it identifies patterns in the data, including which factors affect breakage the most, uses that data to be able to predict breakage rates for given inputs, and in turn determine the optimal cutting speed to minimize breakage with given parameters.

The current test data does not include a cost constraint factor, such as yield. For the prototype to achieve its goal, such a constraint would need to be included and added to future iterations of the tool

To simplify the model, any NA/Blank Data is replaced with the median value for numerical data and the mode for categorical data. In the case of supplier and location, we can more accurately calculate modes according to their corresponding supplier/location pattern as most suppliers have only one location. While future iterations could attempt to adjust numerical values according to highly correlated fields, as calculated and shown on the predictive tab, more complete data will always produce superior models.

The default data loaded into the tool was given to us by Summit City Glass to build and train our model.

Clicking the download button will download an excel file containing default data file as provided by Summit City Glass and described in the data dictionary.

Summit City Glass employees can update and retrain the model with new data using the file upload button. If the file they upload doesn't have the necessary variable fields, an error will appear below the data dictionary on this tab detailing what input is missing.

Filtering the data: a note of caution
The current model can also be filtered after uploading the file, but users should be careful not to filter too narrowly, especially with categorical fields, as the presciptive analytics feature may not be able to adapt to the changes in the model in this iteration of the tool, causing it the applicaton to crash. Future iterations of the tool will include more advanced logic to handle dynamic changes to the model as well as better error handling around the model
