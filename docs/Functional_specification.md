# User Profiles

## User 1: Fiona
### <b>Type: Traveller </b>

- Wants to know the probability of a flight being delayed or expected severity of a delay.
- Interacts with the tool by providing flight details on a website or application.
- Needs low expertise and intuitive interface to navigate and understand the insight provided by the tool.
- Skills required to locate and provide flight details.

## User 2: Bruno
### <b>Type: Technician</b>

- Wants to update the model with new data and understand feature importance.
- Interacts with the model by running scripts to add data and retrain the model.
- Needs quick interface to update model and check new testing accuracy.
- Skills required to be able to upload the data and understand modelling. Some technical skills required are python, bash, excel etc.

# Use Cases

## BTS Flight Forecast
- <b> Background </b>
  
  - BTS Flight Forecast is a tool to predict flight delays utilizing past weather data, and weather forecast, given a specified airport code, date, and time.
- <b> Data source </b>
  
  - Flight Data: https://www.transtats.bts.gov/DL_SelectFields.aspx?gnoyr_VQ=FGK&QO_fu146_anzr=b0-gvzr
  - Weather Data: https://www.wunderground.com/history

### Usecase 1: View Flight Delay Prediction

<b>Objective: Information Validation and Viewing Delay Prediction</b>

- User: Accesses the website/ application.
- System: Displays dropdowns to select departure airport code, date and time.
- User: Selects airport code, date and time from the dropdowns.
- System: Checks if all the required data is entered. Shows error if one any of the fields is not entered, or date is too far in the future.
- User: Clicks button to view the likelihood of delay of a flight starting from the departure airport at the given datetime.
- System: Displays the predicted delay for the selected airport, date and time.

### Usecase 2: Loading new data and re-training model

<b>Objective: Training the model with new flight data.</b>

- User: Access the admin page
- System: Provides an option to upload new flight data. ( This data should be downloaded from BTS. Outside the scope of this tool)
- User: Selects the data file and clicks upload.
- System: Received the file uploaded. Throws error if it is not in the required format (eg: missing columns, different datatype)
- User: Clicks "Retrain Model" button
- System: Runs a script which retrains the model based on the uploaded data in conjunction with the existing data. Displays success or failure.
- User: Views the training and testing results like model accuracy.