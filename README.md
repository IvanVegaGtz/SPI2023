## Data Cleaning

From the database provided by the client, the corresponding exploratory data analysis (EDA) was carried out. To perform this, a preliminary data cleaning was conducted.
Data Cleaning As part of the data cleaning process, the variables "glucosa" (glucose) and "creatinina" (creatinine) were not of numeric type, so the data type was changed to conduct the EDA. This involved correcting data entry errors such as "80|" or "0.6.". Other capture errors were also identified, including negative ages and missing values in age, often due to individuals resisting providing their information. Additionally, unusually low and high values were observed for glucose and uric acid, respectively.

According to client’s feedback, glucose values around 20 to 30 are considered low. However, within the database, values such as 1.22, 1.98, 8.7, and 9.7 were found, significantly below reference values. Furthermore, glucose values are typically integers, so the capture error involved placing a decimal point where it shouldn't be. Similar issues were noted with uric acid values. Normal uric acid levels in men range from 3.5 to 7.2, and in women, from 2.5 to 6. Small values usually include a decimal point, but the database showed very high values like 83 or 62. Consequently, values greater than 20 were replaced with the decimal point value, transforming 83 to 8.3.

## Exploratory Data Analysis (EDA)

 Once the database was cleaned, an exploratory data analysis was performed to examine the irregularities in glucose and uric acid. For a comprehensive and quick analysis, the pandas-profiling library was utilized, providing key statistics of the variables and histograms. The main purpose of this analysis was to gain an initial insight into the data, identify irregularities, or discover possible patterns useful for modeling. Both the cleaning and EDA processes are explained in the Python code.
