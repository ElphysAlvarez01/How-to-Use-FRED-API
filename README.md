# How to Use Federal Reserve Bank of St. Louis (FRED) API Data
![](FredImage.PNG)

## FRED Data Collection
>> This notebook collects key economic data from the Federal Reserve Economic Data (FRED) site for various states in the United States using the fredapi Python package.

## Libraries Used
```
import pandas as pd
# pandas: Used for data manipulation and analysis.

from fredapi import Fred
# fredapi: Allows access to FRED's extensive collection of economic data.

import datetime
# datetime: Used to handle date-related operations.
```

## Retrieving the API From The FRED Site
- Go to the site here - https://fredaccount.stlouisfed.org/apikeys
- Request an API Key. They will ask for your email and information. However, the API is Free and you will receive it on the same day.
- I recommend you use the documentation to understand how to retrieve the information. https://fred.stlouisfed.org/docs/api/fred/
- Once you receive the API key, add it to the code like the example below. You might need at least two API codes depending on how much data you try to retrieve. 
   
```
fred = Fred(api_key='your_api_key_here')
```

## Data Files Collected
This notebook retrieves and processes the following datasets for each state:

1. **State's Unemployment Rate (Monthly):** The unemployment rate of the state's workforce, reported on a monthly basis.
2. **Bachelor's Degree or Higher (Annual):** The percentage of the state's population aged 25 and older who have completed a bachelor's degree or higher.
3. **Resident Population (Annual):** The total number of residents living in the state, reported annually.
4. **State Minimum Wage Rate (Annual):** The minimum hourly wage set by the state government.
5. **Median Household Income (Annual):** The median annual income of households in the state, reported in current dollars.
6. **Labor Force Participation Rate (Monthly):** The percentage of the state's population that is either working or actively looking for work, reported monthly.

#### Please note: 
- **Certain Data Series were not available across all states.** For example, the State Minimum Wage Rate (Annual) was not available in Alabama. If data was missing for a specific state for a data series, it was skipped and noted on the output.
- **To find the series codes quickly, I recommend you do the following:**
   - I recommend you look for the specific series on the site for one state. For example, you can find the state unemployment rate for California.

     ```
      'California': 'CAUR'
     ```
    - Then I would encourage you to go to ChatGPT and ask it to retrieve the other 49 state series codes.

     ```
      state_codes = {
    'Alabama': 'ALUR',
    'Alaska': 'AKUR',
    'Arizona': 'AZUR',
    'Arkansas': 'ARUR',
    'California': 'CAUR',
    'Colorado': 'COUR',
     ```
      
## Acknowledgments
FRED API: This notebook uses data provided by the FRED website, a service maintained by the Federal Reserve Bank of St. Louis.

#### ....And Now, you are ready to get your data party started! 
![](NerdReady.jpg)
