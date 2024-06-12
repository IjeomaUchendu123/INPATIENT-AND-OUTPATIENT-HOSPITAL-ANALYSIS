# IN-PATIENT AND OUT-PATIENT HOSPITAL ANALYSIS

## TABLE OF CONTENTS

- [PROJECT OVERVIEW](#project-overview)
- [DATA SOURCES](#data-sources)
- [TOOLS](#tools)
- [DATA CLEANING](#data-cleaning)
- [EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)
- [DATA ANALYSIS](#data-analysis)
- [FINDINGS](#findings)
- [RECOMMENDATIONS](#recommendations)
- [LIMITATIONS](#limitations)
- [REFERENCES](#references)


### PROJECT OVERVIEW

This project aims to uncover insights into Inpatient and OutPatient cases in a hospital over a period of 4 years. Its analysis spans across variables such as specialty, age ranges, time-bands etc. By analyzing this various aspects, we seek to identify trends, get a clear understanding of patient cases, and make data driven recommendations.


<img width="618" alt="INPATIENT SNIP" src="https://github.com/IjeomaUchendu123/INPATIENT-AND-OUTPATIENT-HOSPITAL-ANALYSIS/assets/150269976/d2213310-f386-401b-8527-498e0821fa4e">


<img width="621" alt="OUTPATIENT SNIP" src="https://github.com/IjeomaUchendu123/INPATIENT-AND-OUTPATIENT-HOSPITAL-ANALYSIS/assets/150269976/3fa1de8a-2002-4f17-b6d0-afbef4eab2bc">


### DATA SOURCES

The primary data sets used for this analysis are the "IN_WL 2018.csv", "IN_WL 2019.csv", "IN_WL 2020.csv","IN_WL 2021.csv","Op_WL 2018.csv", "Op_WL 2019.csv","Op_WL 2020.csv","Op_WL 2021.csv",containing various information for each year for Inpatients and Outpatients of the hospital respectively.

### TOOLS

- PowerBI(Data Cleaning, Analysis and Creating interactive dashboard)
  - (Download Here)(https://powerbi.microsoft.com/en-us/downloads/)

### DATA CLEANING AND PREPARATION

In the data preparation stage, the following tasks were performed:
1. Data Loading and Inspection
2. Appending files for each year
3. Handling missing values
4. Data Formatting such as month and year extraction
5. Renaming blank cells
6. Creating New Measures

### EXPLORATORY DATA ANALYSIS

This involved exploring the data to answer key questions such as;

-   What are the average cases per year ?
-   What are the top specialties ?
-   What age range has the highest cases ?

### DATA ANALYSIS

```PowerBI
RIGHT('Op_WL FILE'[Archive_Date],4)
```

```POWERBI
MONTH NAME = IF('IN_WL FILE'[Month No.]="1","JAN",IF('IN_WL FILE'[Month No.]="2","FEB",IF('IN_WL FILE'[Month No.]="3","MARCH",IF('IN_WL FILE'[Month No.]="4","APRIL",IF('IN_WL FILE'[Month No.]="5","MAY",IF('IN_WL FILE'[Month No.]="6","JUNE",IF('IN_WL FILE'[Month No.]="7","JULY",IF('IN_WL FILE'[Month No.]="8","AUG",IF('IN_WL FILE'[Month No.]="9","SEP",IF('IN_WL FILE'[Month No.]="10","OCT",IF('IN_WL FILE'[Month No.]="11","NOV","DEC")))))))))))
```

```POWERBI
Month No. = MONTH('IN_WL FILE'[Archive_Date])
```

### FINDINGS
The results from the analysis are summarized as follows:
- There are more Outpatient cases than Inpatient Cases in a year with an average Inpatient Cases of 726,000 and average Outpatient cases of 5.43M.
- For both Inpatient and Outpatient cases, adults within the range of 16-64 years has the highest number of cases.
- For both Inpatient and Outpatient cases, the year 2020 had the highest number of cases.
- Cases that are within 0-3 months band are the highest i.e most cases take within 0 to 3 months to treat.
- General Surgeries has the highest number of cases when it comes to specialty.
- For Inpatient Cases, DayCase makes up 70.91% while Inpatient makes up 29.1%.

### RECOMMENDATIONS

Based on the analysis, the following actions are recommended;
- Priortize investing in general surgery equipments as this would help make surgical processes which has the highest number of patients more swift.
- Work on expansion of adult wards instead of children wards in order to accomadate the adult patients that make up the greater percentage of patients.
- For years with an epidemic e.g 2020, there should be more provision of healthcare resources to serve the increased healthcare needs.
- For Inpatient cases, there should be a section for DayCases as they make up the higher population with over 70%.

### LIMITATIONS
There were 175 Outpatients with no records of their age or age range. However, this was left catered to and renamed as "Not Stated" and "Unidentified" respectively in order not to skew the final results of our analysis. This number makes up just about 0.06% 0f our data.

### REFERENCES
Google for searches on some medical terms.
