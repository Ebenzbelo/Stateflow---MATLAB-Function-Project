# Stateflow---MATLAB-Function-Project
This project is aimed at using a Stateflow chart with a MATLAB function to detect outliers in a noisy signal.

The Simulink model provides the last five data points of the signal to the chart.
The criteria for identifying an outlier will be: "Does the current point differ from the mean of the last five points by more than 2?"

## Step 1
Create a new MATLAB function in your chart by using the left mouse button to drag from the icon on the object palette.
Define the function signature as
isOutlier = detectOutlier(input).
<img width="543" height="438" alt="Step 1" src="https://github.com/user-attachments/assets/86808ef5-39fd-4e18-a9e4-12bcfabbe274" />

## Step 2
The MATLAB code to identify outliers is
 
dist = abs(input(end) - mean(input));
isOutlier = dist > 2;
- Double-click on the MATLAB function in the chart to edit it in the MATLAB Editor. The function signature is populated from the chart. Enter the algorithm in the body of the function.
<img width="635" height="246" alt="Step 2" src="https://github.com/user-attachments/assets/10650269-fcb0-4395-b4d4-5ee49bac77d1" />
## Step 3

The transition from NotOutlier to Outlier should occur if detectOutlier(data) returns true. Conversely, the transition from Outlier to NotOutlier should occur if detectOutlier returns false.
-Use calls to the MATLAB function to create the transition conditions between the two states.
<img width="771" height="547" alt="Step 3" src="https://github.com/user-attachments/assets/0363365f-c358-4650-8df0-01b4346ce473" />








