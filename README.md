# Timesheets-Pipeline-Bot
## Arham Anwar

### Timesheets Pipeline using Excel, Python, Tableau & Egnyte

Git-hub repository at:
https://github.com/kakashisensei101/Timesheets-Pipeline-Bot

- Jupyter notebook: **Timesheets_Consolidation _ Email Bot.ipynb**
- data set: Timesheets-Pipeline-Bot/Weekly Files to be Consolidated/

<p align="center">
<img src=https://user-images.githubusercontent.com/64707681/189487172-69a6c5ed-ea84-48ef-a39b-04b57b70721a.gif >
</p>

# Table of contents
1. [Introduction](#introduction)

2. [Flow](#section2)
    1. [Initial steps](#sec2p1)
    2. [Descriptive statistics](#sec2p2)
    3. [Start looking at categories of diner](#sec2p3)
    4. [Plots to summarize some statistics](#sec2p4)
     
3. [Step Details](#section3)
5. [Impact](#conclusion)



## 1. Introduction <a name="introduction"></a>
- This README describes work done on the timesheets tool created by me for my team at Impendi Analytics. Resources used include Python, Tableau, Excel and Egnyte for Cloud storage (and associated python packages Jupyter, matplotlib, Seaborn, scikit-learn, statsmodels, and SciPy). These packages all come as part of the Anaconda distribution of Python.
- The analysis takes the form of a single Jupyter notebook of filename given above. To view this file, download it from this repository and start Jupyter notebook in the folder containing the file. Use the command **Jupyter notebook** on the command line. 
- Alternatively, view a static version of the notebook (by providing its GitHub url) using Jupyter Nbviewer. 
- The weekly timesheet files are included in the repository. The data set is a dummy data set. I replaced actual data with dummy data as it conflicted the privacy policies at my firm.
- All images intended for inclusion in this README are located in the repository.
- I have tried to structure the Jupyter notebook and this README so that they have corresponding sections. However, I do not wish to merely repeat here what has been stated in the notebook. I will endeavour to have this README summarize the work of the notebook and, hopefully, complement the analyses done there.

##  2. Flow <a name="section2"></a>

<img width="960" alt="Flow Map" src="https://user-images.githubusercontent.com/64707681/189486763-12012d50-e301-489f-806a-fad11521673c.PNG">

-Step one: Team members fill in the weekly timesheets through an excel workbook on cloud storage for all hours, including commute, team meals, meetings, weekend hours (if any), paid time offs, vacations, holidays etc. As soon as they would fill the timesheets, the timesheets would get sent to my folders through macros on the workbook.


-Step two: When all workbooks reach my timesheets folder, a python code is executed which consolidates the 75 workbooks, removes duplicate rows, removes blank rows, fixes erroneous entries and validates the total hours.


-Step three: The code sends the cleaned and consolidated file to the project managers through email using smtbl library.
-step four: Tableau Dashboards are automatically refreshed for all since the dashboards are linked to a csv file on the drive with a live connection.



### 2.01 Step Zero: Weekly notifications
Team members are weekly notified to fill in the timesheets by EOD (Friday). The notfication is sent via the email ID managed through the python script.
![image](https://user-images.githubusercontent.com/64707681/189495637-799d95ce-58ed-4147-8d1c-a7d11d760805.png)


### 2.1 step one: Weekly Excel Workbooks <a name="sec2p1"></a>
Team members fill in the weekly timesheets through an excel workbook on cloud storage for all hours, including commute, team meals, meetings, weekend hours (if any), paid time offs, vacations, holidays etc. As soon as they would fill the timesheets, the timesheets would get sent to my folders through macros on the workbook.
![image](https://user-images.githubusercontent.com/64707681/189495716-367d5a4f-0af6-40b7-a61a-529661f709e0.png)

### 2.2 Step two: Consolidation & Cleaning <a name="sec2p2"></a>
Step two: When all workbooks reach my timesheets folder, a python code is executed which consolidates the 75 workbooks, removes duplicate rows, removes blank rows, fixes erroneous entries and validates the total hours.

<img width="264" alt="Code" src="https://user-images.githubusercontent.com/64707681/189495738-9d736984-ece9-4886-b57c-46c890e8ac58.PNG">

### 2.3 Step three: Email Bot <a name="sec2p3"></a>
Step three: The code sends the cleaned and consolidated file to the project managers through email using smtbl library.

<img width="258" alt="Bot Email" src="https://user-images.githubusercontent.com/64707681/189495751-29eb1bbd-b1b0-47ca-bab7-3aec4b75eb39.PNG">

### 2.4 Step four: Tableau Insights <a name="sec2p4"></a>
step four: Tableau Dashboards are automatically refreshed for all since the dashboards are linked to a csv file on the drive with a live connection.

<img width="956" alt="Dashboard SS" src="https://user-images.githubusercontent.com/64707681/189495785-51d5739c-02c8-4f73-b308-5e6b3672172b.PNG">


## 3. UI Snapcshots <a name="section3"></a>


## 4. Impact <a name="conclusion"></a>
The key impact of this analysis is below:
1. Increased visibility into team work life balance
2. Increased visibility into project split of the work hours
3. Increased visibility into firm development activities
4. Ability to identify overworked individuals
5. Ability to avoid concentration of work
