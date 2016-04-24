# Predict customer data usage for a telco

One challenge for Telcos is finding customers whose data usage may exceed their rate plan during a given month. Marketing can seize this as an opportunity to recommend an upgraded plan or offer an add-on.

In this problem, a large telco is providing 5 months data usage in Mega Bytes for 100K of its customers, subscribed to one of its rate plans. Your task is to predict whether a customer will exceed their average usage over the 5 months by 500 Mega Bytes in the coming month.

The usage data for each customer is given in monthly and daily aggregations.

# File descriptions

train.csv - Training set monthly aggregate
test.csv - Testing set monthly aggregate
contract_ref.csv - Customer information
calendar_ref.csv - Date reference for the daily and monthly aggregates
roaming_monthly.csv - Roaming monthly usage
daily_aggregate.csv - A daily aggregate of the 5th month of data for all the given customers
sample_submission.csv - A sample submission file in the correct format containing 1 row for each customer in test.csv
Data fields

# Monthly Aggregate

CONTRACT_KEY - The Customer ID
206-210_USAGE - The usage (in Mega Bytes) of each of the 5 months
206-210_SESSION_COUNT - The number of sessions of each of the 5 months
TARGET - The label to predict. 1 if the customer's usage in the 6th month will be more than their mean usage over 5 months + 500 MB.
Daily Aggregate

CALL_DATE_KEY - Date ID (refer to calendar_ref.csv)
CELL_KEY - The ID of the cell which was serving the customer on that day. Different cells are in different locations.
ROAMING_FLAG - Whether the data usage was local or roaming
TOTAL_CONSUMPTION - Total usage for that day
NO_OF_SESSION - Number of sessions for that day

# Evaluation

Submissions are evaluated on area under the ROC curve between the predicted probability and the observed target.

# Submission File

The file should contain a header and have the following format:

CONTRACT_KEY,PREDICTED_TARGET
1,0
2,0
3,0
etc.

# Competition Timeline

Start Date: 4/22/2016 10:27:45 PM UTC
Merger Deadline: None
First Submission Deadline: None
End Date: 6/2/2016 11:59:00 PM UTC